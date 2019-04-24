---
title: Acerca de la compatibilidad de InfoPath con tecnologías XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: Microsoft InfoPath es una herramienta híbrida que combina lo mejor de una experiencia de edición de documentos tradicional, como un procesador de texto o una aplicación de correo electrónico, con las capacidades rigurosas de captura de datos de un paquete de formularios. Este artículo describe los problemas para los cuales InfoPath fue diseñado y explica los principios de diseño y los estándares de la industria de XML que se usan para solucionar estos problemas.
ms.openlocfilehash: 20831635fba8d76b9d6b45f42a5308ab7236db20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300339"
---
# <a name="about-infopath-support-for-xml-technologies"></a>Acerca de la compatibilidad de InfoPath con tecnologías XML

Microsoft InfoPath es una herramienta híbrida que combina lo mejor de una experiencia de edición de documentos tradicional, como un procesador de texto o una aplicación de correo electrónico, con las capacidades rigurosas de captura de datos de un paquete de formularios. Este artículo describe los problemas para los cuales InfoPath fue diseñado y explica los principios de diseño y los estándares de la industria de XML que se usan para solucionar estos problemas.
  
## <a name="introduction"></a>Introducción

InfoPath es una herramienta de creación de XML de alto nivel que permite a los usuarios finales comunes crear documentos XML que pertenecen a un esquema XML definido por el usuario. Cuando el usuario edita un documento XML, las modificaciones en el documento son controladas por el esquema XML.
  
El usuario interactúa con el documento XML mediante una vista enriquecida y con formato que se muestra aplicando una hoja de estilos XSLT en el documento. Un nodo de hoja o valor del atributo del documento XML se muestra como un campo, por ejemplo, un cuadro de texto o una casilla, mientras que una jerarquía de nodos se muestra como un grupo de campos.
  
InfoPath habilita una edición validada y estructurada de datos XML al mostrar las acciones de edición válidas para el campo o grupo de campos seleccionados. Esta edición estructurada permite al usuario agregar y quitar elementos y atributos XML válidos al trabajar con grupos de campos que se muestran en vistas dinámicas enriquecidas, sin visualizar los elementos y atributos.
  
InfoPath soluciona un problema en el área de recopilación de datos que no pudo ser resuelto antes de la llegada de XML: al proporcionar formularios que pueden crecer con el agregado de grupos de campos que usan el modelo de datos jerárquico XML, InfoPath agrega la flexibilidad de los documentos de un procesador de texto a las rigurosas características de validación de una aplicación de formularios. Las transformaciones complejas XSLT son una parte integral de esta solución que ofrece vistas dinámicas y fáciles de usar de datos XML.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Limitaciones de documentos y formularios convencionales para la recopilación de datos

Al recopilar datos corporativos, los usuarios, por lo general, desean mayor flexibilidad que los formularios estáticos; no obstante, exigen una edición y validación más estructuradas que los documentos de procesador de textos.
  
Los formularios convencionales son estáticos y tienen una extensión limitada. Asimismo, cuentan con un número fijo de filas repetidas, y no se pueden extender cuando se lo completa. Los formularios convencionales son difíciles de usar ya que no tienen características enriquecidas. Por lo general, el usuario debe proporcionar toda la información de una vez.
  
Por otra parte, los documentos convencionales creados mediante el uso de un procesador de textos permiten al usuario agregar y quitar contenido libremente, aunque proporcionan poca ayuda respecto de cómo escribir información completa, estructurada y válida. Cualquier campo que esté definido en el documento tiene una validación mínima o carece de validación respecto de valores de datos y tipos de datos. Los datos en los campos no están etiquetados de manera correcta para permitir una referencia fácil y reutilización automática. Los datos son de forma libre en lugar de estructurados; no se puede agrupar la información, por ejemplo, aplicar una etiqueta "Dirección" a un grupo de campos "Calle", "Ciudad" y "Estado".
  
