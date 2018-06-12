---
title: Nuevo cálculo multiproceso en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- las celdas de seguros para subprocesos [excel 2007], subprocesamiento múltiple en Excel, tareas simultáneas [Excel 2007], funciones de seguros para subprocesos [Excel 2007], multiproceso recálculo [Excel 2007], MTR [Excel 2007], funciones XLL [Excel 2007], registrar como subprocesos, [recálculo Excel 2007], memoria multiproceso, contención [Excel 2007], registrar XLL funciona como subprocesos funciones no seguras de seguros [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815687"
---
# <a name="multithreaded-recalculation-in-excel"></a>Nuevo cálculo multiproceso en Excel

**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Office Excel 2007 fue la primera versión de Excel para usar el nuevo cálculo multiproceso (MTR) de hojas de cálculo. Puede configurar Excel para usar hasta subprocesos simultáneos 1024 al volver a calcular, independientemente del número de procesadores o núcleos de procesador en el equipo. 
  
> [!NOTE]
> No hay un sistema operativo sobrecarga asociado con cada subproceso, por lo que no debe configurar Excel para usar más subprocesos de los que necesita. 
  
Si el equipo tiene varios procesadores o núcleos de procesador, el sistema operativo tiene responsabilidad de asignación de los subprocesos a los procesadores de la manera más eficaz.
  
## <a name="excel-mtr-overview"></a>Introducción a Excel MTR

Excel intenta identificar las partes de la cadena de cálculo que se pueden volver a calcularse simultáneamente en distintos subprocesos. El siguiente árbol muy simple (donde x ← y significa y sólo depende de x), muestra un ejemplo de esto.
  
**En la figura 1. Cálculo simultáneo en distintos subprocesos**

![Cálculo simultáneo en distintos subprocesos] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Cálculo simultáneo en distintos subprocesos")
  
Una vez que se calcula A1, A2 y, a continuación, A3 se pueden calcular en un subproceso mientras B1 y, a continuación, C1 se pueden calcular en otro, suponiendo que todas las celdas son seguros para subprocesos. 
  
> [!NOTE]
> La celda de seguros para subprocesos términos significa una celda que contiene sólo las funciones de subprocesos. ¿Qué es y no es segura para subprocesos se detallan [es no considera subproceso seguros por Excel y ¿qué es](#xl2007xllsdk_threadsafe). 
  
Los libros más prácticos contienen árboles de dependencia mucho más complejos que en este ejemplo. Además, no se puede conocer la hora de actualización de una celda hasta que se realiza un cálculo y se puede variar mucho dependiendo de los argumentos de las funciones. Para obtener los mejores resultados, Excel intenta mejorar el orden de cálculo en todos los cálculos hasta que es posible mejorar la optimización.
  
Excel utiliza un único subproceso principal para ejecutar o ejecutar lo siguiente:
  
- Comandos integrados
    
- Comandos XLL
    
- Funciones de interfaz de administrador de complementos XLL (función**xlAutoOpen** y así sucesivamente) 
    
- Microsoft Visual Basic para aplicaciones (VBA) definidas por el usuario los comandos (que suele denominados macros)
    
- Funciones definidas por el usuario VBA
    
- Funciones integradas de hoja de cálculo no seguras subproceso (vea la sección siguiente para obtener una lista)
    
- Funciones y comandos definidas por el usuario de la hoja de macros XLM
    
- Funciones y comandos de complementos COM
    
- Funciones y operadores dentro de las expresiones de formato condicionales
    
- Funciones y operadores dentro de las definiciones de nombre definido que se utiliza en las fórmulas de la hoja de cálculo
    
- La evaluación de una expresión en el cuadro Editar fórmula con la tecla **F9** forzada 
    
Todas las fórmulas de hoja de cálculo, independientemente de si las funciones son seguros para subprocesos o no, se evalúan en el subproceso principal a menos que Excel está configurado para usar más de un subproceso. Cuando el usuario especifica que se debe usar más de un subproceso, los subprocesos adicionales se utilizan para las celdas de seguros para subprocesos. Tenga en cuenta que el subproceso principal aún se puede usar para las celdas de seguros para subprocesos cuando tenga sentido desde el punto de equilibrio de carga de vista.
  
Merece la pena reformular que Excel no ejecute más de un comando a la vez, por lo que no es necesario emplear las mismas precauciones como cuando se escriben funciones de seguros para subprocesos, como el uso de memoria de proceso local y secciones críticas.
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>¿Qué es y no se considera subproceso seguros por Excel
<a name="xl2007xllsdk_threadsafe"> </a>

Excel sólo tiene en cuenta lo siguiente como subproceso seguro:
  
- Todos los operadores unario y binario de Excel.
    
- Casi todas las funciones de hoja de cálculo integradas a partir de Excel 2007 (vea la lista de excepciones)
    
- En Agregar funciones XLL que se han registrado explícitamente como seguros para subprocesos.
    
Las funciones de hoja de cálculo integradas que no son seguros para subprocesos son:
  
- **FONÉTICO**
    
- **Celda** cuando se utiliza el "formato de" o la "dirección" argumento 
    
- **INDIRECT**
    
- **GETPIVOTDATA**
    
- **CUBEMEMBER**
    
- **CUBEVALUE**
    
- **CUBEMEMBERPROPERTY**
    
- **CUBESET**
    
- **CUBERANKEDMEMBER**
    
- **CUBEKPIMEMBER**
    
- **CUBESETCOUNT**
    
- **Dirección** donde se proporciona el quinto parámetro (sheet_name) 
    
- Cualquier función de base de datos (**DSUM**, **DAVERAGE**etc.) que hace referencia a una tabla dinámica
    
- **ERROR. TIPO DE**
    
- **HIPERVÍNCULO**
    
Para que sea explícito, las siguientes se consideran no seguras:
  
- Funciones definidas por el usuario VBA
    
- Complemento definidas por el usuario funciones COM
    
- Funciones definidas por el usuario de hoja de macros XLM
    
- Funciones de complementos XLL registran no explícitamente como seguros para subprocesos
    
Las implicaciones son que las siguientes operaciones y funciones no son seguros para subprocesos y producirá un error si se les llama desde una función XLL registrada como seguros para subprocesos:
  
- Llama a las funciones de información XLM, por ejemplo, **xlfGetCell** (**GET. CELDA**).
    
- Llama a **xlfSetName** (**SET.NAME**) para definir o eliminar nombres internos de XLL.
    
- Llamadas a funciones no seguras subproceso definidas por el usuario mediante **xlUDF**.
    
- Llama a la función [xlfEvaluate](xlfevaluate.md) para expresiones que contienen funciones no seguras subproceso o que contienen nombres definidos cuyas definiciones contienen funciones no seguras subproceso. 
    
- Llamadas a la función [xlAbort](xlabort.md) para borrar una condición de interrupción. 
    
- Llamadas a la función [xlCoerce](xlcoerce.md) para obtener el valor de una referencia de celda no calculada. 
    
> [!NOTE]
> No se permiten las funciones de hoja de cálculo XLL para llamar a los comandos de la API de C, por ejemplo, **xlcSave**, independientemente de si se han registrado como seguros para subprocesos o no. 
  
Dado que las funciones XLL declaran como seguros para subprocesos no se puede llamar a las funciones de información XLM o referencia a celdas sin calcular, Excel no permite funciones XLL que se registran como equivalentes de hojas de macro también debe registrarse como seguros para subprocesos. Por lo tanto, si se intenta obtener el valor de una referencia de celda no calculada mediante **xlCoerce** produce el error **xlretUncalced** . Llamar a un XLM función de la información se produce un error con un error **xlretFailed** . Los otros puntos enumerados anteriormente producirá un error con un código de error que se introdujo en la API de C de Excel: **xlretNotThreadSafe**. 
  
Las funciones de devolución de llamada sólo API de C son seguros para todos los subprocesos:
  
- **xlCoerce** (excepto aunque coerción de celda no calculada hace referencia se produce un error) 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort** (excepto cuando se utiliza para borrar una condición de interrupción) 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
La única excepción es la función **xlSet** , que es, en cualquier caso, un equivalente de comando y por lo tanto no se puede llamar desde ninguna función de hoja de cálculo. 
  
Una función de hoja de cálculo XLL puede estar registrada con Excel como seguros para subprocesos. Esto indica a Excel que la función se puede llamar de forma segura y simultáneamente en varios subprocesos, si bien, debe asegurarse de que éste es realmente el caso. Posiblemente puede desestabilizar Excel si una función registrada como seguros para subprocesos, a continuación, se comporta de forma no segura.
  
## <a name="registering-xll-functions-as-thread-safe"></a>Registrar funciones XLL como seguros para subprocesos
<a name="xl2007xllsdk_threadsafe"> </a>

Las reglas que un programador debe cumplir al escribir funciones de subprocesos son los siguientes:
  
- No llame a recursos de otras DLL que puede no ser seguros para subprocesos.
    
- No realice las llamadas no seguras subproceso a través de la API de C o COM.
    
- Proteger los recursos que podrían utilizarse simultáneamente por más de un subproceso mediante secciones críticas.
    
- Utilizar memoria local de subprocesos para el almacenamiento de específicas de un subproceso y sustituir las variables estáticas dentro de las funciones con variables locales de subproceso.
    
Excel impone una restricción adicional: funciones de subprocesos no se puede registrar como equivalentes de la hoja de macros y por lo tanto, no se pueden llamar a las funciones de información XLM u obtener los valores de celdas no vuelve a calcular.
  
## <a name="memory-contention"></a>Contención de memoria
<a name="xl2007xllsdk_threadsafe"> </a>

Sistemas multiproceso deben solucionar dos problemas fundamentales:
  
- Procedimiento para proteger la memoria que debe ser leen o escriben en, por más de un subproceso.
    
- Procedimiento para crear y obtener acceso a memoria que está asociado con y, a continuación, por lo que privada al subproceso en ejecución.
    
El sistema operativo Windows y el Kit de desarrollo de Software (SDK) de Windows proporcionan herramientas para estos dos: las secciones críticas y la API de almacenamiento local de subprocesos (TLS) respectivamente. Para obtener m�s informaci�n, consulte [Administraci�n de memoria en Excel](memory-management-in-excel.md).
  
Por ejemplo, el primer problema puede surgir cuando dos funciones de hoja de cálculo (o dos instancias de la misma función simultáneamente ejecución) necesitan tener acceso o modificar una variable global en un proyecto de DLL. Recuerde que este tipo de variable global podría estar oculto en una instancia de un objeto de clase globalmente accesible.
  
El segundo problema puede surgir, por ejemplo, cuando una función de hoja de cálculo que declara una variable estática o un objeto dentro del código del cuerpo de la función. El compilador de C o C++ sólo crea una única copia que usan todos los subprocesos. Esto significa que una instancia de la función puede cambiar el valor, mientras que otra en un subproceso diferente podría ser suponiendo que el valor es qué lo establecido anteriormente.
  
## <a name="example-applications-of-mtr"></a>Aplicaciones de ejemplo de MTR
<a name="xl2007xllsdk_threadsafe"> </a>

Cualquier XLL que exporta las funciones de hoja de cálculo puede aprovechar la actualización del cálculo multiproceso (MTR) en Excel siempre que dichas funciones no es necesario llevar a cabo acciones no seguras subproceso. Esto permite que Excel para volver a calcular libros que dependen de ellos tan pronto como sea posible y es, por tanto, lo deseable que la aplicación.
  
En concreto, MTR tiene un impacto enorme en el tiempo de actualización de los libros que llaman a funciones definidas por el usuario (UDF) que ellos mismos llamar a procesos externos para obtener el resultado deseado. En concreto, considere la posibilidad de una UDF que llame a un servidor remoto que puede procesar simultáneamente muchas solicitudes y un libro que contiene todas las llamadas a esa función. Si recálculo del libro tiene un único subproceso, cada uno de ellos llamar a las UDF y, por lo que en el servidor remoto, debe completar antes de hacer lo siguiente. Se pierde la capacidad del servidor para procesar todas las llamadas a la vez. Si el nuevo cálculo del libro es multiproceso, Excel puede realizar varias llamadas al mismo tiempo o en una sucesión rápida.
  
Si Excel está configurada para usar el mismo número de subprocesos que el servidor: llamar N — y la topología del árbol de la dependencia del libro lo permita, se podría reducir el tiempo total para algo alcanzando 1/N del tiempo de cálculo de un único subproceso. Esto puede ser cierto incluso cuando el equipo cliente (en el que el libro se está ejecutando) sólo tiene un procesador, especialmente donde el tiempo necesario para realizar la llamada al servidor es pequeño en relación con el tiempo que tarda el servidor en proceso de la llamada. 
  
Hay sobrecarga de sistema operativo para cada subproceso adicional. Por lo tanto, es posible que algunos experimentación necesario para un libro determinado y un servidor determinado y el equipo cliente para encontrar el número óptimo de subprocesos de que Excel se debe indicar a usar. 
  
Por ejemplo, considere la posibilidad de un equipo de procesador único que ejecuta Excel y un libro que contiene las celdas de 1.000. Se llama a UDF, que llama a su vez uno o varios servidores remotos. Se supone que las 1.000 celdas no dependen de la otra, por lo que Excel no hay que esperar a una llamada para llevar a cabo antes de llamar a la siguiente. (Algunas descanso de esta restricción es posible sin que ello afecte en este ejemplo). Si los servidores pueden procesar las solicitudes de 100 simultáneamente, y Excel está configurado para usar 100 subprocesos, se pueden reducir el tiempo de ejecución con tan sólo 1/100 de ese where sólo un subproceso que se utiliza. La sobrecarga es decir asociados con Excel asignación de llamadas para cada subproceso y el sistema operativo de administración de 100 subprocesos significa que, en la práctica, la reducción no será un proceso bastante este excelente. También hay una suposición implícita aquí que el servidor funciona bien y solicitando que procesar 100 tareas simultáneamente no afectará a los tiempos de finalización de tareas individuales considerablemente.
  
Una aplicación práctica en la que esta técnica puede tener una ventaja importante es de métodos de Monte Carlo, así como otras tareas numéricamente intensivos que se pueden dividir en las subtareas más pequeñas que pueden se puede asignar a los servidores.
  
## <a name="excel-services-considerations"></a>Consideraciones sobre servicios de Excel
<a name="xl2007xllsdk_threadsafe"> </a>

Excel Services admite la carga, calcular y la representación de hojas de cálculo de Excel en un servidor. Los usuarios pueden, a continuación, obtener acceso e interactuar con las hojas de cálculo mediante el uso de herramientas de explorador estándar.
  
UDF de Excel Services se crean mediante código administrado de Microsoft .NET Framework y disponible aunque un ensamblado. NET. No se admiten los XLL de Excel Services. Un servidor recursos UDF de código administrado puede llamar a un XLL para tener acceso a su funcionalidad, por lo que el usuario puede tener la misma funcionalidad con un libro cargado en servidor al igual que con un libro cargado por el cliente.
  
Para disponer de las funciones de los XLL de esta manera, que por lo tanto, se deben ajustan en un ensamblado de .NET para los tipos de datos administrados de .NET Framework que convierte los argumentos y valores devueltos de los tipos de datos nativos y que llama a las funciones XLL. El contenedor de .NET exportará un UDF de servidor para cada función XLL que se tiene acceso. Un requisito adicional es que las funciones XLL llamadas de esta forma deben ser seguros para subprocesos. Debido a que las funciones XLL no están registradas en el modo en que son con el cliente de Excel, el servidor y el contenedor de .NET no tienen ninguna manera de exigir que son seguros para subprocesos. Es responsabilidad del desarrollador XLL para asegurarse de esto.
  
## <a name="see-also"></a>Ver también

- [Actualización de Excel](excel-recalculation.md)  
- [Administraci�n de memoria en Excel](memory-management-in-excel.md) 
- [Acceso al código XLL en Excel](accessing-xll-code-in-excel.md)  
- [Conceptos de programaci�n de Excel](excel-programming-concepts.md)  
- [Referencia de funciones de API de SDK de XLL de Excel 2013](excel-xll-sdk-api-function-reference.md)

