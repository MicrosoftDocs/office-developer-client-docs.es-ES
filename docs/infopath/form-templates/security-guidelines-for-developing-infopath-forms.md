---
title: Directrices de seguridad para desarrollar formularios de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4690028e-20ac-297b-4651-801f5159c747
description: Antes de leer este tema, vea Conceptos de seguridad adicionales de los formularios de InfoPath para una comprensión general del modelo de seguridad de InfoPath.
ms.openlocfilehash: 3a72421882e655f34abd1eda30fe7e4fb42c45c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815982"
---
# <a name="security-guidelines-for-developing-infopath-forms"></a>Directrices de seguridad para desarrollar formularios de InfoPath

Antes de leer este tema, vea [Conceptos de seguridad adicionales de los formularios de InfoPath](additional-infopath-form-security-concepts.md) para una comprensión general del modelo de seguridad de InfoPath. 
  
## <a name="security-issues-for-users-of-infopath-forms"></a>Problemas de seguridad para usuarios de los formularios de InfoPath

Los problemas de seguridad principales para los usuarios de Microsoft InfoPath son similares a los de las aplicaciones web que se ejecutan en Internet Explorer. Sin embargo, debe tener en cuenta que el nivel de seguridad proporcionado a un formulario sólo depende de la ubicación de la plantilla de formulario y no de la ubicación donde los usuarios almacenan o abren los documentos XML resultantes que crean. Los usuarios podrán determinar la ubicación de la plantilla de formulario con la que trabajan visualizando la barra de estado de InfoPath.
  
InfoPath ayuda a proteger a los usuarios contra las siguientes posibles amenazas que representan las plantillas de formulario creadas de forma malintencionada:
  
- El potencial de divulgación de información confidencial del equipo local o de orígenes de datos remotos.
    
- El uso malintencionado de controles ActiveX.
    
- El uso malintencionado de propiedades y métodos del modelo de objetos de InfoPath.
    
## <a name="disclosure-of-sensitive-information"></a>Divulgación de información confidencial

El escenario de divulgación de información confidencial más común se puede presentar si un autor malintencionado de un formulario crea un formulario que use las credenciales de seguridad actuales del usuario para obtener acceso a un origen de datos distinto del de la implementación del formulario. Por ejemplo, un usuario malintencionado podría enviar un formulario de mensaje de correo electrónico o mediante una dirección URL a un formulario en un recurso compartido o servidor Web. El formulario podría contener un script que realice una solicitud de acceso a datos usando las credenciales del usuario actuales para recuperar datos de un origen de datos en otro dominio al que el usuario malintencionado no tendría acceso de otra manera, como una base de datos de nómina u otra información confidencial. Esta clase de escenarios de riesgo de seguridad se denomina acceso a datos entre dominios.
  
El modelo de seguridad de Internet Explorer en el que se basa InfoPath proporciona una configuración llamada **Tener acceso a origen de datos entre dominios** que, de forma predeterminada, deshabilita el acceso entre dominios a los formularios de InfoPath que residen en las zonas de seguridad de **Internet** y **Sitios restringidos**. Esta configuración también pide al usuario que permita o niegue el acceso entre dominios a los formularios de InfoPath que residen en la zona de seguridad de **Intranet local** y habilita el acceso entre dominios a los formularios de InfoPath que residen en las zonas **Sitios de confianza** o **Equipo local**. 
  
## <a name="malicious-use-of-activex-controls"></a>Uso malintencionado de controles ActiveX.

El escenario principal de uso malintencionado de controles ActiveX se presenta cuando un autor malintencionado de un formulario escribe código en un control ActiveX que obtiene acceso al sistema de archivos para recuperar archivos personales y listas de contraseñas, eliminar archivos o deshabilitar el sistema del usuario. Un formulario de InfoPath puede ejecutar código en los controles ActiveX de lógica empresarial o de un script que se ejecuta en un panel de tareas. InfoPath no permite que los scripts de las vistas de InfoPath ejecuten controles ActiveX.
  