Por lo tanto, existe la necesidad de dicha edición flexible aunque estructurada, pero debido a que este tipo de tecnología no estaba disponible antes de la llegada de XML, los desarrolladores crearon aplicaciones personalizadas, las cuales requieren una codificación amplia. Las aplicaciones personalizadas son costosas y difíciles de modificar, y requieren una codificación personalizada para su validación. Las aplicaciones personalizadas, por lo general, requieren entrenamiento del usuario final, y es difícil reutilizar los datos resultantes para otros procesos corporativos.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Suministro de una edición estructurada al mostrar datos XML como grupos de campos

Un importante problema técnico de diseño que debió ser resuelto fue la manera de ofrecer una interfaz de usuario fácil para agregar y quitar elementos y atributos XML, sin mostrar los elementos y atributos, pero manteniendo el árbol DOM válido de acuerdo con el esquema XML definido por el usuario. La interfaz de usuario necesitaba ofrecer una forma natural de editar el árbol DOM que incluya insertar subárboles opcionales, reemplazar una elección de subárboles y extender los subárboles existentes.
  
A fin de proporcionar esta interfaz de usuario fácil, se muestra un subárbol DOM como un grupo de campos o una sección. Un grupo de campos es un grupo de controles de la UI, como cuadros de texto y listas desplegables, y funciona como una interfaz de usuario sencilla que permite al usuario visualizar y editar datos XML jerárquicos. Un grupo de campos puede contener otros grupos de campos y pueden ser opcionales o repetidos, al igual que un subárbol DOM puede contener otros subárboles y pueden ser opcionales o repetidos. Un subárbol se agrega al árbol DOM cuando el usuario mantiene el puntero del mouse sobre un grupo de campos, hace clic en el menú de la lista desplegable que aparece en el grupo de campos y, luego, selecciona **Insertar \<nombre de grupo de campos\>**.
  
InfoPath proporciona esta edición estructurada de datos XML mediante el uso de un esquema XML especificado para restringir y guiar la edición. El esquema controla si los comandos **Insertar** y **Quitar** aparecen en el menú de la lista desplegable para un grupo de campos. El esquema también se usa para la validación. Para habilitar la edición de un documento XML para el cual no existe ningún esquema XML, InfoPath puede generar un esquema de un documento XML. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Suministro de vistas fáciles de usar de datos XML mediante el uso de transformaciones XSLT

Otro desafío de diseño técnico que fue necesario resolver fue cómo habilitar el contenido de las vistas de la UI para que estén organizadas de diferente manera que la estructura de datos XML. Para presentar los datos de manera intuitiva para el usuario y para habilitarlo a leer y editar los datos, el diseñador debe poder mostrar datos en una secuencia distinta que en el árbol de datos DOM, omitir algunos datos de una vista, reorganizar los nodos del árbol de datos adyacentes en vistas separadas y recopilar datos de distintas partes del árbol de datos en una única vista.
  
Por lo tanto, el orden y la estructura del contenido de las vistas deben ser independientes del orden y de la estructura de los nodos del árbol DOM. Esta independencia estructural de presentación y datos requiere un vínculo o una asignación dinámicos y complejos entre los campos agrupados en las vistas y los nodos en el árbol DOM.
  
Para proporcionar esta asignación compleja entre las vistas y los datos, InfoPath usa las Transformaciones XSL (XSLT) de forma extensiva. XSLT es un lenguaje de hoja de estilos relevante compatible con transformaciones XSLT complejas y vistas enriquecidas con una presentación de contenido flexible y dinámica. Se usa un archivo XSLT para cada vista. El uso de una hoja de estilos es un enfoque de diseño común y bien establecido en herramientas de creación de SGML y XML. Asimismo, XSLT es el estándar de W3C para hojas de estilos que se usan para este tipo de transformación compleja.
  
Para evitar ejecutar la transformación XSLT completa cada vez que el usuario modifica la estructura de un subárbol en el DOM, se usan algoritmos a fin de determinar qué parte de la vista debe ser actualizada. A continuación, se aplica la parte relevante de la hoja de estilos XSLT, y se actualiza la parte afectada de la vista.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Cómo se usan los estándares XML al editar un formulario

InfoPath se construye a partir de los estándares XML que incluyen lo siguiente:
  
- Lenguaje de marcado extensible (XML) 1.0 Segunda edición
    
- Espacios de nombres en XML
    
