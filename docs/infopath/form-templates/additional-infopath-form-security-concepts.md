---
title: Conceptos de seguridad adicionales de los formularios de InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 77425a61-bf33-b3d8-442a-caee48e54a48
description: El modelo de seguridad de Microsoft InfoPath está basado en el modelo de seguridad implementado por Internet Explorer. El modelo de seguridad de Internet Explorer ayuda a proteger su equipo de operaciones inseguras mediante el uso de zonas y niveles de seguridad. Al trabajar junto al modelo de seguridad de Internet Explorer, InfoPath proporciona dos tipos de implementación de formularios que afectan a la manera en que un formulario de InfoPath trabaja dentro de este modelo de seguridad.
ms.openlocfilehash: 00b0e306507db19f55059fba91277af1ad1714b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303776"
---
# <a name="additional-infopath-form-security-concepts"></a>Conceptos de seguridad adicionales de los formularios de InfoPath

El modelo de seguridad de Microsoft InfoPath está basado en el modelo de seguridad implementado por Internet Explorer. El modelo de seguridad de Internet Explorer ayuda a proteger su equipo de operaciones inseguras mediante el uso de zonas y niveles de seguridad. Al trabajar junto al modelo de seguridad de Internet Explorer, InfoPath proporciona dos tipos de implementación de formularios que afectan a la manera en que un formulario de InfoPath trabaja dentro de este modelo de seguridad.
  
- **Formularios basados en URL** Este método de implementación es el predeterminado al publicar un formulario de InfoPath en un servidor web, biblioteca de formularios SharePoint Foundation o recurso compartido de archivos. Estos formularios se conocen como formularios basados en URL debido a que un usuario generalmente abre el formulario desde la dirección URL donde el formulario está publicado y esa dirección URL está especificada en el atributo **publishUrl** del elemento **xDocumentClass** en el archivo de definición de formulario (.xsf). Los formularios basados en URL se denominan de espacio aislado, debido a que tienen acceso restringido a los recursos del sistema y a otras posibles áreas de riesgo. Un formulario basado en URL tiene el mismo nivel de permisos que una página web que se abre desde la misma ubicación que el archivo de plantilla de formulario (.xsn).
    
- **Formularios basados en URN** Este es un método de implementación para formularios que requieren acceso a los recursos del sistema y a otros recursos externos, como controles ActiveX y otros componentes de software. Puede implementar los formularios de InfoPath como formularios de plena confianza. Tales formularios también se conocen como formularios basados en URN porque, en lugar de especificar el atributo **publishUrl**, especifican el nombre de recursos uniforme (URN) del atributo **name** del elemento **xDocumentClass** en el archivo de definición de formulario (.xsf). Esta clase de formulario puede requerir plena confianza si el atributo **requireFullTrust** del elemento **xDocumentClass** se establece como  `"yes"` en el archivo de definición de formulario (.xsf). Los formularios basados en URN se deben registrar en el equipo del cliente por medio de un programa de instalación o script. En este caso, el formulario tiene los mismos permisos que una aplicación que se ejecuta en el equipo local. 
    
Conjuntamente con estos dos métodos de implementación de formularios, cada método y propiedad del modelo de objetos de InfoPath tiene un nivel de seguridad que controla cuándo se puede llamar a ese método o propiedad desde el script que se ejecuta desde el formulario.
  
## <a name="understanding-infopath-integration-with-the-internet-explorer-security-model"></a>Descripción de la integración de InfoPath con el modelo de seguridad de Internet Explorer

Internet Explorer implementa zonas de seguridad que le permiten controlar el nivel de acceso otorgado a su equipo por las páginas web que abre. InfoPath usa algunas de estas zonas para determinar el nivel de acceso a los recursos de su equipo que se otorga a los formularios. De forma predeterminada, los formularios de InfoPath se ejecutan en una ubicación en caché a la que se niega el acceso a recursos del sistema críticos. Los formularios a los que se otorga acceso total a los recursos del sistema se llaman formularios de plena confianza. Los formularios de plena confianza generalmente se instalan y se registran mediante un programa de instalación o script, o se firman digitalmente para que se les conceda un nivel de permisos superior.
  
