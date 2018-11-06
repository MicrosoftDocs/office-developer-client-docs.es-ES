---
title: Glosario de ActiveX Data Objects (ADO)
TOCTitle: ADO Glossary
ms:assetid: 40f00876-7525-4117-8f57-f3d87c54be99
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249184(v=office.15)
ms:contentKeyID: 48544438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9b9fd656aeda727cc829ab47ea4cb9fab8f2a169
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997794"
---
# <a name="ado-glossary"></a>Glosario de ADO

**Se aplica a**: Access 2013, Office 2013

## <a name="a"></a>A

**dirección URL absoluta**

Una dirección URL completa que especifica la ubicación de un recurso que reside en Internet o en una intranet. Vea también **URL** y la **dirección URL relativa**.

**Control ActiveX**

Registra automáticamente, en proceso componente COM que a menudo tiene un elemento visual en tiempo de diseño o tiempo de ejecución. Los controles ActiveX también tienen la capacidad de comunicarse con un contenedor de documentos activos, como Microsoft Internet Explorer.

**ADISAPI (avanzado datos Internet Server Application Programming Interface)**

Una DLL de ISAPI que proporciona funciones de análisis, control de automatización, el cálculo de referencias de **objeto Recordset** y empaquetamiento MIME. El componente ADISAPI funciona a través de la API proporcionada por Internet Information Services (IIS). Vea también **ISAPI**.

**función de agregado**

En una consulta, una función como COUNT, AVG o STDEV que calcula un valor con todas las filas de una columna de una tabla. En la escritura de expresiones y en la programación, puede usar las funciones de agregado de SQL (incluidas las tres anteriores) y funciones de agregado de dominio para determinar varias estadísticas.

**alias**

Un nombre alternativo que se asigna una columna o expresión en una instrucción SELECT de SQL, a menudo más corta o más significativa. Por ejemplo, VentasPilar es un alias en la siguiente instrucción SELECT: "Select ventas-wr as VentasPilar from BDVentas". Un alias se puede usar para asignar columnas dinámicamente a enlaces de controles sobre el objeto **DataControl** .

**subprocesamiento de apartamento**

Un modelo de subprocesamiento COM donde todas las llamadas a un objeto se producen en un subproceso. En el subprocesamiento de apartamento, COM sincroniza y calcula las referencias de las llamadas. Vea también **COM**.

**operación asincrónica**

Una operación que devuelve el control al programa de llamada sin tener que esperar a que finalice la operación. Antes de que la operación se completa, continúa la ejecución de código. Vea también la **operación sincrónica**.

Volver arriba

## <a name="b"></a>B

**entrada de enlace**

Una asignación entre un campo de una tabla y una variable. En las extensiones de Visual C++ de ADO, se asignan campos de **Recordset** a las variables de C/C ++.

**máscara de bits**

Un valor numérico destinado a una comparación bit a bit con otros valores numéricos, normalmente para detectar opciones en parámetros o valores devueltos. Esta comparación se suele realizar mediante operadores lógicos bit a bit, como **y** y **o** en Visual Basic, **&** y **|** en C++.

Por ejemplo, los valores **FieldAttributeEnum** de ADO se pueden usar como máscaras de bits para determinar los atributos de un campo. Suponga que desea determinar si un campo es actualizable. Puede probar con la siguiente expresión en Visual Basic:  
  

Si el resultado es TRUE, el campo es actualizable.

**bookmark**

Un marcador que identifica de forma exclusiva una fila dentro de un conjunto de filas para que un usuario puede navegar rápidamente a ella.

**objeto de negocios**

Un objeto que realiza un conjunto definido de operaciones, como la lógica de datos profesionales o de validación de la regla. Normalmente, los objetos de negocios residen en el nivel intermedio.

**regla de negocio**

La combinación de ediciones de validación, comprobaciones de inicio de sesión, las búsquedas de la base de datos, directivas y transformaciones algorítmicas que constituyen la forma de una empresa de hacer negocios. También se conoce como *lógica de negocios*.

