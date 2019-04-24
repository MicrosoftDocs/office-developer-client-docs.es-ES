---
title: Actualización multiproceso en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- celdas seguras para subprocesos [excel 2007],multithreading en Excel,tareas simultáneas [Excel 2007],funciones seguras para subprocesos [Excel 2007],actualización multiproceso [Excel 2007],MTR [Excel 2007],funciones XLL [Excel 2007], registrar como seguro para subprocesos,actualización [Excel 2007], multiproceso,contención de memoria [Excel 2007],registrar funciones XLL como seguras para subprocesos [Excel 2007],funciones no seguras [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310510"
---
# <a name="multithreaded-recalculation-in-excel"></a>Actualización multiproceso en Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Office Excel 2007 fue la primera versión de Excel en usar la actualización multiproceso (MTR) de hojas de cálculo. Puede configurar Excel para usar hasta 1024 subprocesos simultáneos al actualizar, independientemente del número de procesadores o núcleos de procesador en el equipo. 
  
> [!NOTE]
> Hay una sobrecarga del sistema operativo asociada a cada subproceso, por lo que no debe configurar Excel para usar más subprocesos de los que necesita. 
  
Si el equipo tiene varios procesadores o núcleos de procesador, el sistema operativo asume la responsabilidad de asignar los subprocesos a los procesadores de la manera más eficiente.
  
## <a name="excel-mtr-overview"></a>Información general sobre MTR en Excel

Excel intenta identificar partes de la cadena de cálculo que se pueden actualizar simultáneamente en subprocesos distintos. El siguiente árbol muy sencillo (donde x ← y significa y solo depende de x) muestra un ejemplo de ello.
  
**Figura 1. Cálculo simultáneo en subprocesos distintos**

![Cálculo simultáneo en subprocesos distintos](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Cálculo simultáneo en subprocesos distintos")
  
Después de calcular A1, A2 y A3 pueden calcularse en un subproceso, mientras que B1 y C1 se pueden calcular en otro, suponiendo que todas las celdas son seguras para subprocesos. 
  
> [!NOTE]
> El término “celda segura para subprocesos” se refiere a una celda que solo contiene funciones seguras para subprocesos. Consulte la sección [Qué se considera y qué no se considera seguro para subprocesos en Excel](#xl2007xllsdk_threadsafe) para obtener más información. 
  
Los libros más prácticos contienen árboles de dependencias mucho más complejos que este ejemplo. Además, el tiempo de actualización de una celda no se puede conocer hasta que el cálculo ha finalizado y puede variar enormemente según los argumentos de las funciones. Para obtener los mejores resultados, Excel intenta mejorar el orden de cálculo en cada cálculo hasta que es posible mejorar la optimización.
  
Excel usa un solo subproceso principal para ejecutar lo siguiente:
  
- Comandos integrados
    
- Comandos XLL
    
- Funciones de interfaz del Administrador de complementos XLL (función **xlAutoOpen**, etc.) 
    
- Comandos definidos por el usuario de Microsoft Visual Basic para Aplicaciones (VBA) (a menudo denominadas macros)
    
- Funciones definidas por el usuario de VBA
    
- Funciones integradas de hoja de cálculo no segura para subprocesos (consulte la siguiente sección para obtener una lista)
    
- Funciones y comandos definidos por el usuario de la hoja de macros XLM
    
- Funciones y comandos de complemento COM
    
- Funciones y operadores dentro de las expresiones de formato condicional
    
- Funciones y operadores dentro de las definiciones de nombre definido que se usan en las fórmulas de hoja de cálculo
    
- La evaluación de una expresión en el cuadro de edición de la fórmula con la tecla **F9** 
    
Todas las fórmulas de hoja de cálculo, independientemente de si las funciones son seguras para subprocesos o no, se evalúan en el subproceso principal a menos que Excel esté configurado para usar más de un subproceso. Cuando el usuario especifica que debe usarse más de un subproceso, los subprocesos adicionales se usan para las celdas seguras para subprocesos. Tenga en cuenta que el subproceso principal aún puede usarse para las celdas seguras para subprocesos cuando tiene sentido desde un punto de vista de equilibrio de carga.
  
Conviene reformular que Excel no ejecuta más de un comando a la vez, por lo que no es necesario usar las mismas precauciones que cuando se escriben funciones seguras para subprocesos, como el uso de memoria local para el subproceso y secciones críticas.
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>Qué se considera y qué no se considera seguro para subprocesos en Excel
<a name="xl2007xllsdk_threadsafe"> </a>

En Excel solo se considera seguro para subprocesos lo siguiente:
  
- Todos los operadores unarios y binarios en Excel.
    
- Casi todas las funciones de hoja de cálculo integradas a partir de Excel 2007 (vea la lista de excepciones)
    
- Funciones de complemento XLL que se han registrado explícitamente como seguras para subprocesos.
    
Las funciones de hoja de cálculo integradas que no son seguras para subprocesos son las siguientes:
  
- **PHONETIC**
    
- **CELL** cuando se usa el argumento "format" o "address" 
    
- **INDIRECT**
    
- **GETPIVOTDATA**
    
- **CUBEMEMBER**
    
- **CUBEVALUE**
    
- **CUBEMEMBERPROPERTY**
    
- **CUBESET**
    
- **CUBERANKEDMEMBER**
    
- **CUBEKPIMEMBER**
    
- **CUBESETCOUNT**
    
- **ADDRESS** donde se proporciona el quinto parámetro (sheet_name) 
    
- Ninguna función de base de datos (**BDSUMA**, **BDPROMEDIO**, etc.) que haga referencia a una tabla dinámica
    
- **ERROR.TYPE**
    
- **HYPERLINK**
    
Para ser explícitos, lo siguiente se considera como no seguro:
  
- Funciones definidas por el usuario de VBA
    
- Funciones definidas por el usuario de complemento COM
    
- Funciones definidas por el usuario de hoja de macros XLM
    
- Funciones de complemento XLL que se han registrado explícitamente como seguras para subprocesos
    
Las consecuencias son que las siguientes operaciones y funciones no son seguras para subprocesos y producen un error si se les llama desde una función XLL registrada como segura para subprocesos:
  
- Llamadas a funciones de información XLM, por ejemplo, **xlfGetCell** (**GET.CELL**).
    
- Llamadas a **xlfSetName** (**SET.NAME**) para definir o eliminar nombres internos de XLL.
    
- Llamadas a funciones definidas por el usuario no seguras para subprocesos con **xlUDF**.
    
- Llamadas a la función [xlfEvaluate](xlfevaluate.md) para expresiones que contienen funciones no seguras para subprocesos o que contienen nombres definidos cuyas definiciones contienen funciones no seguras para subprocesos. 
    
- Llamadas a la función [xlAbort](xlabort.md) para borrar una condición de interrupción. 
    
- Llamadas a la función [xlCoerce](xlcoerce.md) para obtener el valor de una referencia de celda no actualizada. 
    
> [!NOTE]
> Las funciones de hoja de cálculo XLL no están permitidas para llamar a los comandos de la API de C, por ejemplo, **xlcSave**, independientemente de si se han registrado como seguras para subprocesos o no. 
  
Dado que las funciones XLL declaradas como seguras para subprocesos no pueden llamar a las funciones de información XLM o hacer referencia a las celdas no actualizadas, Excel no permite que las funciones XLL registrados como equivalentes de hojas de macros se registren también como seguras para subprocesos. Por tanto, al intentar obtener el valor de una referencia de celda no actualizada mediante **xlCoerce** se produce el error **xlretUncalced**. Una llamada a una función de información XLM produce un error **xlretFailed**. Los otros puntos enumerados anteriormente producen un error con un código introducido en la API de C de Excel: **xlretNotThreadSafe**. 
  
Todas las funciones de devolución de llamada solo para API de C son seguras para subprocesos:
  
- **xlCoerce** (excepto cuando haya un error en la coerción de las referencias de celda no actualizadas) 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort** (excepto cuando se usa para borrar una condición de interrupción) 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
La única excepción es la función **xlSet**, que es, en todo caso, equivalente a un comando y no puede llamarse desde ninguna función de hoja de cálculo. 
  
Una función de hoja de cálculo XLL se puede registrar con Excel como segura para subprocesos. Esto indica a Excel que la función puede llamarse de forma segura y simultáneamente en varios subprocesos, aunque debe asegurarse de que realmente es así. Si una función registrada como segura para subprocesos se comporta de forma no segura, probablemente podría desestabilizar Excel.
  
## <a name="registering-xll-functions-as-thread-safe"></a>Registrar funciones XLL como seguras para subprocesos
<a name="xl2007xllsdk_threadsafe"> </a>

Un desarrollador debe cumplir las siguientes reglas al escribir funciones seguras para subprocesos:
  
- No llamar a recursos de otras DLL que posiblemente no sean seguras para subprocesos.
    
- No realizar ninguna llamada no segura para subprocesos a través de la API de C o COM.
    
- Proteger los recursos que más de un subproceso podría usar simultáneamente mediante secciones críticas.
    
- Utilizar la memoria local para el subproceso para el almacenamiento específico de subprocesos y sustituir las variables estáticas dentro de las funciones con variables locales para el subproceso.
    
Excel impone una restricción adicional: las funciones seguras para subprocesos no pueden registrarse como equivalentes de hojas de macros y, por lo tanto, no pueden llamar a funciones de información XLM u obtener los valores de las celdas no actualizadas.
  
## <a name="memory-contention"></a>Contención de memoria
<a name="xl2007xllsdk_threadsafe"> </a>

Los sistemas multiproceso deben resolver dos aspectos fundamentales:
  
- Cómo proteger la memoria en la que más de un subproceso debe leer o escribir.
    
- Cómo crear y consultar memoria que esté asociada y reservada al subproceso en ejecución.
    
El sistema operativo Windows y el Kit de desarrollo de software de Windows ofrecen herramientas para las secciones críticas y la API de almacenamiento local de subprocesos (TLS) respectivamente. Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).
  
El primer problema puede ocurrir, por ejemplo, cuando dos funciones de hoja de cálculo (o dos instancias de la misma función que se ejecutan simultáneamente) necesitan obtener acceso a la variable global o modificarla en un proyecto DLL. Recuerde que esta variable global puede estar oculta en una instancia accesible globalmente de un objeto de clase.
  
El segundo problema puede ocurrir, por ejemplo, cuando una función de hoja de cálculo declara un objeto o una variable estática en el código del cuerpo de la función. El compilador de C o C ++ solo crea una sola copia que usan todas los subprocesos. Esto significa que una instancia de la función podría cambiar el valor, mientras que otra en otro subproceso podría suponer que el valor es el que se estableció previamente.
  
## <a name="example-applications-of-mtr"></a>Aplicaciones de ejemplo de MTR
<a name="xl2007xllsdk_threadsafe"> </a>

Cualquier XLL que exporte funciones de hoja de cálculo puede aprovechar las ventajas de la actualización multiproceso (MTR) en Excel, siempre y cuando esas funciones no necesiten realizar acciones no seguras para subprocesos. Esto permite que Excel actualice los libros que dependen de ellos lo más rápido posible y, por lo tanto, es deseable cualquiera que sea la aplicación.
  
En concreto, MTR tiene un gran impacto en el tiempo actualización de los libros que llaman a funciones definidas por el usuario (UDF) que a su vez llaman a procesos externos para obtener el resultado deseado. En concreto, considere una UDF que llama a un servidor remoto que puede procesar muchas solicitudes al mismo tiempo y un libro que contiene muchas llamadas a esa función. Si la actualización de los libros es uniproceso, cada llamada a la UDF, y por ende al servidor remoto, debe completarse antes de que se pueda realizar la siguiente. Esto supone un desperdicio de la capacidad del servidor para procesar muchas llamadas a la vez. Si la actualización del libro es multiproceso, Excel puede realizar varias llamadas al mismo tiempo o en rápida sucesión.
  
Si Excel se configura para usar el mismo número de subprocesos que el servidor (se le llama N) y la topología del árbol de dependencias del libro lo permite, el tiempo total de actualización podría reducirse a algo cercano a 1/N del tiempo de actualización uniproceso. Esto puede ser verdadero incluso cuando el equipo cliente (en el que el libro se ejecuta) solo tiene un procesador, particularmente cuando el tiempo necesario para realizar la llamada al servidor es pequeño en relación con el tiempo que el servidor tarda en procesar la llamada. 
  
Hay una sobrecarga de sistema operativo para cada subproceso adicional. Por lo tanto, puede necesitarse un poco de experimentación para que un libro determinado y un servidor y un equipo cliente determinados busquen el número óptimo de subprocesos que Excel puede usar. 
  
Por ejemplo, piense en un equipo con un solo procesador que ejecuta Excel y un libro que contiene 1000 celdas. Este llama a una UDF, que a su vez llama a uno o más servidores remotos. Suponga que las 1000 celdas no dependen unas de otras, de modo que Excel no tiene que esperar a que se complete una llamada para poder realizar la siguiente. (Es posible relajar un poco esta restricción sin afectar a este ejemplo). Si los servidores pueden procesar 100 solicitudes al mismo tiempo, y Excel está configurado para usar 100 subprocesos, el tiempo de ejecución puede reducirse hasta 1/100 parte de aquel donde solo se usa un subproceso. La sobrecarga que se asocia con Excel al asignar llamadas a cada subproceso y con el sistema operativo al administrar 100 subprocesos significa que, en la práctica, la reducción no será tan grande. También hay aquí un supuesto implícito de que el servidor se escala bien y, al solicitarle que procese 100 tareas al mismo tiempo, no se afectará significativamente a la finalización de tareas individuales.
  
Una aplicación práctica en la que esta técnica puede tener una importante ventaja es la de los métodos de Monte Carlo, así como otras tareas numéricamente intensivas que se pueden dividir en subtareas más pequeñas que pueden asignarse a los servidores.
  
## <a name="excel-services-considerations"></a>Consideraciones sobre Excel Services
<a name="xl2007xllsdk_threadsafe"> </a>

Excel Services admite la carga, el cálculo y la representación de hojas de cálculo de Excel en un servidor. Los usuarios pueden tener acceso a las hojas de cálculo e interactuar con ellas mediante herramientas estándar del explorador.
  
Las UDF de Excel Services se crean con un código administrado de Microsoft .NET Framework y se publican a través de un ensamblado de .NET. Los XLL no son compatibles con Excel Services. Un recurso de UDF de servidor de código administrado puede llamar a un XLL para obtener acceso a su funcionalidad, de modo que el usuario puede tener la misma funcionalidad con un libro cargado en el servidor que con un libro cargado en el cliente.
  
Por lo tanto, para disponer de las funciones de un XLL de esta forma, deben ajustarse en un ensamblado de .NET que convierta argumentos y valores devueltos de los tipos de datos nativos a los tipos de datos administrados de .NET Framework y que llame a las funciones XLL. El contenedor de .NET exportará una UDF de servidor para cada función XLL a la que se tiene acceso. Un requisito adicional es que las funciones XLL denominadas así deben ser seguras para subprocesos. Dado que las funciones XLL no se registran de la misma forma que Excel del cliente, el servidor y el contenedor de .NET no tienen manera de exigir que sean seguras para subprocesos. Es responsabilidad del desarrollador de XLL garantizarlo.
  
## <a name="see-also"></a>Vea también

- [Actualización de Excel](excel-recalculation.md)  
- [Administración de memoria en Excel](memory-management-in-excel.md) 
- [Obtener acceso a código XLL en Excel](accessing-xll-code-in-excel.md)  
- [Conceptos de programación de Excel](excel-programming-concepts.md)  
- [Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

