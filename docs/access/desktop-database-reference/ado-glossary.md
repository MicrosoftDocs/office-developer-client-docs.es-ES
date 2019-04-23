---
title: Glosario de ActiveX Data Objects (ADO)
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

Una dirección URL completa que especifica la ubicación de un recurso que reside en Internet o en una intranet. Consulte también **URL** y **dirección URL relativa**.

**Control ActiveX**

El autoregistro, el componente COM en proceso que a menudo tiene un elemento visual, ya sea en tiempo de diseño o en tiempo de ejecución. Los controles ActiveX también tienen la capacidad de comunicarse con un contenedor de documentos activos, como Microsoft Internet Explorer.

**ADISAPI (interfaz de programación de aplicaciones de servidor de Internet Advanced Data)**

DLL ISAPI que proporciona análisis, control de automatización, cálculo de referencias de **Recordset** y empaquetado MIME. El componente ADISAPI funciona a través de la API proporcionada por Internet Information Services (IIS). Vea también **ISAPI**.

**función de agregado**

En una consulta, función como COUNT, AVG o STDEV que calcula un valor usando todas las filas de una columna de una tabla. En la escritura de expresiones y en programación, puede usar las funciones de agregado de SQL (incluidas las tres anteriores) y las funciones de agregado de dominio para determinar varias estadísticas.

**alias**

Un nombre alternativo que se da a una columna o expresión en una instrucción SELECT de SQL, a menudo menor o más significativo. Por ejemplo, BobSales es el alias de la siguiente instrucción SELECT: "Select WR sales as BobSales from SalesDB". Se puede usar un alias para asignar columnas dinámicamente a los enlaces de control en el objeto **DataControl** .

**subprocesamiento controlado**

Modelo de subprocesos COM en el que todas las llamadas a un objeto se producen en un subproceso. En el subprocesamiento controlado, COM sincroniza y convierte las llamadas. Vea también **com**.

**operación asincrónica**

Operación que devuelve el control al programa de llamada sin esperar a que se complete la operación. Antes de que se complete la operación, la ejecución de código sigue. Vea también **operación sincrónica**.

Volver al principio

## <a name="b"></a>B

**entrada de enlace**

Una asignación entre un campo de una tabla y una variable. En las extensiones de Visual C++ para ADO, los campos de **Recordset** se asignan a variables de C/c++.

**máscara**

Valor numérico pensado para una comparación de valor bit a bit con otros valores numéricos, normalmente para marcar opciones en parámetros o valores devueltos. Normalmente, esta comparación se realiza con operadores lógicos de bits, como **and** y **or** en Visual **&** Basic **|** y en C++.