Volver arriba

## <a name="c"></a>C

**expresión calculada**

Una expresión que no es constante, pero cuyo valor depende de otros valores. Para evaluar, una expresión calculada debe obtener y calcular valores de otros orígenes, normalmente en otros campos o filas.

**capítulo**

Una referencia a un rango de filas de un origen de datos. En ADO, un capítulo suele ser una referencia a otro **conjunto de registros**.

Columnas de capítulo permiten definir una relación de *elementos primarios y secundarios* donde el objeto *primario* es el **objeto Recordset** que contiene la columna de capítulo y el *elemento secundario* es el **objeto Recordset** representado por el capítulo.

**alias de capítulo**

Un alias que hace referencia a la columna anexada al elemento principal.

**juego de caracteres**

Una asignación de un conjunto de caracteres a sus valores numéricos. Por ejemplo, Unicode es un carácter de 16 bits establecer capaz de codificar todos los caracteres conocidos y usa como un estándar de codificación de caracteres en todo el mundo.

**secundarios**

La parte dependiente de una relación jerárquica. Un elemento secundario es un nodo en una estructura jerárquica que tiene otro nodo por encima de él (más cerca de la raíz). Vea también **alias de elemento secundario**, la **relación de elementos primarios y secundarios**, **primario**.

**alias secundario**

Un alias que hace referencia al elemento secundario. Vea también **alias**, **secundarios**.

**CLSID (identificador de clase)**

Identificador único universal (UUID) que identifica un componente COM. Cada componente COM tiene su CLSID en el registro de Windows que se puede cargar por otras aplicaciones. Vea también **ProgID**, **COM**.

**nivel del cliente**

Una capa lógica de un sistema distribuido que normalmente presenta datos a y procesa la entrada del usuario, a veces se denomina el *front-end*. Normalmente, el nivel de cliente solicita datos de un servidor basado en la entrada y, a continuación, se da formato y muestra el resultado. Vea también **nivel intermedio**, **nivel de origen de datos**y **aplicación distribuida**.

**COM (modelo de objetos componentes)**

Un estándar binario que permite a los objetos interoperar en un entorno de red independientemente del idioma en el que se desarrollaron o en los equipos que se encuentren. Tecnologías basadas en COM incluyen los controles ActiveX, automatización y vinculación e incrustación de objetos (OLE). COM permite a un objeto exponer su funcionalidad a otros componentes y aplicaciones host. Define cómo se expone el objeto y cómo funciona esa exposición entre distintos procesos y redes. COM también define el ciclo de vida del objeto.

**Componente COM**

Archivo binario — como .dll, .ocx y algunos archivos .exe, que es compatible con el estándar de COM para proporcionar objetos. Este archivo contiene código para uno o varios generadores de clases, clases COM, mecanismos de entrada del registro, código de carga y así sucesivamente.

**operador de comparación**

Un operador que compara dos expresiones y devuelve un valor Boolean.

Un parámetro de criterios que se puede expresar como "\>"(mayor que),"\<"(menor que), "=" (igual a),"\>=" (mayor o igual que), "\<=" (menor o igual que), "\<\>" (no igual a), o "like" (coincidencia de modelos).

**componente**

Un objeto que encapsula datos y código y proporciona un conjunto bien especificado de servicios públicamente disponibles.

**archivo compuesto**

Una implementación de COM había estructurado de almacenamiento para los archivos. Un archivo compuesto almacena objetos independientes en un único archivo estructurado formado por dos elementos principales: objetos de almacenamiento y objetos stream. Ambos funcionan conjuntamente como un sistema de archivos dentro de un archivo. Para obtener más información, vea archivos compuestos en Microsoft Platform SDK.

Un número de archivos individuales enlazados conjuntamente en un único archivo físico. Puede tener acceso cada archivo individual en un archivo compuesto como si fuese un único archivo físico.