- Lenguaje de rutas XML (XPath) 1.0
    
- Esquema XML (XSD) 1.0 Parte 1: Estructuras y Parte 2: Tipos de datos
    
- Lenguaje de transformación basado en hojas de estilos (XSLT) 1.0
    
- Lenguaje de marcado de hipertexto extensible (XHTML) 1.0
    
- Hojas de estilo en cascada (CSS)
    
- Modelo de objetos de documento (DOM) 1.0
    
- Firmas digitales XML (XML DSig)
    
- Protocolo simple de acceso a objetos (SOAP) 1.1
    
- Lenguaje de descripción de servicios web (WSDL) 1.1
    
- Universal Description, Discovery, and Integration (UDDI) 1.0
    
Por ejemplo, InfoPath usa y genera archivos estándar XML, XSLT y XSD que se pueden reutilizar en diversos procesos corporativos. InfoPath usa MSXML, el kit de herramientas SOAP y el espacio de nombres .NET System.XML para admitir estos estándares, y proporciona una compatibilidad completa e integrada para los servicios web XML.
  
La figura 1 muestra el menú de la lista desplegable contextual para un grupo de campos **customer**, que permite al usuario agregar otro grupo de campos **customer**, quitar este grupo de campos **customer**, insertar una fila **item** en la tabla de elementos de compra de este grupo de campos, o insertar un grupo de campos **actions** opcional dentro de este grupo de campos. El vínculo **Haga clic aquí** ofrece otra manera de insertar el grupo de campos **actions**. Un menú de la lista desplegable más abreviado aparece en cada fila de los elementos de compra. 
  
1. En InfoPath, el usuario crea un documento XML nuevo basado en una plantilla de formulario de InfoPath o abre un documento XML existente basado en una plantilla de formulario. El documento XML es un archivo de datos XML que contiene una referencia a la plantilla de formulario y puede usar espacios de nombres XML. 
    
    Una plantilla de formulario es un conjunto de archivos que proporciona una edición estructurada de documentos XML que cumplen con un esquema XML específico definido por el usuario. Los archivos que conforman la plantilla de formulario pueden estar empaquetados como archivos individuales dentro de una carpeta común o como archivos que residen en una carpeta de archivos. En ambos casos, los archivos son archivos XML estándar y archivos auxiliares opcionales, como ensamblados de código administrado.
    
2. Si el documento XML está firmado de forma digital con Firma XML, InfoPath confirma que el archivo XML es consistente antes de abrirlo.
    
3. InfoPath crea un árbol de datos DOM del documento XML en la memoria.
    
4. Las transformaciones XSLT se aplican al árbol DOM, lo cual genera vistas que muestran una presentación apropiada del documento al usuario. Los elementos al comienzo del documento XML se pueden mostrar en la parte inferior de la vista y también en un arreglo distinto en otra vista. Las vistas consisten en contenedores de UI, como las secciones que contienen texto y controles, por ejemplo, cuadros de texto, cuadros de texto enriquecidos, selectores de fechas y listas desplegables. Los contenedores también incluyen otros contenedores.
    
5. La transformación XSLT genera un XHTML como resultado y, a continuación, se usan CSS para controlar la presentación del XHTML.
    
6. Si el esquema XML permite agregar nodos a un nodo de un árbol de datos, el campo o grupo de campos asignados al nodo tiene un menú desplegable que habilita al usuario agregar o quitar grupos de campos. El usuario edita el documento al agregar un grupo de campo repetido u opcional, al escribir un valor, al seleccionar una opción o al escribir texto enriquecido. Si un nodo del esquema XML está asociado al esquema XHTML, InfoPath presenta una UI para crear texto enriquecido. Cuando el usuario escribe texto enriquecido, el contenido XHTML se crea como un subárbol en el DOM.
    
7. El árbol DOM siempre se mantiene válido. A medida que el usuario edita el documento XML, las modificaciones son validadas con el esquema XML asociado. Los cambios intentados en los valores de la estructura del DOM y del nodo de hojas son validados con el esquema XML a fin de comprobar que sus tipos y valores de datos sean válidos. Si los cambios intentados no son válidos, se abre un cuadro de diálogo de validación, y los cambios no se aplican en el árbol DOM. Si los cambios son válidos, el árbol DOM se actualiza.
    