El modelo de seguridad de Internet Explorer en el que se basa InfoPath proporciona una configuración llamada **Inicializar y generar scripts de controles ActiveX marcados como no seguros**. Esta configuración, de forma predeterminada, deshabilita la inicialización y el scripting de los controles ActiveX marcados como no seguros para los formularios de InfoPath que residen en las zonas de seguridad de **Intranet local**, **Internet** y **Sitios restringidos**. Le pide al usuario que permita o niegue el scripting de controles ActiveX marcados como no seguros para los formularios de InfoPath que residen en las zonas de seguridad de **Sitios de confianza** o de **Equipo local**, y habilita el scripting de controles ActiveX marcados como no seguros para formularios de InfoPath que sean de plena confianza. 
  
Tampoco podrá insertar un control ActiveX marcado como no seguro para inicializar o generar scripts en el panel de tareas de los controles en modo de diseño, independientemente de la zona de seguridad en que se encuentre o del nivel de confianza del formulario.
  
## <a name="malicious-use-of-infopath-object-model-code"></a>Uso malintencionado del código del modelo de objetos de InfoPath

De la misma manera, los métodos y propiedades de InfoPath llamados desde código pueden presentar diferentes niveles de riesgo. Por ejemplo, el método [SaveAs(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) de la clase [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) se puede usar para escribir datos en cualquier lugar del sistema de archivos. Para protegerse del uso malintencionado de estos miembros del modelo de objetos, el modelo de objetos de InfoPath implementa tres niveles de seguridad que determinan cómo y dónde se puede usar un miembro concreto del modelo de objeto. Para obtener más información acerca de esta característica, vea el tema [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md).
  
## <a name="best-practices-for-developers-of-infopath-forms"></a>Recomendaciones para los programadores de los formularios de InfoPath

Los programadores que crean formularios de InfoPath deberían saber cómo implementar las siguientes recomendaciones de seguridad:
  
- Cómo reconocer posibles problemas de seguridad en el archivo XML asociado con el formulario.
    
- Cómo evitar que se presenten mensajes de error confusos o molestos para los usuarios de formularios.
    
- Cómo firmar los archivos CAB de los controles ActiveX.
    
- Cómo firmar plantillas de formulario enviadas como datos adjuntos a un mensaje de correo electrónico.
    
## <a name="best-practices-for-xml-data-associated-with-a-form"></a>Recomendaciones para datos XML asociados con un formulario

Tenga en cuenta que los datos XML que alimentan los formularios de InfoPath pueden proceder de cualquier origen, incluso de aquellos en los que el usuario no necesariamente confía o controla. Por ejemplo, InfoPath puede obtener datos XML desde un vínculo a una página Web o desde un archivo adjunto de XML enviado al usuario en el mensaje de correo electrónico. Para mitigar estos riesgos, tenga en cuenta las siguientes recomendaciones:
  
- No pase datos que no sean de confianza, leídos del XML, a la función **eval()** de Microsoft JScript o a la propiedad **innerHTML** del panel de tareas. Ambas llamadas pueden usarse para ejecutar un script malintencionado. En un panel de tareas, use la propiedad **innerText** como alternativa. Tenga en cuenta que las vistas de InfoPath no pueden ejecutar un script. 
    
- Los datos enviados a una base de datos de un archivo XML pueden presentar riesgos de seguridad para la base de datos si no se validan antes del envío.
    
Los datos que no son validados antes de enviarse al origen de datos pueden dañar la integridad de los datos del origen de datos o, en casos más extremos, presentar la posibilidad de saturaciones del búfer. También puede ocasionar inyección de script o inyección de código SQL si intenta usar datos que no son de confianza directamente en su servidor.
  
## <a name="best-practices-to-avoid-presenting-confusing-error-messages"></a>Recomendaciones para evitar que se presenten mensajes de error confusos

 **Implemente los formularios y sus orígenes de datos en el mismo dominio**
  
La mayoría de los usuarios no comprende claramente el riesgo de seguridad de acceso a datos entre dominios. La implementación de formularios que constantemente advierten y piden al usuario el permiso de acceso a datos entre dominios tiene el efecto de que muchos usuarios se acostumbran a aprobar todas las solicitudes de acceso entre dominios o agregan el dominio de origen a su lista de **Sitios de confianza**, sin tomar en serio los riesgos de seguridad. Para evitar esta situación, implemente los formularios de InfoPath en el mismo servidor que los orígenes de datos de los que dependen. 
  
 **Evite usar controles ActiveX que no estén marcados como seguros para scripting**
  
Los controles ActiveX pueden exponer propiedades y métodos que se pueden usar para poner en peligro el sistema de un usuario, tales como métodos para obtener acceso al sistema de archivos de un equipo. Siempre que sea posible, solo debería usar controles ActiveX marcados como seguros para scripting. Éstos son controles sobre los que se han realizado pruebas para garantizar que no dañan el sistema de un usuario ni ponen en peligro la seguridad del usuario, independientemente de cómo un script de una página web manipule los métodos y propiedades del control. De la misma manera, al crear controles ActiveX para usar con InfoPath, inspeccione el código y pruebe el control ActiveX rigurosamente antes de marcarlo como seguro para scripting.
  
InfoPath usa un modelo de seguridad basado en las zonas de seguridad de Internet Explorer. Por lo tanto, un formulario de InfoPath usa los mismos permisos que Internet Explorer, lo que, de forma predeterminada, habilita las llamadas de script a controles ActiveX marcados como seguros para scripting, sin peticiones al usuario.
  
## <a name="best-practices-for-managing-the-cab-files-of-activex-controls"></a>Recomendaciones para administrar los archivos CAB de los controles ActiveX

Los controles ActiveX se pueden hospedar en plantillas de formulario diseñadas para el editor de InfoPath. Los archivos CAB para estos controles que todavía no se encuentran presentes en el equipo del usuario se deben incluir en el archivo (.xsn) de la plantilla de formulario. Los archivos CAB incluidos en las plantillas de formulario deben estar firmados digitalmente para que el archivo CAB se pueda instalar. InfoPath no instalará un archivo CAB sin firmar, independientemente del nivel de confianza de la zona de seguridad.
  
Para garantizar que la firma digital del archivo CAB se pueda comprobar, el archivo debería firmarse con un certificado que tenga una cadena de confianza que conduzca a un certificado raíz de confianza. De lo contrario, la firma no se podrá autenticar, se producirá un error al comprobar la firma y no se instalará el archivo CAB.
  
## <a name="best-practices-for-form-templates-sent-as-an-attachment-to-an-email-message"></a>Procedimientos recomendados para plantillas de formulario enviadas como datos adjuntos a un mensaje de correo electrónico

InfoPath admite la implementación de plantillas de formulario como datos adjuntos a un mensaje de correo electrónico y mover plantillas de formulario de una ubicación a otra. Es buena práctica de seguridad para firmar digitalmente una plantilla de formulario que diseñe y pretenda implementar como datos adjuntos a un mensaje de correo electrónico. Una firma digital en una plantilla de formulario implementada por mensaje de correo electrónico no sólo garantiza la autenticidad de la plantilla. También tiene el beneficio adicional de permitir que la plantilla de formulario se actualice automáticamente.
  
La plantilla de formulario se debería firmar con un certificado que tenga una cadena de confianza que conduzca a un certificado raíz de confianza. Si no se firma con un certificado de ese tipo, se producirá un error al comprobar la firma debido a que ésta no se podrá autenticar.
  
> [!NOTE]
> [!NOTA] Si una plantilla de formulario firmada solicita acceso a Dominio o Restringido, InfoPath no comprobará la firma excepto para determinar si InfoPath puede actualizar la plantilla automáticamente. 
  
Puede encontrar más información acerca de la implementación de correo electrónico en [niveles de seguridad, implementación por correo electrónico y plantillas de formulario remotas](security-levels-email-deployment-and-remote-form-templates.md).
  