**constante**

Un valor numérico o de cadena que no cambia. Enumeraciones de ADO con nombre (constantes enumeradas) se pueden usar en el código en lugar de los valores reales, por ejemplo, **adUseClient** es una constante cuyo valor es 3. (Const adUseClient = 3). Vea también **(enumeración)**.

**cursor**

Un elemento de base de datos que controla la exploración de registros, actualización de los datos y la visibilidad de los cambios realizados en la base de datos por otros usuarios.

Volver arriba

## <a name="d"></a>D

**enlace de datos**

El proceso de asociar los objetos o controles de una aplicación para un origen de datos. Un control asociado con un origen de datos se denomina un *control enlazado a datos*.

El contenido de un control enlazado a datos se asocian con los valores de una base de datos. Por ejemplo, un control de cuadrícula está enlazado a un objeto **Recordset** puede actualizarse cuando se actualizan las filas en el **conjunto de registros** . Cuando el **objeto Recordset**se recuperan nuevos valores, nuevos valores se muestran en la cuadrícula.

**proveedor de datos**

Software que expone los datos a una aplicación ADO directamente o a través de un proveedor de servicios. Vea también **proveedor de servicios**.

**forma de datos**

Una técnica que utiliza una sintaxis formalizada (denominada **Lenguaje Shape**) para definir un objeto **Recordset** especializado (denominado un **objeto Recordset con forma**) que contiene no sólo datos, sino también referencias a otros objetos **Recordset** y y/o valores calculados basados en esos otros objetos **Recordset** .

**nivel de origen de datos**

Una capa lógica de un sistema distribuido que representa un equipo que ejecuta un DBMS, como una base de datos de SQL Server. Vea también **nivel de cliente**, **nivel intermedio**y **aplicación distribuida**.

**DCOM**

Un protocolo que permite a los componentes COM comunicarse directamente con cada una de las demás a través de una red. Vea también **COM**y **componente**.

**DDL (lenguaje de definición de datos)**

Las instrucciones en SQL que definen, en contraposición a manipular datos. El esquema de una base de datos se crea o modifica con DDL. Por ejemplo, **CREATE TABLE**, **CREATE INDEX**, **GRANT**y **REVOKE** son instrucciones DDL de SQL.

**secuencia predeterminada**

Un texto o secuencia binaria (representado por un objeto **Stream** ) que está asociada con los objetos **Record** o **Recordset** cuando se utilizan ciertos proveedores OLE DB, como Microsoft OLE DB Provider for Internet Publishing. Normalmente, la secuencia predeterminada contiene el contenido de un archivo como el código HTML para la raíz de un sitio Web.

**aplicación distribuida**

Un programa escrito de modo que el procesamiento se puede dividir en varios equipos a través de una red. Normalmente, una aplicación distribuida se divide en presentación, lógica de negocios y capas de almacén de datos o *niveles*. Vea también **nivel de cliente**, **nivel intermedio**y **nivel de origen de datos**.

**conjunto de registros desconectado**

Un objeto **Recordset** en una memoria caché de cliente que ya no tiene una conexión activa con el servidor. Si el origen de datos original debe obtenerse acceso nuevo por algún motivo, como la actualización de datos, se debe restablecer la conexión. Sin embargo, aún se pueden tener acceso a las colecciones, propiedades y métodos de un **objeto Recordset** de desconectado.

**DLL (biblioteca de vínculos dinámicos)**

Un archivo que contiene una o más funciones que se compilan, vinculado y almacenan por separado de los procesos que las utilizan. El sistema operativo asigna los archivos DLL en el espacio de direcciones del proceso de llamada cuando se inicia el proceso, o mientras se está ejecutando.

**DML (lenguaje de manipulación de datos)**

Las instrucciones en SQL que manipulan, en lugar de definir, datos. Los valores en una base de datos son seleccionados y modificados con DML. Por ejemplo, **Insertar**, **Actualizar**, **Eliminar**y **Seleccione** son instrucciones DML SQL.