Los formularios en caché de InfoPath se identifican por la dirección URL o el URN especificados en el archivo de definición de formulario (.xsf) del formulario. El tipo de identificación que se usa y el dominio (ubicación) desde el que se abre la plantilla de formulario determinan qué permisos de zona de seguridad de Internet Explorer heredará el formulario. Los formularios identificados por una dirección URL están almacenados en la memoria caché del equipo del usuario, lo que permite el uso sin conexión del formulario. Estos formularios basados en URL heredan sus permisos de seguridad y sus privilegios de acceso específicos, como acceso entre dominios, de la configuración de seguridad de Internet Explorer aplicable a la ubicación original de la plantilla de formulario. Las plantillas de formulario almacenadas en un servidor web o en un servidor que ejecuta SharePoint Foundation se ejecutan en Internet o en la zona intranet local, según el dominio del servidor. Los formularios instalados que son identificados por un URN, por el contrario, heredan sus permisos de la zona de equipo local, que concede un nivel de permisos similar al de los archivos de aplicación HTML (.hta).
  
Los formularios de plena confianza se identifican por su URN y por el hecho de que el atributo **requireFullTrust** del elemento **xDocumentClass** del archivo de definición del formulario (.xsf) está establecido como  `"yes"`. En InfoPath, una vez que los formularios de plena confianza se han instalado, aparecerán en la pestaña **Nuevo** en el Microsoft Office Backstage del editor de InfoPath. 
  
Para obtener detalles sobre cómo funcionan los formularios de plena confianza y cómo crearlos e implementarlos, vea el tema sobre la [Descripción de los formularios de plena confianza](understanding-fully-trusted-forms.md).
  
## <a name="trusting-installed-forms"></a>Confiar en los formularios instalados

La capacidad de usar formularios de confianza se puede habilitar o deshabilitar en equipos individuales. Cuando un equipo se configura para confiar en los formularios instalados, los usuarios pueden rellenar formularios que requieren acceso a los recursos de sus equipos.
  
En el editor de InfoPath, se puede configurar un equipo para que confíe en los formularios instalados en Backstage; para ello, haga clic en **Opciones**, **Centro de confianza**, **Configuración del Centro de confianza** y, a continuación, active la casilla de verificación **Permitir que se ejecuten en mi equipo formularios de plena confianza** de la ficha **Editores de confianza** del cuadro de diálogo **Centro de confianza**. 
  
## <a name="using-security-features-in-infopath"></a>Usar características de seguridad en InfoPath

El modelo de seguridad de InfoPath ayuda a proteger a los usuarios contra las siguientes amenazas que representan las plantillas creadas de forma malintencionada:
  
- El potencial de divulgación de información confidencial del equipo local o de los orígenes de datos remotos.
    
- El uso malintencionado de controles ActiveX.
    
- El uso malintencionado de propiedades y métodos del modelo de objetos de InfoPath.
    
## <a name="cross-domain-data-access"></a>Acceso a datos entre dominios

Esta clase de escenarios de riesgo de seguridad se denomina acceso a datos entre dominios.
  
El modelo de seguridad de Internet Explorer en el que se basa InfoPath proporciona una configuración llamada **Tener acceso a origen de datos entre dominios**. De forma predeterminada, esta configuración deshabilita el acceso entre dominios a los formularios de InfoPath que residen en las zonas de seguridad de Internet y Sitios restringidos. Le pide al usuario que permita o niegue el acceso entre dominios a los formularios de InfoPath que residen en la zona de seguridad de intranet local y habilita el acceso entre dominios a los formularios de InfoPath que residen en las zonas **Sitios de confianza** o **Equipo local**. 
  
## <a name="use-of-the-infopath-html-task-pane"></a>Uso del panel de tareas HTML de InfoPath

