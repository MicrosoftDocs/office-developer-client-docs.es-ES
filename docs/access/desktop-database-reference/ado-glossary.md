---
title: ActiveX Glosario de objetos de datos (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ecb6208a8c970f037cb0ac699c947544eb8f547
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284837"
---
# <a name="ado-glossary"></a>Glosario de ADO

**Se aplica a:** Access 2013, Office 2013

## <a name="a"></a>A

**URL absoluta**

Una dirección URL completa que especifica la ubicación de un recurso que reside en Internet o en una intranet. Vea también **DIRECCIÓN URL** y dirección **URL relativa.**

**Control ActiveX**

Componente COM en proceso de registro propio que a menudo tiene un elemento visual en tiempo de diseño o en tiempo de ejecución. ActiveX controles también tienen la capacidad de comunicarse con un contenedor de documentos activos, como Microsoft Internet Explorer.

**ADISAPI (Interfaz avanzada de programación de aplicaciones de Internet Server de datos)**

Dll isapi que proporciona análisis, control de automatización, serialización **de** conjuntos de registros y empaquetado MIME. El componente ADISAPI funciona a través de la API proporcionada por Internet Information Services (IIS). Vea también **ISAPI**.

**función de agregado**

En una consulta, una función como COUNT, AVG o STDEV que calcula un valor usando todas las filas de una columna de una tabla. Al escribir expresiones y en la programación, puede usar SQL de agregado (incluidas las tres enumeradas anteriormente) y funciones de agregado de dominio para determinar varias estadísticas.

**alias**

Un nombre alternativo que se da a una columna o expresión de una instrucción SELECT SQL, a menudo más corta o más significativa. Por ejemplo, BobSales es el alias de la siguiente instrucción SELECT: "Select wr-Sales as BobSales from SalesDB". Se puede usar un alias para asignar dinámicamente columnas a enlaces de control en el **objeto DataControl.**

**subprocesos de apartamento**

Modelo de subproceso COM donde todas las llamadas a un objeto se producen en un subproceso. En el subproceso de departamentos, COM sincroniza y serializa las llamadas. Vea también **COM**.

**operación asincrónica**

Operación que devuelve el control al programa de llamada sin esperar a que se complete la operación. Antes de que se complete la operación, la ejecución de código continúa. Vea también **operación sincrónica**.

Volver al principio

## <a name="b"></a>B

**entrada de enlace**

Asignación entre un campo de una tabla y una variable. En las extensiones de Visual C++ de ADO, los campos **Recordset** se asignan a variables de C/C++.

**máscara de bits**

Un valor numérico destinado a una comparación de valores bit a bit con otros valores numéricos, normalmente para marcar opciones en valores de parámetro o valores devueltos. Normalmente, esta comparación se realiza con operadores lógicos bit a bit, como **And** y **Or** en Visual Basic y **&** en **|** C++.

Por ejemplo, los valores de ADO **FieldAttributeEnum** se pueden usar como máscaras de bits para determinar los atributos de un campo. Supongamos que desea determinar si un campo se puede actualizar. Puede probar esto con la siguiente expresión en Visual Basic:  
  

Si el resultado es TRUE, el campo se puede actualizar.

**bookmark**

Marcador que identifica de forma única una fila dentro de un conjunto de filas para que un usuario pueda navegar rápidamente a ella.

**objeto de negocios**

Un objeto que realiza un conjunto definido de operaciones, como validación de datos o lógica de regla de negocio. Los objetos de negocio suelen residir en el nivel intermedio.

**regla de negocio**

La combinación de ediciones de validación, comprobaciones de inicio de sesión, búsquedas de bases de datos, directivas y transformaciones algorítmicas que constituyen la forma de hacer negocios de una empresa. También conocido como *lógica de negocios*.

Volver al principio

## <a name="c"></a>C

**expresión calculada**

Expresión que no es constante, pero cuyo valor depende de otros valores. Para ser evaluada, una expresión calculada debe obtener y calcular valores de otros orígenes, normalmente en otros campos o filas.

**capítulo**

Referencia a un rango de filas de un origen de datos. En ADO, un capítulo suele ser una referencia a otro **objeto Recordset**.

Las columnas de capítulo permiten definir una relación de *objeto primario-objeto secundario* donde el *objeto primario* es el objeto **Recordset** que contiene la columna de capítulo y el *objeto secundario* es el objeto **Recordset** representado por el capítulo.

**alias de capítulo**

Alias que hace referencia a la columna anexada al elemento primario.

**juego de caracteres**

Asignación de un conjunto de caracteres a sus valores numéricos. Por ejemplo, Unicode es un conjunto de caracteres de 16 bits capaz de codificar todos los caracteres conocidos y se usa como un estándar de codificación de caracteres en todo el mundo.

**child**

El lado dependiente de una relación jerárquica. Un elemento secundario es un nodo de una estructura jerárquica que tiene otro nodo encima (más cerca de la raíz). Vea también **child-alias**, **parent-child relationship**, **parent**.

**alias secundario**

Alias que hace referencia al elemento secundario. Vea también **alias**, **child**.

**CLSID (identificador de clase)**

Un identificador único universal (UUID) que identifica un componente COM. Cada componente COM tiene su CLSID en el registro Windows para que otras aplicaciones puedan cargarlo. Vea también **ProgID**, **COM**.

**nivel de cliente**

Una capa lógica de un sistema distribuido que normalmente presenta datos y procesa la entrada del usuario, a veces denominada *front-end*. Normalmente, el nivel de cliente solicita datos de un servidor en función de la entrada y, a continuación, da formato y muestra el resultado. Vea también **nivel intermedio,** **nivel de origen de datos,** **aplicación distribuida.**

**COM (modelo de objetos de componente)**

Un estándar binario que permite a los objetos interoperar en un entorno en red independientemente del idioma en el que se desarrollaron o en qué equipos residen. Las tecnologías basadas en COM incluyen ActiveX controles, automatización y vinculación e inserción de objetos (OLE). COM permite que un objeto exponga su funcionalidad a otros componentes y a las aplicaciones host. Define tanto cómo se expone el objeto como cómo funciona esta exposición en todos los procesos y entre redes. COM también define el ciclo de vida del objeto.

**Componente COM**

Archivo binario , como .dll, .ocx y algunos archivos .exe, que admite el estándar COM para proporcionar objetos. Este archivo contiene código para una o varias fábricas de clases, clases COM, mecanismos de entrada del Registro, código de carga, etc.

**operador de comparación**

Operador que compara dos expresiones y devuelve un valor booleano.

Parámetro criteria que puede expresarse como " \> " (mayor que), \< " " (menor que), "=" (igual), " =" (mayor o \> igual), " \< =" (menor o igual), " \< \> " (no igual) o "like" (coincidencia de patrones).

**component**

Un objeto que encapsula los datos y el código y proporciona un conjunto bien especificado de servicios disponibles públicamente.

**archivo compuesto**

Una implementación del almacenamiento estructurado COM para archivos. Un archivo compuesto almacena objetos independientes en un único archivo estructurado formado por dos elementos principales: objetos de almacenamiento y objetos de secuencia. Juntos, funcionan como un sistema de archivos dentro de un archivo. Para obtener más información, consulte Compound Files in the Microsoft Platform SDK.

Varios archivos individuales enlazados en un archivo físico. Se puede tener acceso a cada archivo individual de un archivo compuesto como si se tratase de un único archivo físico.

**constante**

Valor numérico o de cadena que no cambia. Las enumeraciones con nombre ADO (constantes enumeradas) se pueden usar en el código en lugar de los valores reales, por ejemplo, **adUseClient** es una constante cuyo valor es 3. (Const adUseClient = 3). Vea también **enumeración**.

**cursor**

Elemento de base de datos que controla la navegación de registros, la actualización de los datos y la visibilidad de los cambios realizados en la base de datos por otros usuarios.

Volver al principio

## <a name="d"></a>D

**enlace de datos**

Proceso de asociación de los objetos o controles de una aplicación a un origen de datos. Un control asociado a un origen de datos se denomina control enlazado a *datos*.

El contenido de un control enlazado a datos está asociado a valores de una base de datos. Por ejemplo, un control de cuadrícula enlazado a un **objeto Recordset** se puede actualizar cuando se actualizan las filas del **objeto Recordset.** Cuando el objeto **Recordset** recupera nuevos valores, se muestran nuevos valores en la cuadrícula.

**proveedor de datos**

Software que expone datos a una aplicación de ADO directamente o a través de un proveedor de servicios. Vea también **proveedor de servicios**.

**forma de datos**

Una técnica que usa una sintaxis formalizada (denominada Lenguaje **de** formas) para definir un objeto **Recordset** especializado (denominado Recordset **con** forma) que contiene no solo datos, sino también referencias a otros objetos **Recordset** o valores calculados basados en esos otros objetos **Recordset.**

**nivel de origen de datos**

Una capa lógica de un sistema distribuido que representa un equipo que ejecuta un DBMS, como una base SQL Server datos. Vea también **nivel de cliente,** **nivel intermedio,** **aplicación distribuida.**

**DCOM**

Un protocolo de cable que permite que los componentes COM se comuniquen directamente entre sí a través de una red. Vea también **COM**, **component**.

**DDL (lenguaje de definición de datos)**

Las instrucciones de SQL que definen, en lugar de manipular, los datos. El esquema de una base de datos se crea o modifica con DDL. Por ejemplo, **CREATE TABLE**, **CREATE INDEX,** **GRANT** y **REVOKE** son SQL instrucciones DDL.

**secuencia predeterminada**

Un texto o secuencia binaria (representado por un **objeto Stream)** que está asociado con objetos **Record** o **Recordset** cuando se usan determinados proveedores OLE DB, como el proveedor microsoft OLE DB para publicación en Internet. La secuencia predeterminada normalmente contiene el contenido de un archivo, como el código HTML de la raíz de un sitio web.

**aplicación distribuida**

Un programa escrito para que el procesamiento se pueda dividir entre varios equipos a través de una red. Normalmente, una aplicación distribuida se divide en capas de presentación, lógica empresarial y almacén de datos o *niveles.* Vea también **nivel de cliente,** **nivel intermedio,** **nivel de origen de datos.**

**recordset desconectado**

Un **objeto Recordset** en una memoria caché de cliente que ya no tiene una conexión activa al servidor. Si es necesario tener acceso de nuevo al origen de datos original por algún motivo, como la actualización de datos, se debe volver a establecer la conexión. Sin embargo, se puede obtener acceso a las colecciones, propiedades y métodos de un **objeto Recordset** desconectado.

**DLL (biblioteca de vínculos dinámicos)**

Un archivo que contiene una o más funciones compiladas, vinculadas y almacenadas por separado de los procesos que las usan. El sistema operativo asigna las DLL al espacio de direcciones del proceso de llamada cuando se inicia el proceso o mientras se está ejecutando.

**DML (lenguaje de manipulación de datos)**

Las instrucciones de SQL que manipulan, en lugar de definir, los datos. Los valores de una base de datos se seleccionan y modifican con DML. Por ejemplo, **INSERT,** **UPDATE,** **DELETE** y **SELECT** son SQL instrucciones DML.

**proveedor de origen de documentos**

Una clase especial de proveedores que administran carpetas y documentos. Cuando un documento está representado por un **objeto Record** o una carpeta de documentos está representada por un objeto **Recordset,** el proveedor de origen de documentos rellena esos objetos con un conjunto único de campos que describen las características del documento, en lugar del propio documento real. Vea también **registro de recursos**.

**DSN (nombre del origen de datos)**

La colección de información que se usa para conectar la aplicación a una base de datos ODBC determinada. El Administrador de controladores ODBC usa esta información para crear una conexión a la base de datos. Un DSN se puede almacenar en un archivo (un archivo DSN) o en el registro de Windows (un DSN de máquina).

**dynamic (propiedad)**

Propiedad específica de un proveedor de datos o del servicio de cursores. La **colección Properties** de un objeto se rellena con estos automáticamente ("dinámicamente"). Un objeto no tiene propiedades dinámicas hasta que se conecta a un origen de datos a través de un proveedor de datos determinado. Vea también **proveedor de datos**, **cursor**.

Volver al principio

## <a name="e-i"></a>E-I

**enumeración**

Una lista de constantes con nombre. Los valores enumerados no deben ser únicos. Sin embargo, el nombre de cada valor debe ser único dentro del ámbito donde se define la enumeración. En ADO, las enumeraciones se usan para parámetros numéricos y valores devueltos, para agregar significado al código de ADO y para proteger al desarrollador de los valores numéricos (que pueden cambiar de versión a versión). Por ejemplo, para abrir un conjunto de **registros estático**, use el valor **enumerado adOpenStatic:**  
  

También se conoce como constante *enumerada*. Vea también **constante**.

**evento**

Una acción reconocida por un objeto, para la que puede escribir código para responder. Los eventos se pueden generar mediante la ejecución de comandos, la finalización de transacciones, la navegación del conjunto de registros y las actualizaciones de datos, entre otras acciones. Vea también controlador **de eventos**.

**controlador de eventos**

Un controlador de eventos es el código que se ejecuta cuando se produce un evento. Vea también **el evento**.

**handler**

Una rutina que administra una condición u operación común y relativamente sencilla, como la recuperación de errores o la administración de datos.

**conjunto de registros jerárquico**

Conjunto **de registros** que contiene otro objeto **Recordset**. Vea también **forma de datos**, **capítulo**.

Para obtener más información, vea [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)

**jerarquía**

En general, una jerarquía es una estructura clasificada con un nivel superior y niveles subordinados. En ADO, se usan **conjuntos de registros jerárquicos** para representar la relación primario-secundario entre un registro y un capítulo. También en ADO, **los objetos Record** y **Stream** se pueden usar para tener acceso a estructuras jerárquicas de árbol, como una carpeta y documentos. ADO MD también incluye **objetos Hierarchy** para representar una relación entre los niveles de una dimensión en un cubo OLAP. Vea también **conjuntos de registros jerárquicos**, **relación primario-secundario**, **capítulo**, **árbol**.

**ISAPI (Interfaz de programación de aplicaciones de Internet Server)**

Un conjunto de funciones para servidores de Internet, como un servidor WINDOWS NT/Windows 2000 Server que ejecuta Microsoft Internet Information Services (IIS).

Volver al principio

## <a name="k-m"></a>K-M

**key**

Columna o columnas de una tabla que identifican de forma única una fila; a menudo se usa para indizar una tabla.

**marshaling**

Proceso de empaquetado, envío y desembalaje de parámetros del método de interfaz entre los límites de subprocesos o procesos.

**nivel intermedio**

La capa lógica de un sistema distribuido entre una interfaz de usuario o un cliente web y la base de datos. Suele ser aquí donde se crea una instancia de objetos de negocio. El nivel intermedio es una colección de reglas y funciones empresariales que generan y operan al recibir información. Lo logran a través de reglas de negocio, que pueden cambiar con frecuencia y, por lo tanto, se encapsulan en componentes que están físicamente separados de la propia lógica de la aplicación. También conocido como nivel *de servidor de aplicaciones*. Vea también **aplicación distribuida,** **nivel de cliente,** **nivel de origen de datos.**

**MIME (extensión multipropósito de correo de Internet)**

Un protocolo de Internet desarrollado originalmente para permitir el intercambio de mensajes de correo electrónico con contenido enriquecido en entornos heterogéneos de red, máquina y correo electrónico. En la práctica, MIME también se ha adoptado y extendido por aplicaciones que no son de correo.

MIME es un estándar que permite publicar y leer datos binarios en Internet. El encabezado de un archivo con datos binarios contiene el tipo MIME de los datos; esto informa a los programas cliente (exploradores web y paquetes de correo, por ejemplo) de que tendrán que controlar los datos de una forma diferente a la que manejan el texto recto. Por ejemplo, el encabezado de un documento web que contiene un gráfico JPEG contiene el tipo MIME específico del formato de archivo JPEG. Esto permite que un explorador muestre el archivo con su visor JPEG, si está presente.

Volver al principio

## <a name="n-o"></a>N-O

**nodo**

Elemento de una estructura jerárquica de árbol. Un nodo puede ser la raíz o el elemento secundario de otro nodo. Un nodo también puede ser el elemento primario de varios elementos secundarios. Vea también **jerarquía**, **árbol**, **raíz**, **secundario**, **primario**.

**variable de objeto**

Variable que contiene una referencia a un objeto. Por ejemplo, objCustomObject es una variable que apunta a un objeto de tipo CustomObject:  
  
es una variable que apunta a un objeto de tipo CustomObject:  
  
Set objCustomObject = CreateObject(adodb. Recordset)

**ODBC (Conectividad abierta de bases de datos)**

Una interfaz de lenguaje de programación estándar que se usa para conectarse a una variedad de orígenes de datos. Normalmente se tiene acceso a esto a través del Panel de control, donde se pueden asignar nombres de origen de datos (DSN) para usar controladores ODBC específicos.

**OLE DB**.

Un conjunto de interfaces que exponen datos de una variedad de orígenes mediante COM. Las interfaces OLE DB proporcionan a las aplicaciones un acceso uniforme a los datos almacenados en diversos orígenes de información. Estas interfaces admiten la cantidad de funcionalidad dbms adecuada para el origen de datos, lo que le permite compartir sus datos. Vea también **COM**.

**bloqueo optimista**

Un tipo de bloqueo en el que la página de datos que contiene uno o varios registros, incluido el registro que se está editando, no está disponible para otros usuarios solo mientras el método **Update** actualiza el registro, pero está disponible antes y después de la llamada a **Update**.

El bloqueo optimista se usa cuando se abre el objeto **Recordset** con el parámetro **LockType** o la propiedad establecido en **adLockOptimistic** o **adLockBatchOptimistic**. Vea también **bloqueo pesimista**.

**Valor ordinal**

Ubicación numérica de un elemento dentro de un pedido. En una colección ADO, el valor ordinal del primer elemento es cero (0). El siguiente elemento es uno (1), y así sucesivamente.

Volver al principio

## <a name="p"></a>P

**comando parametrizado**

Consulta o comando que permite establecer valores de parámetro antes de ejecutar el comando. Por ejemplo, una cadena SQL se puede parametrizar insertando marcadores de parámetros en la cadena SQL (designada por el carácter '?'). A continuación, la aplicación especifica los valores de cada parámetro y ejecuta el comando.

**primario**

El lado controlador de una relación jerárquica. En una estructura jerárquica, un elemento primario tiene uno o varios nodos secundarios directamente debajo de ella en la jerarquía. Vea también **parent-alias**, **parent-child relationship**, **child**.

**alias primario**

Alias que hace referencia al elemento primario. Vea también **alias**, **parent**.

**relación parent-child**

Relación en una estructura jerárquica en la que el elemento primario es un nivel superior y está directamente asociado a uno o más elementos secundarios. Un elemento secundario es un nivel inferior y debe tener un elemento primario. Vea también **parent**, **child**.

**persist**

Para guardar datos en un estado permanente, como guardar un **objeto Recordset** en un archivo.

**bloqueo pesimista**

Un tipo de bloqueo en el que la página que contiene uno o varios registros, incluido el registro que se está editando, no está disponible para otros usuarios para asegurarse de que se realizará una actualización. El proveedor OLE DB define el comportamiento de bloqueo pesimista. Por lo general, los registros se bloquean al editar y permanecen sin estar disponibles hasta que se haya completado **el método Update.**

El bloqueo pesimista se habilita cuando se abre el objeto **Recordset** con el parámetro **LockType** o la propiedad establecido en **adLockPessimistic**. Vea también **bloqueo optimista**.

**agrupación**

Optimización del rendimiento basada en el uso de colecciones de recursos asignados previamente, como objetos o conexiones de base de datos. Es más eficaz dibujar un recurso existente del grupo que crear un nuevo recurso.

**ProgID (identificador de programación)**

Un nombre único asignado al registro Windows por una aplicación COM. El ProgID para una conexión de ADO es "ADODB. Conexión". Vea también **CLSID**, **COM**.

**proxy**

Un objeto específico de la interfaz que proporciona el cálculo de referencias de parámetros y la comunicación necesaria para que un cliente llame a un objeto de aplicación que se ejecuta en un entorno de ejecución diferente, como en un subproceso diferente o en otro proceso. El proxy se encuentra con el cliente y se comunica con un código auxiliar correspondiente que se encuentra con el objeto de aplicación al que se llama. Vea también **código auxiliar**.

Volver al principio

## <a name="r"></a>R

**dirección URL relativa**

Una dirección URL parcialmente cualificada que especifica un recurso en Internet o una intranet cuya ubicación es relativa a un punto inicial especificado por una dirección URL absoluta o un objeto Connection de ADO equivalente. En efecto, las direcciones URL absolutas y relativas concatenadas constituyen una dirección URL completa. Vea también **DIRECCIÓN URL** y dirección **URL absoluta.**

**origen de datos remoto**

Un origen de datos que existe en otro equipo, en lugar de en el sistema local (donde se ejecuta la aplicación cliente).

**registro de recursos**

Un registro de un proveedor de origen de documentos que contiene campos para la definición y descripción de una carpeta o documento. El documento en sí no está incluido en el registro de recursos, pero normalmente se puede obtener acceso a él mediante la secuencia predeterminada o un campo del registro de recursos que contiene una dirección URL. Vea también **proveedor de origen de documentos**, secuencia **predeterminada**, **DIRECCIÓN URL**.

**root**

Nivel superior de una estructura jerárquica de árbol. El nodo raíz no tiene padres, pero puede tener secundarios. Vea también **hierarchy**, **tree**, **parent**, **child**.

**conjunto de filas**

Un conjunto de filas de un origen de datos, todos con el mismo esquema de campo. Un conjunto de filas puede representar todos o algunos campos de una tabla. Un conjunto de filas también puede representar una tabla virtual, creada por una consulta o una combinación de dos o más tablas. En ADO, los conjuntos de filas se representan mediante **objetos Recordset.**

Volver al principio

## <a name="s"></a>S

**esquema**

Descripción de una base de datos en el sistema de administración de bases de datos (DBMS), que normalmente se genera mediante el lenguaje de definición de datos proporcionado por dbms. Un esquema define atributos de la base de datos, como tablas, columnas y propiedades.

**ámbito**

Intervalo de referencia para un objeto o variable o un intervalo de registros en una vista o tabla. Por ejemplo, solo se puede hacer referencia a variables locales dentro del procedimiento en el que se han definido. Las variables públicas son accesibles desde cualquier lugar de la aplicación. Los objetos, como la base de datos actual, están en el ámbito si están en la ruta de búsqueda definida. Los intervalos de registros se pueden especificar con una cláusula Scope en muchos comandos.

**proveedor de servicios**

Software que encapsula un servicio mediante la producción y el consumo de datos, el aumento de características en las aplicaciones de ADO. Es un proveedor que no expone datos directamente, sino que proporciona un servicio, como el procesamiento de consultas. El proveedor de servicios puede procesar los datos proporcionados por un proveedor de datos. Vea también proveedor **de datos**.

**conjunto de registros con forma**

Conjunto **de** registros cuyas columnas se han definido específicamente para contener no solo datos, sino también referencias (denominadas capítulos) a otros objetos **Recordset** o valores calculados basados en otros objetos **Recordset.**

**sibling**

Dos o más nodos de una estructura jerárquica que estén en el mismo nivel de la jerarquía. El nodo raíz de una jerarquía no tiene elementos relacionados.

**procedimiento almacenado**

Una colección precompilada de código, como instrucciones SQL y instrucciones de control de flujo opcionales almacenadas con un nombre y procesadas como una unidad. Los procedimientos almacenados se almacenan en una base de datos; se pueden ejecutar con una llamada desde una aplicación y permitir variables declaradas por el usuario, ejecución condicional y otras características de programación eficaces.

**stub**

Un objeto específico de la interfaz que proporciona el cálculo de referencias y la comunicación de parámetros necesarios para que un objeto de aplicación reciba llamadas de un cliente que se ejecuta en un entorno de ejecución diferente, como en un subproceso diferente o en otro proceso. El código auxiliar se encuentra con el objeto de aplicación y se comunica con un proxy correspondiente que se encuentra con el cliente que lo llama. Vea también **proxy**.

**subnúdes**

Vea **el elemento** secundario .

**operación sincrónica**

Una operación iniciada por código que se completa antes de que pueda iniciarse la siguiente operación. Vea también **operación asincrónica**.

Volver al principio

## <a name="t-w"></a>T-W

**árbol**

Estructura que representa una relación jerárquica entre elementos (nodos). Hay un nodo en el nivel superior de un árbol (la raíz). Debajo de la raíz, puede haber varios elementos secundarios. A su vez, cada elemento secundario puede ser el elemento primario de otros elementos secundarios, por lo que se bifurca como un árbol. Una carpeta que contiene documentos y otras carpetas es un ejemplo típico de una estructura de árbol. Vea también **hierarchy**, **node**, **root**, **child**, **parent**.

**DIRECCIÓN URL (localizador uniforme de recursos)**

Especifica la ubicación de un recurso que reside en Internet o una intranet. Una dirección URL completa consta de un esquema (como FTP, HTTP, mailto, archivo, entre otros), seguido de dos puntos, un nombre de servidor y la ruta de acceso completa de un recurso (como un documento, un gráfico u otro archivo). Algunos ejemplos de direcciones URL son:  
  
- https://www.domain.com/default.html  
- ftp://ftp.server.somewhere/ftp.file  
  
- ftp://ftp.server.somewhere/ftp.file  
- file://Server/Share/File.doc

Vea también **dirección URL absoluta** y dirección URL **relativa.**

**servidor web**

Un equipo que proporciona servicios web y páginas a usuarios de Intranet e Internet.