**proveedor de origen de documentos**

Una clase especial de proveedores que administran carpetas y documentos. Cuando un documento está representado por un objeto **Record** , o una carpeta de documentos está representada por un objeto **Recordset** , el proveedor de origen de documentos rellena esos objetos con un conjunto único de campos que describen las características del documento, en lugar del real propio documento. Consulte también **registro de recursos**.

**DSN (nombre de origen de datos)**

La recopilación de información que se usa para conectar la aplicación a una base de datos ODBC determinada. El Administrador de controladores ODBC utiliza esta información para crear una conexión a la base de datos. Un DSN puede almacenarse en un archivo (DSN de archivo) o en el registro de Windows (DSN de equipo).

**propiedad dinámica**

Una propiedad específica de un proveedor de datos o el servicio de cursores. La colección **Properties** de un objeto se rellena automáticamente con estos ("dinámicamente"). Un objeto no tiene propiedades dinámicas hasta que se conecta a un origen de datos a través de un proveedor de datos en particular. Vea también **proveedor de datos**, **cursor**.

Volver arriba

## <a name="e-i"></a>E-I

**(enumeración)**

Una lista de constantes con nombre. Los valores enumerados no deben ser únicos. Sin embargo, el nombre de cada valor debe ser único dentro del ámbito donde se define la enumeración. En ADO, las enumeraciones se utilizan para parámetros numéricos y valores devuelven, para agregar significado al código de ADO y para proteger al programador de los valores numéricos (que pueden cambiar de una versión a otra). Por ejemplo, para abrir un **objeto Recordset**de estático, utilice el valor **adOpenStatic** enumeradas:  
  

Se conoce también como *constante enumerada*. Vea también **constante**.

**event**

Una acción reconocida por un objeto, para los que puede escribir código para responder. Los eventos se pueden generar mediante la ejecución de comandos, finalización de transacciones, navegación de conjunto de registros y las actualizaciones de datos, entre otras acciones. Vea también el **controlador de eventos**.

**controlador de eventos**

Un controlador de eventos es el código que se ejecuta cuando se produce un evento. Vea también el **evento**.

**handler**

Una rutina que administra una operación, como la administración de recuperación o datos de error o condición común y relativamente simple.

**objeto Recordset jerárquico**

Un **objeto Recordset** que contiene otro **objeto Recordset**. Vea también **forma de datos**, **capítulo**.

Para obtener más información, vea [Obtener acceso a filas de un Recordset jerárquico](accessing-rows-in-a-hierarchical-recordset.md)

**jerarquía**

En general, una jerarquía es una estructura clasificada con una parte superior de nivel y niveles subordinados. En ADO, los **conjuntos de registros** jerárquicos se utilizan para representar la relación de elementos primarios y secundarios entre un registro y un capítulo. También en ADO, los objetos **Record** y **Stream** se pueden usar para tener acceso a estructuras jerárquicas en árbol, como una carpeta y documentos. ADO MD también incluye objetos **Hierarchy** para representar una relación entre los niveles de una dimensión en un cubo OLAP. Vea también **conjuntos de registros jerárquicos**, **relación de elementos primarios y secundarios**, **capítulo**y **árbol**.

**ISAPI (interfaz de programación de aplicaciones de servidor de Internet)**

Un conjunto de funciones para servidores de Internet, como un servidor de Windows NT Server o Windows 2000 que ejecuta Microsoft Internet Information Services (IIS).

Volver arriba

## <a name="k-m"></a>K-M

**clave**

Una columna o columnas de una tabla que identifican una fila; a menudo se utiliza para indizar una tabla.

**el cálculo de referencias**

El proceso de empaquetado, envío y desempaquetado de parámetros de método de interfaz a través de límites de subproceso o proceso.

**nivel intermedio**