8. La parte modificada de la vista se actualiza al aplicar las partes requeridas solamente de la hoja de estilos XSLT en el árbol DOM.
    
9. El usuario puede guardar el documento XML o enviar el documento XML al usar HTTP o SOAP sin formato. El usuario no puede enviar el documento a menos que éste sea válido de acuerdo con el esquema XML.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a>Cómo se usan los estándares XML en el diseño de un formulario

Se puede diseñar un formulario al comenzar con un esquema XML existente, al conectarse a un servicio web o a una base de datos XML y obtener su esquema XML, o al generar de manera automática un esquema desde un nuevo formulario o desde un archivo de datos XML. Estos escenarios se describen en los siguientes procedimientos. La figura 3 muestra la interfaz de usuario básica para diseñar una plantilla de formulario.
  
1. Para crear un nuevo formulario en InfoPath Designer, seleccione la plantilla de formulario **XML o esquema** y elija un archivo de esquema XML existente como origen de datos. El esquema XML se carga en el panel de tareas y se muestra como un control del árbol. 
    
2. Use las herramientas de diseño para disponer los controles de la UI, como las filas y el diseño de fondo, en una o más vistas. Esto genera algunos de los elementos XSLT. Las vistas XSLT y el esquema XML se asocian de forma automática a la plantilla de formulario.
    
3. Asigne los elementos del esquema XML a los controles de la UI en las vistas mediante la operación de arrastrar y colocar. InfoPath le ayuda a elegir los controles apropiados para los elementos del esquema XML, basados en el tipo de elementos del esquema. Por ejemplo, si el tipo de datos XML es una fecha, InfoPath sugiere un control de selector de fechas. Según las elecciones en el esquema XML, InfoPath puede insertar grupos de campos opcionales o repetidos. La asignación de los elementos del esquema XML a los controles de la UI genera la estructura XSLT.
    
4. Guarde la plantilla de formulario. Puede guardar los archivos que conforman la plantilla de formulario como archivos individuales en una carpeta regular o como archivos en una carpeta de archivos. En ambos casos, los archivos son archivos XML estándar. La plantilla de formulario está ahora lista para su uso.
    
Una plantilla de formulario incluye toda la información semántica necesaria para proporcionar una edición estructurada cuando se abre un formulario en InfoPath. Una plantilla de formulario incluye un archivo de manifiesto, los archivos XSLT que definen las vistas, la información necesaria para validar datos y un identificador de recursos opcional para un servicio web XML.
  
El archivo de manifiesto o el archivo de definición del formulario es un concentrador y punto de entrada comunes para todos los archivos requeridos por la plantilla de formulario. El manifiesto incluye referencias de los otros archivos en la plantilla de formulario y contiene la información necesaria para validar datos y proporcionar una edición estructurada. La información de validación del esquema XML está personalizada para la interfaz de usuario resultante y se agrega al archivo de manifiesto. Por ejemplo, si el esquema permite insertar varios elementos opcionales en un subárbol específico, puede diseñar la UI para que los elementos opcionales se agreguen cuando el usuario realiza una operación de UI única. Esta personalización es importante para proporcionarle al usuario estándar una buena experiencia. 
  
Asimismo, puede diseñar un formulario al usar un servicio web existente para proporcionar el esquema XML. Para hacerlo:
  
1. Use UDDI para ubicar los servicios web relevantes.
    
2. Seleccione el servicio web que va a usar. InfoPath muestra el archivo WSDL asociado al servicio web e identifica el esquema XML que se va a usar.
    
3. Abra el esquema XML para cargarlo.
    
4. Disponga los controles de la UI y asócielos a los elementos y atributos del esquema XML.
    
5. Defina cómo enviar el documento XML al servicio web que usa SOAP.
    
Si desea diseñar un formulario desde el principio y generar de manera automática el esquema XML:
  
1. En la ficha **Archivo**, seleccione la plantilla de formulario **Formulario en blanco** o **Formulario en blanco (InfoPath Filler)** y haga clic en **Diseñar formulario**.
    