El panel de tareas HTML de InfoPath permite la presentación de páginas web, como archivos .htm, .asp y .hta. Las páginas a las que se hace referencia desde los paneles de tareas se pueden ubicar dentro o fuera de la plantilla de formulario. La única restricción con respecto a qué se puede hacer referencia desde fuera de la plantilla de formulario es que la página web debe estar en el mismo dominio que la plantilla de formulario o que la zona de seguridad en que la plantilla reside debe permitir los permisos de acceso entre dominios para cargar el panel de tareas.
  
El panel de tareas no expone una barra de direcciones o de estado y, por lo tanto, el usuario no tiene posibilidad de confirmar la ubicación del origen del panel de tareas o si se está teniendo acceso a esa ubicación a través de un canal cifrado (https). Por esta razón, debería evitar usar el panel de tareas para implementar o escribir información confidencial. El panel de tareas se diseñó para implementar información de ayuda dinámica y controles para navegar entre vistas y otros elementos de una solución integrada. Además, la lógica empresarial y el script de una plantilla de formulario en el panel de tareas pueden interactuar. Sin embargo, esta interacción se permite solo si la plantilla de formulario y el panel de tareas se encuentran en el mismo dominio, lo que ayuda a impedir el intercambio de información entre dominios.
  
## <a name="cross-domain-data-access-prompts"></a>Peticiones de acceso a datos entre dominios

Si una plantilla de formulario que requiere acceso a datos entre dominios está ubicada en una zona de seguridad configurada para pedir acceso a datos entre dominios (configuración predeterminada para la zona de intranet local), al usuario se le pedirá permitir el acceso. La elección del usuario se conservará por el tiempo en que el formulario permanezca abierto. Si debe implementar plantillas de formulario de InfoPath que requieren acceso a datos entre dominios, debería implementarlas como formularios de plena confianza o hacerlas disponibles en un servidor que se encuentre en la zona de seguridad de Sitios de confianza, para evitar peticiones de acceso. No se debería informar a los usuarios que al disminuir el nivel de seguridad de la zona de intranet local se pueden evitar estas peticiones.
  
## <a name="forms-without-a-publishurl-attribute"></a>Formularios sin un atributo publishURL

Si InfoPath carga una plantilla de formulario del equipo local y tiene un atributo **publishUrl** en blanco o falta el atributo, se ubicará el formulario en una zona de seguridad más restrictiva. Esto se realiza para reducir la amenaza de una plantilla de formulario malintencionada que se distribuye por correo electrónico. Como resultado, si el usuario guarda esta plantilla de formulario en el disco, ésta no podrá ejecutar los permisos de un formulario que reside en la zona del **Equipo local**. 
  
## <a name="unsafe-activex-controls"></a>Controles ActiveX no seguros

El escenario más común del uso malintencionado de los controles ActiveX se puede presentar si un autor usa un script con un control ActiveX que proporciona métodos para obtener acceso al sistema de archivos para recuperar archivos personales y listas de contraseñas, para eliminar archivos o para deshabilitar el sistema del usuario. Un formulario de InfoPath puede usar controles ActiveX solo desde script en el archivo scripting principal de un formulario (script.js) o desde script en un panel de tareas. InfoPath no permite que el script de las vistas de InfoPath ejecute controles ActiveX.
  
El modelo de seguridad de Internet Explorer en el que se basa Microsoft InfoPath proporciona una configuración llamada **Inicializar y generar script de controles ActiveX marcados como no seguros** que, de forma predeterminada, produce las siguientes acciones para formularios de InfoPath o paneles de tareas que intentan inicializar y generar script de controles ActiveX marcados como no seguros para scripting. 
  
|**Zona de seguridad e Implementación**|**Action**|
|:-----|:-----|
|Internet  <br/> |Deshabilitado  <br/> |
|Intranet local  <br/> |Deshabilitado  <br/> |
|Sitios restringidos  <br/> |Deshabilitado  <br/> |
|Sitios de confianza  <br/> |Prompt  <br/> |
|Mi PC  <br/> |Prompt  <br/> |
|Formulario de plena confianza  <br/> |Habilitación  <br/> |
   
## <a name="malicious-use-of-the-infopath-object-model"></a>Uso malintencionado del modelo de objetos de InfoPath