La capa lógica de un sistema distribuido entre un cliente de web o de interfaz de usuario y la base de datos. Normalmente, esto es donde se crean instancias de objetos de negocios. El nivel intermedio es una colección de reglas de negocio y las funciones que se generan y actúan tras recibir la información. Para ello a través de reglas de negocio, que pueden cambiar con frecuencia y, por tanto, se encapsulan en componentes físicamente independientes de la lógica de la aplicación. También se conoce como *nivel de servidor de aplicaciones*. Vea también **aplicación distribuida**, el **nivel del cliente**, el **nivel de origen de datos**.

**MIME (extensión de correo de Internet de varios propósitos)**

Un protocolo de Internet desarrollado originalmente para permitir el intercambio de mensajes de correo electrónico con contenido enriquecido entre la red heterogénea, equipo y entornos de correo electrónico. En la práctica, MIME tiene también se han adoptado y extendido por las aplicaciones que no sean de correo.

MIME es un estándar que permite que los datos binarios poder publicar y leer en Internet. El encabezado de un archivo con datos binarios contiene el tipo MIME de los datos; así se informa a los programas cliente (exploradores web y paquetes de correo, por ejemplo) que se necesitan administrar los datos de una manera diferente lo hacen con texto recta. Por ejemplo, el encabezado de un documento web que contiene un gráfico JPEG contiene el tipo MIME específico para el formato de archivo JPEG. Esto permite a un explorador mostrar el archivo con su visor JPEG, si hay alguno.

Volver arriba

## <a name="n-o"></a>N O

**nodo**

Un elemento en una estructura de árbol jerárquica. Puede ser un nodo de la raíz o el elemento secundario de otro nodo. Un nodo también puede ser el elemento principal de varios elementos secundarios. Vea también **jerarquía**, **árbol**, **raíz**, **secundario**, **primario**.

**variable de objeto**

Variable que contiene una referencia a un objeto. Por ejemplo, objCustomObject es una variable que apunta a un objeto de tipo CustomObject:  
  
es una variable que apunta a un objeto de tipo CustomObject:  
  
Establecer objCustomObject = CreateObject (adodb. Conjunto de registros)

**ODBC (conectividad de base de datos abierta)**

Interfaz estándar de programación idioma usada para conectarse a una variedad de orígenes de datos. Normalmente, esto se tiene acceso a través del Panel de Control, donde se pueden asignar nombres de origen de datos (DSN) a usar controladores ODBC específicos.

**OLE DB**

Un conjunto de interfaces que exponen datos de una serie de orígenes mediante COM. Interfaces de OLE DB proporcionan aplicaciones con acceso uniforme a los datos almacenados en diversos orígenes de información. Estas interfaces admiten la cantidad de funcionalidad DBMS adecuada para el origen de datos, lo que permite compartir sus datos. Vea también **COM**.

**bloqueo optimista**

Un tipo de bloqueo en el que la página de datos que contiene uno o más registros, incluido el registro que se está editando, está disponible para otros usuarios sólo mientras se está actualizando el registro mediante el método **Update** , pero está disponible antes y después de la llamada a **Update** .

Bloqueo optimista se utiliza cuando se abre el objeto **Recordset** con el parámetro **LockType** o la propiedad establecido en **adLockOptimistic** o **adLockBatchOptimistic**. Vea también **bloqueo pesimista**.

**valor ordinal**

La ubicación numérico de un elemento dentro de un pedido. En una colección de ADO, el valor ordinal del primer elemento es cero (0). El siguiente elemento es uno (1) y así sucesivamente.

Volver arriba

## <a name="p"></a>P

**comando parametrizado**

Una consulta o el comando que le permite establecer los valores de parámetro antes de ejecutar el comando. Por ejemplo, se puede parametrizar una cadena SQL mediante la incorporación de los marcadores de parámetros en la cadena SQL (designado por la '?' carácter). A continuación, la aplicación especifica valores para cada parámetro y ejecuta el comando.

