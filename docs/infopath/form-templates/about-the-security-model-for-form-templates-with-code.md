---
title: Acerca del modelo de seguridad de las plantillas de formulario con código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, security,code access security [InfoPath 2007],security [InfoPath 2007], security model for managed code,security [InfoPath 2007], levels,CAS [InfoPath 2007],InfoPath 2003-compatible form templates, security,permissions [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: Las plantillas de formulario con código administrado de InfoPath admiten los mismos niveles de seguridad que las secuencias de comandos que se ejecutan en las plantillas de formulario no administradas; también admiten funciones de seguridad adicionales para el acceso al código que se aplican al código administrado que se ejecuta en common language runtime (CLR) de .NET Framework.
ms.openlocfilehash: 97f0239a5bd6699b539ddaebf4d1d2ed7d1394db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436149"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Acerca del modelo de seguridad de las plantillas de formulario con código

Las plantillas de formulario con código administrado de InfoPath admiten los mismos niveles de seguridad que las secuencias de comandos que se ejecutan en las plantillas de formulario no administradas; también admiten funciones de seguridad adicionales para el acceso al código que se aplican al código administrado que se ejecuta en common language runtime (CLR) de .NET Framework.
  
## <a name="infopath-managed-object-model-security-levels"></a>Niveles de seguridad del modelo de objetos administrado de InfoPath

En la tabla siguiente, se describe la relación entre los niveles de seguridad para los miembros del modelo de objetos de secuencia de comandos y el conjunto de permisos correspondiente que se pide para cada nivel cuando el miembro del modelo de objetos se usa en una plantilla de formulario de código administrado.
  
|**Nivel de seguridad del modelo de objetos**|**Descripción**|**Conjunto de permisos exigido**|
|:-----|:-----|:-----|
|0  <br/> |Se puede tener acceso sin restricciones.  <br/> |Ninguno  <br/> |
|2  <br/> |Sólo pueden tener acceso los formularios que se ejecuten en el mismo dominio que el formulario abierto actualmente o los formularios a los que se haya concedido permisos entre dominios.  <br/> |Ninguno  <br/> |
|3  <br/> |Sólo pueden obtener acceso los formularios de plena confianza.  <br/> |FullTrust  <br/> |
   
> [!NOTE]
> El servidor COM de InfoPath actual no utiliza el nivel de seguridad "1", que se reserva para su uso futuro. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Aunque los niveles 0 y 2 del modelo de objetos no exigen ningún conjunto de permisos, porque contienen código administrado, se comportan tal como se definió para el nivel de seguridad de acceso al dominio que se describe en la sección siguiente. 
  
El nivel de seguridad de cada miembro del modelo de objetos que expone el ensamblado de interoperabilidad Microsoft.Office.InfoPath y Microsoft.Office.Interop.InfoPath.SemiTrust se especifica en la sección Comentarios del tema que documenta ese miembro del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) y [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="infopath-domain-access-security-levels"></a>Niveles de seguridad para el acceso al dominio de InfoPath

En combinación con los niveles de seguridad del modelo de objetos cuyo cumplimiento exige el servidor COM que expone la aplicación InfoPath, ésta define tres niveles de seguridad cuya aplicación depende de la ubicación de la plantilla de formulario, de cómo se haya implementado y de las opciones que se hayan configurado en el modo de diseño. Estos tres niveles de seguridad se definen en la tabla siguiente:
  
|**Nivel de seguridad de acceso al dominio**|**Descripción**|
|:-----|:-----|
|Restringido  <br/> |No permite la comunicación de la plantilla de formulario con el exterior. Este nivel de seguridad está concebido para impedir que los formularios dañinos transmitan datos desde su PC al atacante malintencionado. Cuando se ejecuta en este modo de seguridad, las siguientes características no funcionarán: Panel de tareas personalizado, Conexiones de datos (excepto envío de correo electrónico), controles ActiveX, código de formulario de código administrado, Roles y Flujo de trabajo. Las plantillas de formulario de código administrado no se pueden ejecutar en el dominio Restringido. Cuando una plantilla se configura como **Determinar automáticamente el nivel de seguridad** en la categoría **Seguridad y confianza** del cuadro de diálogo **Opciones de formulario**, siempre requerirá al menos el nivel de seguridad de acceso al dominio para ejecutar el código.  <br/><br/>**IMPORTANTE:** El ensamblado de código administrado creado para una plantilla de formulario de código administrado no se cargará y se ejecutará cuando se abra un formulario desde un dominio restringido, por ejemplo, desde un formulario de InfoPath enviado como datos adjuntos de correo electrónico. Cualquier plantilla de formulario que desee implementar como datos adjuntos de correo electrónico debe omitir las características enumeradas anteriormente y, si la plantilla de formulario contiene código de formulario, el código de formulario debe implementarse en JScript o VBScript y solo debe usar miembros del modelo de objetos con un nivel de seguridad de 0 (cero).           |
|Dominio  <br/> |Restringe un formulario basándose en su ubicación en una de las zonas de seguridad que define Microsoft Internet Explorer. Por ejemplo, si el formulario está ubicado en la zona Intranet local, se puede comunicar con otros datos dentro de su propio dominio pero no le está permitido recuperar datos de otros dominios. La ubicación en una zona de seguridad de Microsoft Internet Explorer también determina si se permite la ejecución de controles ActiveX marcados como no seguros para las secuencias de comandos.  <br/> |
|Plena confianza  <br/> |Permite ejecutar un formulario de plena confianza en el equipo en el que se va a utilizar. Este nivel de seguridad sólo se puede utilizar al trabajar con formularios firmados digitalmente con una firma que proceda de un emisor raíz que haya sido registrado como de confianza en el equipo, o bien creando un programa que instale el formulario y establezca el valor "sí" en el atributo **requireFullTrust** del elemento **xDocumentClass** en el archivo de definición del formulario (.xsf). Con esta configuración, el formulario puede obtener acceso a las llamadas al modelo de objetos que requieren el nivel de seguridad 3, como las propiedades y los métodos que tienen acceso al sistema de archivos; asímismo se pueden deshabilitar determinadas preguntas relacionadas con la seguridad que aparecen durante la ejecución en un nivel más restrictivo.<br/> |
   
De manera predeterminada, los formularios de InfoPath están configurados para seleccionar automáticamente el nivel de seguridad Restringido o Dominio según las funciones que utilice la plantilla de formulario y la forma y la ubicación en que se implemente la misma. Por ejemplo, una plantilla de formulario implementada como datos adjuntos de correo electrónico se configura automáticamente en el nivel de seguridad restringido. La configuración de seguridad es lo más restrictiva posible, empezando por Restringido, para garantizar un nivel de protección mayor para el usuario y sus datos. Cuando una plantilla de formulario que contiene código administrado se configura para seleccionar automáticamente el nivel de seguridad, siempre requerirá al menos el nivel de seguridad de acceso al dominio para ejecutar el código. Puede invalidar manualmente esta configuración en tiempo de diseño para seleccionar un nivel de seguridad más apropiado para el formulario mediante el siguiente procedimiento. 
  
### <a name="specify-a-forms-security-level"></a>Especificar el nivel de seguridad de un formulario

1. Abra el formulario en el diseñador de formularios de InfoPath, haga clic en la pestaña **Archivo**, haga clic en **Información** y, a continuación, haga clic en **Opciones de formulario**.
    
2. En el cuadro de diálogo **Opciones de formulario**, haga clic en la categoría **Seguridad y confianza**. 
    
3. Desactive la casilla de verificación **Determina automáticamente el nivel de seguridad (recomendado)**. 
    
4. Seleccione el nivel de seguridad deseado.
    
> [!NOTE] 
> - Si selecciona el nivel de seguridad **Restringido** para una plantilla de formulario con código administrado, el código que está detrás del formulario no se cargará ni se ejecutará, con independencia de los miembros del modelo de objetos que utilice. Este nivel de seguridad está diseñado principalmente para formularios de InfoPath que se implementan mediante correo electrónico.     
> - Si selecciona el nivel de seguridad **Plena confianza**, necesita firmar digitalmente el formulario o instalar y registrarlo. Para obtener más información, vea [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).
    
La tabla siguiente resume el modelo de seguridad de InfoPath. La primera columna contiene la lista de niveles requeridos o especificados para los formularios. La segunda y tercera columnas especifican si el formulario tiene un identificador URN o URL para su ubicación. Las columnas siguientes especifican lo que está permitido ejecutar. Para obtener más información sobre escenarios de implementación y conjuntos de permisos para las plantillas de formulario con código administrado, consulte la sección "Funciones de seguridad para el acceso al código de Common Language Runtime" de este tema.
  
|**Nivel que requiere el formulario**|**Tiene un identificador URN**|**Tiene un identificador URL**|**ActiveX marcado como no seguro para scripting**|**Acceso entre dominios**|**Código administrado**|**Seguridad del modelo de objetos**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Restricted  <br/> ||X  <br/> |Sin ActiveX  <br/> |Error  <br/> |El formulario se carga, pero no se ejecuta el código administrado  <br/> |0  <br/> |
|Dominio (zona de Internet Explorer **Sitios restringidos**)  <br/> |No se ejecutará  <br/> |No se ejecutará  <br/> |No se ejecutará  <br/> |No se ejecutará  <br/> |No se ejecutará  <br/> |No se ejecutará  <br/> |
|Dominio (zona de Internet Explorer **Internet**)  <br/> |X  <br/> ||Error  <br/> |Error  <br/> |No se ejecutará  <br/> |0  <br/> |
|Dominio (zona de Internet Explorer **Intranet local**)  <br/> |X  <br/> ||Error  <br/> |Prompt  <br/> |El código administrado se ejecuta con permisos de **Intranet local**.  <br/> |2  <br/> |
|Dominio (zona de **Sitios de confianza** de Internet Explorer)  <br/> |X  <br/> ||Prompt  <br/> |Aceptar  <br/> |El código administrado se ejecuta con permisos de **Internet**. Está permitido el acceso entre dominios. Tenga en cuenta que aunque el formulario se encuentre en la zona **Sitios de confianza**, se aplican los permisos de la zona **Internet**.<br/> |2  <br/> |
|Dominio (zona de **Equipo local** de Internet Explorer)  <br/> |X  <br/> |X  <br/> |Prompt  <br/> |Error  <br/> |El código administrado se ejecuta con permisos de **Intranet local**.  <br/> |2  <br/> |
|Plena confianza  <br/> |X  <br/> |X  <br/> |Aceptar  <br/> |Aceptar  <br/> |Plena confianza  <br/> |3  <br/> |
   
> [!IMPORTANT]
> Las descripciones anteriores de las columnas "ActiveX marcado como no seguro para las secuencias de comandos" y "Acceso entre dominios" suponen que la configuración de seguridad es la predeterminada para Microsoft Internet Explorer. Si un usuario modifica la configuración de seguridad, el comportamiento de InfoPath variará en consecuencia. Por ejemplo, si en la zona **Intranet local**, **Tener acceso a origen de datos entre dominios** está **Habilitado**, no se pedirá a los usuarios que permitan el acceso entre dominios tal como se describe en la tabla. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Funciones de seguridad para el acceso al código de Common Language Runtime

Al compilar una plantilla de formulario con código administrado de InfoPath, se crea un ensamblado privado que contiene la implementación de la lógica del código de formulario.
  
De manera predeterminada en .NET Framework, un ensamblado de código administrado tiene permisos de plena confianza cuando se ejecuta en un equipo local y no los tiene cuando se ejecuta en la Intranet. Para ofrecer un control más fino en la directiva de seguridad y la opción de ejecutar plantillas de formulario con código administrado de InfoPath como plantillas de plena confianza desde la Intranet, InfoPath implementa la siguiente arquitectura de seguridad.
  
- La aplicación InfoPath hospeda Common Language Runtime (CLR) de .NET Framework.
    
- Dentro del CLR que hospeda InfoPath, cada plantilla de formulario con código administrado se ejecuta en un dominio de aplicación separado, que es un entorno que proporciona aislamiento, descargas y límites de seguridad para la ejecución de código administrado.
    
- InfoPath establece, en el dominio de la aplicación, una directiva de seguridad predeterminada que depende del nivel de confianza asociado a la plantilla de formulario y la dirección URL de su ubicación.
    
- De manera predeterminada, una plantilla de código administrado que se ejecuta en un equipo local (el grupo de código de la zona Mi equipo) obtiene un nivel de permisos menor que plena confianza (permisos de la zona Intranet local). Para tener permisos de plena confianza, el formulario se debe registrar o estar firmado digitalmente con un certificado de confianza.
    
La directiva de seguridad predeterminada que se establece para el dominio de la aplicación de una plantilla de formulario con código administrado garantiza que se cumplan los niveles de seguridad para el acceso al dominio de InfoPath, además de cualquier otra restricción de seguridad adicional de .NET. Para ofrecer más flexibilidad, el sistema de seguridad de InfoPath reconoce un grupo de código de seguridad para el acceso al código de .NET denominado "Plantillas de formulario de InfoPath". Si este grupo de código está presente en el equipo de un usuario, su configuración de seguridad, así como las de los grupos de código secundarios que pueda ver dentro del mismo, se aplica al dominio de la aplicación.
  
> [!IMPORTANT] 
> - El grupo de código Plantillas de formulario de InfoPath se aplica sólo al propio ensamblado de código de formulario de código administrado. En consecuencia, si concede el permiso de plena confianza establecido en el código de formulario de código administrado de InfoPath, pero no ha instalado y registrado (o firmado digitalmente) la propia plantilla de formulario (que convierte toda la plantilla de formulario en un elemento de plena confianza), seguirán produciendo error las llamadas en el código de formulario para miembros de modelo de objeto de nivel de seguridad 3.   
> - Si hace referencia o carga explícitamente (Assembly.Load) un ensamblado que está configurado con un permiso restringido establecido con prueba de Hash, Nombre seguro o Editor para determinar su condición de miembro en un proyecto de plantilla de formulario, el ensamblado será no obstante cargado y ejecutado por la plantilla de formulario.
    
Para obtener información sobre cómo crear y configurar el grupo de código Plantillas de formulario de InfoPath, [vea Configure Security Configuración for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).
  
En la tabla siguiente se resumen los escenarios de implementación y los conjuntos de permisos que se aplican a la plantillas de formulario con código administrado.
  
|**Escenario de implementación**|**Conjunto de permisos**|**Notas**|
|:-----|:-----|:-----|
|La plantilla de formulario está publicada en el equipo local y el programador está utilizando Visual Studio para escribir y depurar el código del formulario.  <br/> |Conjunto de permisos Intranet local.  <br/> Ensamblados instalados en la Caché de ensamblados global (GAC) y marcada con el atributo **AllowPartiallyTrustedCallersAttribute** tienen el conjunto de permisos de plena confianza.  <br/> |De manera predeterminada, no se concede el conjunto de permisos Plena confianza a las plantillas de formulario que se ejecutan desde el equipo local. Al desarrollar plantillas de formulario que usan características y llamadas a miembros del modelo de objetos que requieren permisos de plena confianza, puede usar el procedimiento descrito en Vista previa y Depurar plantillas de formulario que requieren [plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md).  <br/> |
|La plantilla de formulario se publica en el equipo local y hace referencia a un ensamblado personalizado que solicita el conjunto de permisos Plena confianza en el equipo local.  <br/> |Conjunto de permisos Intranet local.  <br/> Ensamblados instalados en la Caché de ensamblados global (GAC) y marcada con el atributo **AllowPartiallyTrustedCallersAttribute** tienen el conjunto de permisos de plena confianza. El ensamblado personalizado tiene el conjunto de permisos de Intranet local.<br/> |Para hacer referencia a ensamblados externos y utilizarlos en el código de una plantilla de formulario, el programador debe utilizar el grupo de código Plantillas de formulario de InfoPath si desea conceder el conjunto de permisos Plena confianza (o el que corresponda) al ensamblado externo al que se hace referencia en el código de la plantilla de formulario. InfoPath no confía en ningún ensamblado externo que no esté instalado en la Caché de ensamblados global (GAC). El programador debe conceder explícitamente los permisos necesarios al ensamblado usando el grupo de código Plantillas de formulario de InfoPath, incluso si el ensamblado ya es de confianza según los permisos que se le han concedido en el grupo de código de la zona Mi equipo.  <br/> |
|La plantilla de formulario se publica en una ubicación compartida de la intranet local, como un recurso compartido de archivos, una biblioteca de formularios de SharePoint o un servidor Web.  <br/> |Conjunto de permisos Intranet local.  <br/> Ensamblados instalados en la Caché de ensamblados global (GAC) y marcada con el atributo **AllowPartiallyTrustedCallersAttribute** tienen el conjunto de permisos de plena confianza.  <br/> ||
|La plantilla de formulario se publica en una ubicación compartida de la intranet local, como un recurso compartido de archivos, una biblioteca de formularios de SharePoint o un servidor web que esté designado como sitio de confianza en Internet Explorer.  <br/> |Conjunto de permisos Internet.  <br/> Se concede el conjunto de permisos Plena confianza a los ensamblados firmados por Microsoft y ECMA.  <br/> |La seguridad para el acceso al código CLR sólo concede el conjunto de permisos Internet a los sitios designados como de confianza en Internet Explorer. InfoPath respeta esta directiva. Observe que éste no es el caso de las plantillas de formulario de InfoPath que utilizan secuencias de comandos en el código del formulario, ya que éstas reciben un nivel de permisos superior al publicarse en la zona Sitios de confianza.  <br/> |
|La plantilla de formulario se descarga o copia desde una ubicación de Internet.  <br/> |De manera predeterminada, ninguno. El ensamblado de código administrado de la plantilla de formulario no se carga ni se ejecuta.  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Configurar la seguridad Configuración plantillas de formulario con código](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Obtener una vista previa y depurar plantillas de formulario con código que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