Al igual que los controles ActiveX llamados desde script, los métodos y propiedades de InfoPath llamados desde código pueden presentar diferentes niveles de riesgo. Por ejemplo, el método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) se puede usar para escribir datos en cualquier punto del sistema de archivos. 
  
Para protegerse del uso malintencionado de los miembros del modelo de objetos de InfoPath, el modelo de objetos de InfoPath implementa tres niveles de seguridad que determinan cómo y dónde se puede usar un miembro concreto del modelo de objeto. Existen tres niveles de seguridad en el modelo de objetos de InfoPath:
  
- **0** Miembros del modelo de objetos a los que se puede tener acceso sin restricciones. Estos miembros del modelo de objetos son seguros y, por lo tanto, se puede tener acceso a ellos sin restricciones. 
    
- **2** Solo pueden tener acceso a estos miembros del modelo de objetos los formularios que se ejecuten en el mismo dominio que el formulario abierto actualmente o los formularios a los que se hayan concedido permisos de acceso a datos entre dominios. Las plantillas de formulario restringidas que llaman a los métodos del modelo de objetos de nivel de seguridad 2 solo lo lograrán si están tratando de tener acceso a los recursos contenidos en la plantilla de formulario misma. 
    
- **3** Solo pueden tener acceso a estos miembros del modelo de objetos los formularios de plena confianza. 
    
- Cada uno de los temas sobre propiedades y métodos de la Referencia del modelo de objetos de InfoPath contiene una sección de seguridad que especifica el nivel de seguridad que se aplica a ese miembro del modelo de objetos.
    
- El nivel de seguridad **1** se reserva para uso futuro. 
    
## <a name="summary"></a>Resumen

En la siguiente tabla se resumen los permisos predeterminados para cada método de implementación de formularios en InfoPath. Los permisos se basan en la zona de seguridad del dominio desde el que se origina la plantilla de formulario.
  
|**Zona de seguridad**|**Implementación**|**Permisos predeterminados**|
|:-----|:-----|:-----|
||**Basado en URL** <br/> |**Basado en URN** <br/> |**ActiveX marcado como no seguro para scripting** <br/> |**Acceso a datos entre dominios** <br/> |**Nivel de seguridad del modelo de objetos** <br/> |
|Sitios restringidos  <br/> |N/D  <br/> |N/D  <br/> |N/D  <br/> |N/D  <br/> |N/D  <br/> |
|Internet  <br/> |X  <br/> ||Deshabilitar  <br/> |Deshabilitar  <br/> |2  <br/> |
|Intranet local  <br/> |X  <br/> ||Deshabilitar  <br/> |Prompt  <br/> |2  <br/> |
|Sitios de confianza  <br/> |X  <br/> ||Prompt  <br/> |Habilitación  <br/> |2  <br/> |
|Equipo local  <br/> |X  <br/> |X  <br/> |Deshabilitar  <br/> |Prompt  <br/> |2  <br/> |
|Formulario de plena confianza  <br/> |X (firmado por un Editor de confianza)  <br/> |X  <br/> |Habilitación  <br/> |Habilitación  <br/> |3  <br/> |
|Formulario de plena confianza  <br/> ||X  <br/> |Habilitación  <br/> |Habilitación  <br/> |3  <br/> |
|Restricted  <br/> ||X  <br/> |Ningún ActiveX (excepto una lista codificada de forma rígida limitada)  <br/> |Deshabilitar  <br/> |2  <br/> |
|Restricted  <br/> |X  <br/> ||Ningún ActiveX (excepto una lista codificada de forma rígida limitada)  <br/> |Deshabilitar  <br/> |2  <br/> |
|Restricted  <br/> |X  <br/> |X  <br/> |Ningún ActiveX (excepto una lista codificada de forma rígida limitada)  <br/> |Deshabilitar  <br/> |2  <br/> |
   
Para obtener información acerca de las directrices generales de seguridad cuando se desarrollan formularios, vea el tema [Directrices de seguridad para desarrollar formularios de InfoPath](security-guidelines-for-developing-infopath-forms.md).
  
## <a name="understanding-other-security-features"></a>Descripción de otras características de seguridad