**primario**

El control al lado de una relación jerárquica. En una estructura jerárquica, un elemento primario tiene uno o varios nodos secundarios directamente por debajo de él en la jerarquía. Vea también **alias primario**, la **relación de elementos primarios y secundarios**, **secundarios**.

**alias primario**

Un alias que hace referencia al elemento primario. Vea también **alias**, **principal**.

**relación de elementos primarios y secundarios**

Una relación en una estructura jerárquica en el que el objeto primario es un nivel superior y directamente asociado a uno o más elementos secundarios. Un elemento secundario está un nivel por debajo y debe tener un elemento primario. Vea también: **primario**, **secundario**.

**conservar**

Para guardar datos en un estado permanente, como guardar un **objeto Recordset** en un archivo.

**bloqueo pesimista**

Un tipo de bloqueo en el que la página que contiene uno o más registros, incluido el registro que se está editando, está disponible para otros usuarios para asegurarse de que se realizará una actualización. Comportamiento del bloqueo pesimista es definido por el proveedor OLE DB. Normalmente, los registros se bloquean durante una modificación y permanecen no disponibles hasta que haya completado el método **Update** .

Bloqueo pesimista se habilita cuando el objeto **Recordset** se abre con el parámetro **LockType** o la propiedad que se establece en **adLockPessimistic**. Vea también **bloqueo optimista**.

**limitación de peticiones**

Optimización del rendimiento en función de las colecciones de recursos previamente asignados, como objetos o conexiones de base de datos. Es más eficaz para dibujar un recurso existente desde el grupo de servidores que la creación de un nuevo recurso.

**ProgID (identificador de programación)**

Un nombre único asignado al registro de Windows por una aplicación COM. El ProgID para una conexión ADO es "ADODB. Conexión". Vea también **CLSID**, **COM**.

**proxy**

Un objeto específica de la interfaz que proporciona el cálculo de referencias de parámetro y comunicación necesarios para que un cliente llamar a un objeto application que se ejecuta en un entorno de ejecución diferente, como en un subproceso diferente o en otro proceso. El proxy se encuentra con el cliente y se comunica con un código auxiliar correspondiente que se encuentra con el objeto de aplicación que se llama. Vea también **código auxiliar**.

Volver arriba

## <a name="r"></a>L

**dirección URL relativa**

Dirección URL parcialmente cualificada que especifica un recurso en Internet o en una intranet cuya ubicación es relativa a un punto de partida especificado por una dirección URL absoluta o un objeto Connection de ADO equivalente. En efecto, la constituyen de direcciones URL concatenado de absolutas y relativa una dirección URL completa. Vea también **URL** y **URL absoluta**.

**origen de datos remoto**

Un origen de datos que se encuentra en un equipo de otro, en lugar de en el sistema local (donde se ejecuta la aplicación cliente).

**registro de recursos**

Un registro de un proveedor de orígenes de documentos que contiene campos para la definición y la descripción de una carpeta o un documento. El propio documento no está contenido en el registro de recursos, pero normalmente se puede tener acceso por la secuencia predeterminada o un campo en el registro de recursos que contiene una dirección URL. Vea también **proveedor de origen de documentos**, **secuencia predeterminada**y **dirección URL**.

**root**

El nivel superior de una estructura de árbol jerárquica. El nodo raíz no tiene principales, pero puede tener elementos secundarios. Vea también **jerarquía**, **árbol**, **primario**y **secundario**.

**conjunto de filas**

Un conjunto de filas de un origen de datos, todos los que tengan el mismo esquema de campo. Un conjunto de filas puede representar algunos o todos los campos de una tabla. Un conjunto de filas también puede representar una tabla virtual, creada mediante una consulta o una combinación de dos o más tablas. En ADO, los conjuntos de filas se representan mediante objetos **Recordset** .

Volver arriba

## <a name="s"></a>S

**esquema**