Por ejemplo, los valores de FieldAttributeEnum (de ADO se pueden usar como máscaras de **** para determinar los atributos de un campo. SuPongamos que desea determinar si un campo se puede actualizar. Puede probar esto con la siguiente expresión en Visual Basic:  
  

Si el resultado es TRUE, el campo es actualizable.

**bookmark**

Un marcador que identifica de forma única una fila dentro de un conjunto de filas para que un usuario pueda desplazarse rápidamente a ella.

**objeto de negocios**

Un objeto que realiza un conjunto definido de operaciones, como validación de datos o lógica de regla de negocio. Los objetos de negocio suelen residir en el nivel intermedio.

**regla de negocio**

La combinación de las ediciones de validación, las comprobaciones de inicio de sesión, las búsquedas de base de datos, las directivas y las transformaciones algorítmicas que constituyen la forma de hacer negocios de una empresa. También se conoce como *lógica empresarial*.

Volver al principio

## <a name="c"></a>C

**expresión calculada**

Una expresión que no es constante, pero cuyo valor depende de otros valores. Para que se evalúe, una expresión calculada debe obtener y calcular valores de otros orígenes, normalmente en otros campos o filas.

**Capítulo**

Referencia a un rango de filas de un origen de datos. En ADO, un capítulo suele ser una referencia a otro **conjunto de registros**.

Las columnas de capítulo permiten definir una relación de *objeto primario-objeto secundario* donde el *objeto primario* es el objeto **Recordset** que contiene la columna de capítulo y el *objeto secundario* es el objeto **Recordset** representado por el capítulo.

**alias de capítulo**

Alias que hace referencia a la columna anexada al elemento principal.

**juego de caracteres**

Una asignación de un conjunto de caracteres a sus valores numéricos. Por ejemplo, Unicode es un juego de caracteres de 16 bits que puede codificar todos los caracteres conocidos y usarse como un estándar de codificación de caracteres en todo el mundo.

**hija**

Lado dependiente de una relación jerárquica. Un elemento secundario es un nodo de una estructura jerárquica que tiene otro nodo por encima de él (más cerca de la raíz). Vea también **alias de elemento secundario**, **principal-secundario**, **principal**.

**alias secundario**

Un alias que hace referencia a la secundaria. Consulte también **alias**, **secundario**.

**CLSID (identificador de clase)**

Identificador único universal (UUID) que identifica un componente COM. Cada componente COM tiene su CLSID en el registro de Windows para que se pueda cargar en otras aplicaciones. Vea también **ProgID**y **com**.

**nivel de cliente**

Capa lógica de un sistema distribuido que normalmente presenta datos y procesa las entradas del usuario, en ocasiones conocidas como Front- *End*. Normalmente, el nivel de cliente solicita datos de un servidor en función de las entradas y, a continuación, da formato y muestra el resultado. Vea también **nivel intermedio**, **nivel de origen de datos**, **aplicación distribuida**.

**COM (modelo de objetos de componentes)**

Un estándar binario que permite que los objetos interoperen en un entorno de red independientemente del idioma en el que se desarrollaron o de los equipos en los que residan. Las tecnologías basadas en COM incluyen controles ActiveX, automatización y vinculación e incrustación de objetos (OLE). COM permite a un objeto exponer su funcionalidad a otros componentes y hospedar aplicaciones. Define el modo en que el objeto se expone a sí mismo y cómo funciona esta exposición en los procesos y en las redes. COM también define el ciclo de vida del objeto.

**Componente COM**

Archivo binario, como. dll,. ocx y algunos archivos. exe, que admite el estándar COM para suministrar objetos. Un archivo de este tipo contiene código para una o varias fábricas de clases, clases COM, mecanismos de entrada del registro, código de carga, etc.

**operador de comparación**

Operador que compara dos expresiones y devuelve un valor booleano.

Un parámetro Criteria que se puede expresar como "\>" (mayor que), "\<" (menor que), "=" (igual), "\>=" (mayor o igual que), "\<=" (menor o igual que), "\<\>" (no es igual a) o "like" (coincidencia de patrón).

**component**

Un objeto que encapsula datos y código, y proporciona un conjunto bien especificado de servicios disponibles públicamente.

**archivo compuesto**

Una implementación del almacenamiento COM estructurado para los archivos. Un archivo compuesto almacena objetos independientes en un único archivo estructurado que consta de dos elementos principales: objetos de almacenamiento y objetos de secuencia. Juntos, funcionan como un sistema de archivos dentro de un archivo. Para obtener más información, consulte archivos compuestos en el SDK de la plataforma de Microsoft.

Una cantidad de archivos individuales enlazados juntos en un archivo físico. Se puede tener acceso a cada archivo individual de un archivo compuesto como si fuera un único archivo físico.

**constante**

Un valor numérico o de cadena que no cambia. Las enumeraciones de ADO con nombre (constantes enumeradas) se pueden usar en el código en lugar de valores reales; por ejemplo, **adUseClient** es una constante cuyo valor es 3. (Const adUseClient = 3). Vea también **enumeración**.

**cursor**

Un elemento de base de datos que controla la navegación por los registros, la actualización de los datos y la visibilidad de los cambios realizados en la base de datos por otros usuarios.

Volver al principio

## <a name="d"></a>D

**enlace de datos**

El proceso de asociar los objetos o controles de una aplicación a un origen de datos. Un control asociado a un origen de datos se denomina *control enlazado a datos*.

El contenido de un control enlazado a datos está asociado a valores de una base de datos. Por ejemplo, un control de cuadrícula enlazado a un objeto **Recordset** se puede actualizar cuando se actualizan las filas del objeto **Recordset** . Cuando se recuperan nuevos valores mediante el **objeto Recordset**, se muestran nuevos valores en la cuadrícula.

**proveedor de datos**

Software que expone datos a una aplicación de ADO, ya sea directamente o a través de un proveedor de servicios. Vea también **proveedor de servicios**.

**forma de datos**

Técnica que hace uso de una sintaxis formalizada (denominada **lenguaje de forma**) para definir un objeto de **conjunto de registros** especializado (denominado **Recordset con forma**) que no solo contiene datos, sino también referencias a otros objetos **Recordset** y valores calculados basados en estos otros objetos **Recordset** .

**nivel de origen de datos**

Capa lógica de un sistema distribuido que representa un equipo que ejecuta un DBMS, como una base de datos de SQL Server. Vea también **nivel de cliente**, **nivel intermedio**, **aplicación distribuida**.

**DCOM**

Protocolo de conexión que permite a los componentes COM comunicarse directamente entre sí a través de una red. Vea también **com**, **componente**.

**DDL (lenguaje de definición de datos)**

Las instrucciones de SQL que definen, a diferencia de la manipulación, los datos. El esquema de una base de datos se crea o se modifica con DDL. Por ejemplo, **CREATE TABLE**, **Create index**, **Grant**y **REVOKE** son instrucciones de DDL de SQL.

**secuencia predeterminada**

Una secuencia binaria o de texto (representada por un objeto **Stream** ) que está asociada con los objetos **Record** o **Recordset** cuando se usan determinados proveedores OLE DB, como Microsoft OLE DB Provider for Internet Publishing. Normalmente, la secuencia predeterminada incluye el contenido de un archivo, como el código HTML para la raíz de un sitio Web.

**aplicación distribuida**

Programa escrito para que el procesamiento se pueda dividir en varios equipos a través de una red. Normalmente, una aplicación distribuida se divide en presentación, lógica empresarial, capas del almacén de datos o *niveles*. Vea también nivel de **cliente**, nivel **intermedio**, **nivel de origen de datos**.

**Objeto Recordset desconectado**

Un objeto **Recordset** en una memoria caché de cliente que ya no tiene una conexión activa con el servidor. Si es necesario volver a obtener acceso al origen de datos original por algún motivo, como la actualización de datos, se debe volver a establecer la conexión. Sin embargo, todavía se puede tener acceso a las colecciones, las propiedades y los métodos de un **objeto Recordset** desconectado.

**DLL (biblioteca de vínculos dinámicos)**

Un archivo que contiene una o más funciones que se compilan, vinculan y almacenan por separado de los procesos que los usan. El sistema operativo asigna los archivos dll en el espacio de direcciones del proceso de llamada cuando el proceso se inicia o mientras se ejecuta.

**DML (lenguaje de manipulación de datos)**

Las instrucciones de SQL que manipulan, en lugar de definir los datos. Los valores de una base de datos se seleccionan y modifican con DML. Por ejemplo, **Insert**, **Update**, **Delete**y **Select** son instrucciones DML de SQL.

**proveedor de orígenes de documentos**

Una clase especial de proveedores que administran carpetas y documentos. Cuando un documento está representado por un objeto **Record** , o una carpeta de documentos se representa mediante un objeto **Recordset** , el proveedor de orígenes de documentos rellena dichos objetos con un conjunto único de campos que describen las características del documento. en lugar del propio documento real. Consulte también **registro de recursos**.

**DSN (nombre de origen de datos)**

Colección de información que se usa para conectar la aplicación a una base de datos ODBC en particular. El administrador de controladores ODBC usa esta información para crear una conexión a la base de datos. Un DSN se puede almacenar en un archivo (DSN de archivo) o en el registro de Windows (un DSN de equipo).

**propiedad Dynamic**

Una propiedad específica de un proveedor de datos o el servicio de cursores. La colección **Properties** de un objeto se rellena automáticamente ("dinámicamente"). Un objeto no tiene propiedades dinámicas hasta que se conecta a un origen de datos a través de un proveedor de datos determinado. Vea también **proveedor de datos**, **cursor**.

Volver al principio

## <a name="e-i"></a>E-I

**las**

Una lista de constantes con nombre. Los valores enumerados no tienen que ser únicos. Sin embargo, el nombre de cada valor debe ser único dentro del ámbito en el que se define la enumeración. En ADO, las enumeraciones se utilizan para parámetros numéricos y valores devueltos, para agregar significado al código ADO y para proteger al desarrollador de los valores numéricos (que pueden cambiar de una versión a una). Por ejemplo, para abrir un **objeto Recordset**estático, use el valor enumerado **adOpenStatic** :  
  

También se conoce como *constante enumerada*. Vea también **constante**.

**evento**

Una acción reconocida por un objeto para el que se puede escribir código para responder. Los eventos se pueden generar mediante la ejecución de comandos, la finalización de transacciones, la navegación de Recordset y las actualizaciones de datos, entre otras acciones. Vea también **controlador de eventos**.

**controlador de eventos**

Un controlador de eventos es el código que se ejecuta cuando se produce un evento. Vea también **evento**.

**handler**

Rutina que administra una condición u operación común y relativamente sencilla, como la recuperación de errores o la administración de datos.

**Recordset jerárquico**

Un **objeto Recordset** que contiene otro **objeto Recordset**. Vea también forma de **datos**, **capítulo**.

Para obtener más información, vea [obtener acceso a filas en un objeto Recordset jerárquico](accessing-rows-in-a-hierarchical-recordset.md) .

**jerárquico**

En general, una jerarquía es una estructura clasificada con un nivel superior y los niveles subordinados. En ADO, los **conjuntos de registros** jerárquicos se usan para representar la relación principal-secundario entre un registro y un capítulo. También en ADO, los objetos **Record** y **Stream** se pueden usar para tener acceso a estructuras jerárquicas de árbol como una carpeta y documentos. ADO MD también incluye objetos **Hierarchy** para representar una relación entre los niveles de una dimensión en un cubo OLAP. Vea también **conjuntos de registros jerárquicos**, **relación principal-secundario**, **capítulo**, **árbol**.

**ISAPI (interfaz de programación de aplicaciones de servidor de Internet)**

Un conjunto de funciones para servidores de Internet, como un servidor Windows NT Server/Windows 2000 que ejecuta Microsoft Internet Information Services (IIS).

Volver al principio

## <a name="k-m"></a>K-M

**key**

Columna o columnas de una tabla que identifican de forma única una fila; se suele usar para indizar una tabla.

**serialización**

Proceso de empaquetar, enviar y desempaquetar los parámetros del método de la interfaz entre los límites del proceso o subproceso.

**nivel intermedio**

La capa lógica en un sistema distribuido entre una interfaz de usuario o un cliente web y la base de datos. Suele ser donde se crean instancias de los objetos de negocio. El nivel intermedio es una colección de reglas y funciones de negocio que genera y opera cuando recibe información. Lo hacen a través de reglas de negocio, que pueden cambiar con frecuencia y se encapsulan en componentes separados físicamente de la lógica de la aplicación. También se conoce como *nivel del servidor de aplicaciones*. Vea también **aplicación distribuida**, **nivel de cliente**y nivel de **origen de datos**.

**MIME (extensión multipropósito de correo Internet)**

Protocolo de Internet desarrollado originalmente para permitir el intercambio de mensajes de correo electrónico con contenido enriquecido en entornos heterogéneos de red, equipo y correo electrónico. En la práctica, MIME también ha sido adoptado y ampliado por aplicaciones que no son de correo.

MIME es un estándar que permite que los datos binarios se publiquen y lean en Internet. El encabezado de un archivo con datos binarios contiene el tipo MIME de los datos; de este modo, se informa a los programas cliente (por ejemplo, los exploradores Web y los paquetes de correo) de que deben controlar los datos de una forma diferente a la que controlan el texto directo. Por ejemplo, el encabezado de un documento Web que contiene un gráfico JPEG contiene el tipo MIME específico del formato de archivo JPEG. Esto permite que un explorador muestre el archivo con su visor JPEG, si hay alguno presente.

Volver al principio

## <a name="n-o"></a>N-O

**nodos**

Un elemento en una estructura de árbol jerárquica. Un nodo puede ser la raíz o el elemento secundario de otro nodo. Un nodo también puede ser el primario de varios elementos secundarios. Vea también **jerarquía**, **árbol**, **raíz**, **secundario**, **principal**.

**variable de objeto**

Variable que contiene una referencia a un objeto. Por ejemplo, objCustomObject es una variable que apunta a un objeto de tipo CustomObject:  
  
es una variable que apunta a un objeto de tipo CustomObject:  
  
Set objCustomObject = CreateObject (ADODB. Registros

**ODBC (Conectividad abierta de bases de datos)**

Una interfaz de lenguaje de programación estándar que se usa para conectarse a varios orígenes de datos. Suele tener acceso a a través del panel de control, donde se pueden asignar nombres de origen de datos (DSN) para usar controladores ODBC específicos.

**OLE DB**.

Un conjunto de interfaces que exponen datos de una gran variedad de orígenes mediante COM. Las interfaces OLE DB proporcionan a las aplicaciones un acceso uniforme a los datos almacenados en diversos orígenes de información. Estas interfaces admiten la cantidad de funciones de DBMS apropiadas para el origen de datos, lo que permite que comparta sus datos. Vea también **com**.

**bloqueo optimista**

Un tipo de bloqueo en el que la página de datos que contiene uno o varios registros, incluido el registro que se está editando, no está disponible para otros usuarios mientras el registro se actualiza mediante el método **Update** , pero está disponible antes y después de la llamada a **Update** . .

El bloqueo optimista se utiliza cuando el objeto **Recordset** se abre con el parámetro o la propiedad **LockType** establecidos en **adLockOptimistic** o **adLockBatchOptimistic**. Vea también **bloqueo pesimista**.

**valor ordinal**

La ubicación numérica de un elemento dentro de un pedido. En una colección de ADO, el valor ordinal del primer elemento es cero (0). El siguiente elemento es uno (1) y así sucesivamente.

Volver al principio

## <a name="p"></a>P

**comando parametrizado**

Una consulta o un comando que permite establecer los valores de los parámetros antes de que se ejecute el comando. Por ejemplo, se puede parametrizar una cadena SQL incrustando marcadores de parámetros en la cadena SQL (designados mediante el carácter '? '). A continuación, la aplicación especifica los valores de cada parámetro y ejecuta el comando.

**origen**

El lado de control de una relación jerárquica. En una estructura jerárquica, un elemento primario tiene uno o más nodos secundarios directamente debajo de él en la jerarquía. Vea también **alias primario**, **principal-secundario, relación** **secundaria**.

**alias primario**

Alias que hace referencia al elemento primario. Consulte también **alias**, **principal**.

**relación de elementos principales y secundarios**

Una relación en una estructura jerárquica en la que el elemento principal es un nivel superior y asociado directamente con uno o más elementos secundarios. Un elemento secundario es un nivel inferior y debe tener un elemento primario. Vea también **principal**y **secundario**.

**mantener**

Para guardar los datos en un estado permanente, como guardar un **objeto Recordset** en un archivo.

**bloqueo pesimista**

Un tipo de bloqueo en el que la página que contiene uno o más registros, incluido el registro que se está editando, no está disponible para otros usuarios para asegurarse de que se va a realizar una actualización. El proveedor OLE DB define el comportamiento de bloqueo pesimista. Normalmente, los registros se bloquean tras la edición y permanecen no disponibles hasta que el método **Update** haya finalizado.

El bloqueo pesimista está habilitado cuando el objeto **Recordset** se abre con el parámetro o la propiedad **LockType** establecidos en **adLockPessimistic**. Consulte también **bloqueo optimista**.

**agrupación**

Optimización del rendimiento basada en el uso de colecciones de recursos preasignados, como objetos o conexiones de base de datos. Es más eficaz dibujar un recurso existente del grupo que crear un nuevo recurso.

**Identificador de programa (ProgID)**

Un nombre único asignado al registro de Windows mediante una aplicación COM. El ProgID para una conexión ADO es "ADODB. Conexión ". Vea también **CLSID**, **com**.

**proxy**

Objeto específico de una interfaz que proporciona el cálculo de referencias de parámetros y la comunicación necesaria para que un cliente llame a un objeto de aplicación que se está ejecutando en un entorno de ejecución diferente, como en un subproceso diferente o en otro proceso. El proxy se encuentra con el cliente y se comunica con un código auxiliar correspondiente que se encuentra en el objeto Application al que se llama. Consulte también **código auxiliar**.

Volver al principio

## <a name="r"></a>R

**Dirección URL relativa**

Una dirección URL parcialmente calificada que especifica un recurso en Internet o una intranet cuya ubicación es relativa a un punto de inicio especificado por una dirección URL absoluta o un objeto Connection de ADO equivalente. De hecho, las direcciones URL absolutas y relativas concatenadas consitute una dirección URL completa. Consulte también **dirección URL** y **dirección URL absoluta**.

**origen de datos remoto**

Origen de datos que existe en otro equipo, en lugar de en el sistema local (donde se ejecuta la aplicación cliente).

**registro de recursos**

Un registro de un proveedor de orígenes de documentos que contiene campos para la definición y la descripción de una carpeta o un documento. El documento en sí no está incluido en el registro de recursos, pero normalmente se puede tener acceso a él mediante una secuencia predeterminada o un campo en el registro de recursos que contiene una dirección URL. Vea también **proveedor de origen de documentos**, **secuencia predeterminada**, **dirección URL**.

**root**

Nivel superior de una estructura jerárquica en árbol. El nodo raíz no tiene elementos primarios, pero puede tener elementos secundarios. Vea también **jerarquía**, **árbol**, **principal**, **secundario**.

**RowSet**

Un conjunto de filas de un origen de datos que tienen el mismo esquema de campo. Un conjunto de filas puede representar todos o algunos de los campos de una tabla. Un conjunto de filas también puede representar una tabla virtual, creada por una consulta o una combinación de dos o más tablas. En ADO, los conjuntos de filas se representan mediante objetos **Recordset** .

Volver al principio

## <a name="s"></a>S

**esquema**

Una descripción de una base de datos para el sistema de administración de bases de datos (DBMS), normalmente generada con el lenguaje de definición de datos proporcionado por el DBMS. Un esquema define los atributos de la base de datos, como tablas, columnas y propiedades.

**scope**

El rango de referencia para un objeto o una variable o un rango de registros de una vista o tabla. Por ejemplo, se puede hacer referencia a variables locales solo dentro del procedimiento en el que se definieron. Las variables públicas son accesibles desde cualquier lugar de la aplicación. Los objetos, como la base de datos activa, están en el ámbito si están en la ruta de búsqueda definida. Los intervalos de registros se pueden especificar con una cláusula Scope en muchos comandos.

**proveedor de servicios**

Software que encapsula un servicio mediante la generación y el consumo de datos, que aumenta las características de las aplicaciones de ADO. Se trata de un proveedor que no expone datos directamente, sino que proporciona un servicio, como procesamiento de consultas. El proveedor de servicios puede procesar los datos proporcionados por un proveedor de datos. Vea también **proveedor de datos**.

**Recordset con forma**

Un **objeto Recordset** cuyas columnas se han definido específicamente para que contengan no solo datos, sino también referencias (denominadas capítulos) a otros objetos **Recordset** o valores calculados basados en otros objetos **Recordset** .

**elemento**

Dos o más nodos de una estructura jerárquica que se encuentran en el mismo nivel de la jerarquía. El nodo raíz de una jerarquía no tiene elementos del mismo nivel.

**procedimiento almacenado**

Una colección precompilada de código, como instrucciones SQL e instrucciones opcionales de control de flujo, almacenada con un nombre y procesada como una unidad. Los procedimientos almacenados se almacenan en una base de datos; se pueden ejecutar con una llamada desde una aplicación y permitir las variables declaradas por el usuario, la ejecución condicional y otras características de programación eficaces.

**desprendible**

Objeto específico de una interfaz que proporciona el cálculo de referencias de parámetros y la comunicación necesaria para que un objeto de aplicación reciba llamadas de un cliente que se ejecuta en un entorno de ejecución diferente, como en un subproceso diferente o en otro proceso. El código auxiliar se encuentra en el objeto Application y se comunica con un proxy correspondiente que se encuentra en el cliente que lo llama. Consulte también **proxy**.

**nodo secundario**

Consulte **Child**.

**operación sincrónica**

Una operación iniciada por código que finaliza antes de que se inicie la siguiente operación. Vea también **operaciones asincrónicas**.

Volver al principio

## <a name="t-w"></a>T-W

**árboles**

Estructura que representa una relación jerárquica entre elementos (nodos). Hay un nodo en el nivel superior de un árbol (la raíz). Debajo de la raíz, puede haber varios elementos secundarios. Cada elemento secundario puede ser, a su vez, el elemento principal de otros secundarios, de modo que se ramifica como un árbol. Una carpeta que contiene documentos y otras carpetas es un ejemplo típico de una estructura de árbol. Vea también **jerarquía**, **nodo**, **raíz**, **secundario**, **principal**.

**Dirección URL (localizador uniforme de recursos)**

Especifica la ubicación de un recurso que reside en Internet o en una intranet. Una dirección URL completa consta de un esquema (como FTP, HTTP, mailto, archivo, etc.), seguido de dos puntos, un nombre de servidor y la ruta de acceso completa de un recurso (por ejemplo, un documento, un gráfico u otro archivo). Algunos ejemplos de direcciones URL son:  
  
- https://www.domain.com/default.html  
- FTP://ftp.Server.Somewhere/FTP.File  
  
- FTP://ftp.Server.Somewhere/FTP.File  
- file://Server/Share/File.doc

Vea también **dirección URL absoluta** y **dirección URL relativa**.

**servidor Web**

Un equipo que proporciona páginas y servicios web a los usuarios de la intranet y de Internet.