InfoPath proporciona otras medidas de seguridad para formularios que incluyen la protección del diseño del formulario mediante firmas digitales, la administración de ciertas operaciones de formularios como la combinación y el envío y la confianza en formularios instalados. En las siguientes secciones se describen estas medidas de seguridad y cuándo están habilitadas en InfoPath.
  
## <a name="digital-signatures"></a>Firmas digitales

Los datos contenidos en un formulario se pueden firmar digitalmente para garantizar que no se alteren sus contenidos.
  
Puede configurar un formulario para que use firmas digitales seleccionando las opciones **Permitir firmas para todo el formulario** o **Permitir firmas en algunas partes del formulario** en la sección **Firmas digitales** del cuadro de diálogo **Opciones de formulario**, que está disponible desde el Microsoft Office Backstage en el diseñador de formularios de InfoPath. Al rellenar el formulario, los usuarios pueden firmar y comprobar los formularios haciendo clic en el botón **Firmar formulario** en la pestaña **Información** del Microsoft Office Backstage. Cuando el formulario se vuelve a abrir, se alertará al usuario si los contenidos del formulario fueron alterados. 
  
-  Se pueden habilitar las firmas digitales para todo el formulario o para conjuntos específicos de datos del formulario que se puedan firmar por separado. 
    
- Puede elegir firmar sólo una sección específica de un formulario en lugar de firmar todo el formulario.
    
- Puede especificar si desea permitir firmas simples o múltiples. También puede especificar cuál es la relación para cada grupo de datos que se pueden firmar. Por ejemplo, puede especificar si las firmas son cofirmas en paralelo o si cada nueva firma contrafirma todas las anteriores.
    
- Puede usar el modelo de objetos de InfoPath para agregar mediante programación información personalizada al bloque de la firma en un formulario de plena confianza.
    
- Puede mejorar la seguridad de las firmas digitales capturando e incluyendo información adicional, como la marca de tiempo, como evidencia de no rechazo. Debido a que la evidencia adicional es parte de la firma, no se puede quitar sin invalidarla. En cualquier momento, podrá recuperar o examinar los datos capturados haciendo clic en una firma digital del formulario o seleccionando una firma digital de la lista de firmas digitales que se muestra en el cuadro de diálogo **Firmas digitales**. 
    
-  Puede insertar y ver una firma en el documento, y ver el formulario tal como fue presentado a cada firmante. 
    
- La firma digital también incluye una instantánea de la vista como fue presentada al firmante cuando firmó el formulario. La instantánea se almacena como una imagen con codificación Base64 en el formato de archivo estándar PNG. 
    
## <a name="email-deployment"></a>Implementación de correo electrónico

Puede implementar las plantillas de formulario como datos adjuntos a un mensaje de correo electrónico y mover las plantillas de formulario de una ubicación a otra. La implementación de correo electrónico es una forma fácil y efectiva de distribuir formularios para uso interno y de implementar formularios para usuarios remotos.
  
Puede firmar digitalmente una plantilla de formulario y, a continuación, establecer el nivel de seguridad de ese formulario como de Plena confianza. Además, los formularios de plena confianza firmados, cuando se implementan como datos adjuntos de correo electrónico, se pueden actualizar de forma más fácil y eficaz.
  
Todos los formularios de InfoPath Designer se crean con una identidad. Esta información ayuda a InfoPath a asociar formularios con plantillas de formulario en caché y a recuperar actualizaciones de formularios cuando se publican en una ubicación compartida. De forma predeterminada, InfoPath crea dos identidades para las plantillas de formulario: un id. de formulario y una ruta de acceso (también conocida como el atributo **publishURL**). Encontrará más información sobre la implementación de correo electrónico en el tema Niveles de seguridad, Implementación de correo electrónico [y Plantillas de formulario remotas.](security-levels-email-deployment-and-remote-form-templates.md)
  
## <a name="activex-controls"></a>Controles ActiveX