2. En la ficha **Inicio**, haga clic en la flecha de la esquina inferior derecha del grupo **Controles** para mostrar el panel de tareas **Controles** y asegúrese de que la casilla de verificación **Crear origen de datos automáticamente** está activada. (Esta casilla de verificación está activada de manera predeterminada). 
    
3. Disponga los controles de la UI. Cuando los disponga, InfoPath crea de manera automática el esquema XML y asigna sus elementos y atributos a los controles de la UI.
    
Para diseñar un formulario comenzando con cualquier archivo de datos XML de formato correcto:
  
1. En la ficha **Archivo**, seleccione la plantilla de formulario **XML o esquema** y haga clic en **Diseñar formulario**.
    
2. En el **Asistente del origen de datos**, seleccione el archivo XML que desea usar como origen de datos. Se creará automáticamente un esquema XML basado en el archivo de datos XML.
    
3. Disponga los controles de la UI como se describieron anteriormente en esta sección.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Diseñado como un cliente ideal para servicios web

La amplia compatibilidad en toda la industria para los servicios web está comenzando a estar disponible. Muchos sistemas back-end y de nivel intermedio se pueden configurar para comunicar usando los estándares de servicios web, como SOAP, UDDI y WSDL. Estos sistemas de servicios web habilitados incluyen bases de datos, sistemas de flujo de trabajo, planeación de recursos empresariales (ERP), administración de relaciones con el cliente (CRM) y otros sistemas. Actualmente, InfoPath proporciona una UI ideal para visualizar y editar datos XML que se envían a través de los servicios web. La figura 4 muestra la compatibilidad integrada de los servicios web XML.
  
InfoPath se adapta bien con el modelo acoplado de forma imprecisa de los servicios web, en el que los datos se envían entre equipos como documentos XML completos. Este modelo de comunicación general se adapta bien con la naturaleza asincrónica de la Web. Como herramienta de creación de alto nivel para documentos XML, InfoPath admite la codificación SOAP de documento/literal en lugar de la codificación SOAP de llamada a procedimiento remoto (RPC). InfoPath es un cliente ideal para servicios web, ya que puede leer de forma nativa el esquema XML detallado en el mensaje SOAP y, luego, crear una UI basada en el esquema, la cual permite a los usuarios visualizar y editar con facilidad los documentos XML generados o recibidos por medio del servicio web correspondiente. InfoPath también admite ADO.NET DataSets que incluye seguimiento de cambios.
  
## <a name="terminology"></a>Terminología

|||
|:-----|:-----|
|**grupo de campos:** <br/> |Una sección, una sección repetida u opcional, o una tabla repetida. Las secciones y las tablas repetidas son controles en un formulario que incluyen otros controles, y que se repiten a medida que son necesarios. Los usuarios pueden insertar varias secciones o filas cuando completan el formulario.  <br/> |
|**Árbol DOM:** <br/> |La estructura del origen de datos del formulario. En concreto, la colección de campos y grupos que definen y almacenan los datos de un formulario de InfoPath.  <br/> |
   
## <a name="conclusion"></a>Conclusión

InfoPath usa estándares open XML para proporcionar a los usuarios una edición XML flexible aunque estructurada para la recopilación de datos. A fin de proporcionar una interfaz de usuario sencilla para visualizar y editar datos XML jerárquicos, los grupos de campos anidados que contienen controles de UI se asignan al árbol DOM. Las transformaciones XSLT permiten que el contenido de las vistas de la UI se organicen de forma diferente que la estructura de los datos XML.
  
InfoPath proporciona mayor flexibilidad que los formularios estáticos, con una edición y validación más estructuradas que los documentos de procesador de textos. El resultado es una herramienta híbrida que combina lo mejor de una experiencia de edición de documentos convencional con las rigurosas capacidades de captura de datos de un paquete de formularios, lo cual permite a los usuarios crear documentos XML válidos que pertenecen a un esquema XML definido por el usuario. La compatibilidad integrada de los servicios web habilita vistas de definición sencillas para editar documentos XML que cumplen con un esquema de servicios web.
  