Una descripción de una base de datos para el sistema de administración de base de datos (DBMS), normalmente generado mediante el lenguaje de definición de datos proporcionado por el DBMS. Un esquema define los atributos de la base de datos, como tablas, columnas y propiedades.

**ámbito**

El intervalo de referencia para un objeto o variable o un intervalo de registros de una tabla o vista. Por ejemplo, pueden hacer referencia a las variables locales sólo dentro del procedimiento en el que se definieron. Las variables public son accesibles desde cualquier parte de la aplicación. Objetos, como la base de datos actual, están en el ámbito si se encuentran en la ruta de acceso de búsqueda definidas. Los intervalos de registros se pueden especificar con una cláusula de ámbito en muchos comandos.

**proveedor de servicios**

Software que encapsula un servicio al producir y consumir datos, aumentan las características de las aplicaciones ADO. Es un proveedor que no expone datos directamente, sino que proporciona un servicio, como el procesamiento de consultas. El proveedor de servicio puede procesar datos proporcionados por un proveedor de datos. Vea también **proveedor de datos**.

**objeto Recordset con forma**

Un **objeto Recordset** cuyas columnas se han definido específicamente para contener no sólo datos, sino también referencias (denominadas capítulos) a otros objetos **Recordset** y/o valores calculados basados en otros objetos **Recordset** .

**elemento del mismo nivel**

Dos o más nodos en una estructura jerárquica que se encuentran en el mismo nivel en la jerarquía. El nodo raíz en una jerarquía no tiene ningún elementos del mismo nivel.

**procedimiento almacenado**

Conjunto precompilado de código como instrucciones SQL e instrucciones de control de flujo opcionales almacenadas con un nombre y procesadas como una unidad. Los procedimientos almacenados se almacenan en una base de datos; se pueden ejecutar con una llamada desde una aplicación y permiten variables declaradas por el usuario, ejecución condicional y otras características de programación eficaces.

**código auxiliar**

Un objeto específica de la interfaz que proporciona el cálculo de referencias de parámetro y comunicación necesarios para que un objeto application recibir llamadas desde un cliente que se ejecuta en un entorno de ejecución diferente, como en un subproceso diferente o en otro proceso. El código auxiliar se encuentra con el objeto application y se comunica con un proxy correspondiente que se encuentra con el cliente que lo llama. Vea también **proxy**.

**nodo secundario**

Vea **secundario**.

**operación sincrónica**

Una operación iniciada por el código que se haya completado antes de que puede comenzar la siguiente operación. Vea también la **operación asincrónica**.

Volver arriba

## <a name="t-w"></a>T-W

**árbol**

Una estructura que representa una relación jerárquica entre elementos (nodos). Hay un nodo en el nivel superior de un árbol (la raíz). Debajo de la raíz, puede haber varios elementos secundarios. Cada objeto secundario a su vez puede ser el elemento principal de otros secundarios, bifurcando así la estructura como un árbol. Una carpeta que contiene documentos y otras carpetas es un ejemplo típico de una estructura de árbol. Vea también **jerarquía**, **nodo**, **raíz**, **secundario**y **primario**.

**Dirección URL (Uniform Resource Locator)**

Especifica la ubicación de un recurso que reside en Internet o en una intranet. Una dirección URL completa consta de un esquema (por ejemplo, FTP, HTTP, mailto, archivo y así sucesivamente), seguido de un punto y coma, un nombre de servidor y la ruta de acceso completa de un recurso (por ejemplo, un documento, gráfico u otro archivo). Algunos ejemplos de direcciones URL son:  
  
- https://www.domain.com/default.html  
- FTP://FTP.Server.somewhere/ftp.File  
  
- FTP://FTP.Server.somewhere/ftp.File  
- File://Server/Share/File.doc

Vea también **URL absoluta** y **URL relativa**.

**servidor Web**

Un equipo que proporciona servicios web y las páginas en la intranet y los usuarios de Internet.