InfoPath admite el hospedaje de controles ActiveX en formularios que se abren en el editor de InfoPath. Los controles ActiveX pueden ser preexistentes (con algunas restricciones) o escritos específicamente para uso con InfoPath. ActiveX los controles que se usan en los formularios de InfoPath no se descargan automáticamente de los sitios web. En cambio, los archivos CAB para los controles ActiveX que todavía no se encuentran presentes en el equipo del usuario se deben agregar al archivo de plantilla de formulario.
  
Cuando se usa un control ActiveX en un formulario y el control no está registrado en el equipo del usuario, el comportamiento cuando se abre el formulario depende de la configuración del control ActiveX dentro del formulario. Si no se incluye un archivo CAB en el archivo de plantilla de formulario, InfoPath no abrirá el formulario. Si el archivo CAB está presente en el archivo de plantilla de formulario, InfoPath iniciará un proceso de instalación. Para que InfoPath instale un archivo CAB, el archivo debe estar firmado y la firma debe ser de un editor de confianza. Si el editor todavía no se encuentra en la lista de editores de confianza del usuario que tenga un certificado presente (con una cadena de confianza que conduzca a un certificado raíz de confianza), se le pedirá al usuario que acepte o niegue confiar en el editor. Si el usuario elige no confiar en el editor, no se instalará el archivo CAB para el control e InfoPath no abrirá el formulario.
  
> [!NOTE]
> [!NOTA] Para que InfoPath use los controles ActiveX, estos deben estar marcados como "Seguro para scripting" y "Seguro para inicializar con datos que no son de confianza". 
  
## <a name="net-security"></a>Seguridad .NET

Las plantillas de formulario con código administrado admiten, además de los niveles de seguridad específicos de InfoPath, características de seguridad adicionales para el acceso al código que se aplican al código administrado que se ejecuta en Common Language Runtime (CLR) de Microsoft .NET Framework.
  
Si el formulario es de plena confianza, puede tener acceso automáticamente a los recursos fuera de la plantilla de formulario. Se puede usar cualquier ensamblado en el código de lógica empresarial. Puede personalizar el conjunto de permisos que se agrega a una plantilla de formulario con código administrado mediante la herramienta de configuración de Microsoft .NET Framework o la herramienta de directiva de seguridad de acceso a código (Caspol.exe). InfoPath buscará un grupo de códigos predefinido y aplicará el grupo de permisos definido bajo ese grupo al dominio de aplicación (AppDomain) donde se ubica el código administrado y desde donde éste se ejecuta. Se deben implementar las directivas de seguridad personalizadas .NET en los equipos del cliente donde se ejecutará la plantilla de formulario con código administrado.
  
Tenga en cuenta que la seguridad de .NET concede el conjunto de permisos de Internet solo a código administrado que se ejecuta en sitios de confianza de Internet Explorer. Por lo tanto, los formularios con código administrado de InfoPath no se ejecutarán si se publican en un Sitio de confianza.
  
## <a name="merging-forms"></a>Combinar formularios

Puede deshabilitar la característica de combinación de formularios para evitar que los usuarios importen datos de varios formularios a un solo formulario.
  
Puede habilitar o deshabilitar la combinación de formularios mediante la casilla de verificación **Habilitar la combinación de formularios** en la sección **Avanzadas** del cuadro de diálogo **Opciones de formulario**, que está disponible desde la pestaña **Información** del Microsoft Office Backstage cuando se diseña el formulario. Cuando la combinación de formularios está deshabilitada, los usuarios no pueden hacer clic en **Combinar formularios** en la pestaña **Compartir** del Microsoft Office Backstage cuando rellenan el formulario. 
  
## <a name="submitting-forms"></a>Enviar formularios

Puede deshabilitar la función de envío de formularios para evitar que los usuarios envíen formularios.
  
Puede habilitar o deshabilitar el envío de formularios mediante el cuadro de diálogo **Opciones de envío**, que está disponible al hacer clic en **Opciones de envío** en el menú de pestañas **Datos** en modo de diseño. Cuando el envío de formularios está deshabilitado, los usuarios no pueden hacer clic en **Enviar** en la pestaña **Inicio** cuando rellenan el formulario. 
  

