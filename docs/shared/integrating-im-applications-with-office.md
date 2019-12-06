---
title: Integración de aplicaciones de mensajería instantánea con Office
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artículo describe cómo configurar una aplicación cliente de mensajería instantánea (MI) para que se integre con las características sociales de Office 2013 y siguientes, como mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contactos.
localization_priority: Priority
ms.openlocfilehash: c0094b880bae5cac2cef4236d3ff3edcefd21678
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819297"
---
# <a name="integrating-im-applications-with-office"></a>Integración de aplicaciones de mensajería instantánea con Office

Este artículo describe cómo configurar una aplicación cliente de mensajería instantánea (MI) para que se integre con las características sociales de Office 2013, Office 2016, Office 2019, y Office 365 como mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contactos.
  
## <a name="introduction"></a>Introducción
<a name="off15_IMIntegration_Intro"> </a>

Office 2013 (y siguientes) ofrece una completa integración con aplicaciones cliente de MI, incluidos Lync 2013 y Teams. Esta integración proporciona a los usuarios capacidades de MI desde dentro de Word, Excel, PowerPoint, Outlook, Visio, Project y OneNote, así como la integración de presencia en las páginas de SharePoint. Los usuarios pueden ver la foto, el nombre, el estado de presencia y los datos de contacto de los usuarios de su lista de contactos. Pueden iniciar una sesión de MI, realizar una videollamada o una llamada telefónica directamente desde la tarjeta de contactos (el elemento de la IU en Office que expone opciones de información de contacto y comunicación). Office te permite mantenerte conectado a tus contactos sin tener que salir de tus correos o documentos. 
  
> [!NOTE]
> Este artículo usa el término aplicación cliente de MI para hacer referencia específicamente para la aplicación instalada en el equipo de un usuario que se comunica con el servicio de MI. Por ejemplo, Lync 2013 y Teams se consideran aplicaciones cliente de MI. Este artículo no proporciona detalles acerca de cómo se comunica la aplicación cliente de MI con el servicio de MI o acerca del servicio de MI en sí mismo. 
  
Puedes personalizar una aplicación cliente de MI para que se comunique con Office. En concreto, puedes modificar la aplicación de MI para que muestre la siguiente información dentro de la IU de Office:
  
- Foto del contacto.
    
- Nombre de contacto.
    
- Nota de estado personal del contacto.
    
- Estado de presencia del contacto.
    
- Cadena de disponibilidad del contacto (por ejemplo, "Disponible" o "Fuera de la oficina").
    
- Cadena de función del contacto (por ejemplo, "listo para video").
    
- Inicio de MI con un solo clic.
    
- Inicio de videollamada con un solo clic.
    
- Inicio de llamada de teléfono con un solo clic (incluye SIP, número de teléfono, correo de voz y llamada a un número nuevo).
    
- Administración de contactos (agregar al grupo de MI).
    
- Ubicación y zona horaria del contacto.
    
- Datos, número de teléfono, dirección de correo, puesto y nombre de la compañía del contacto.
    
**Ilustración 1. Tarjeta de contactos en Office 2013**

![Tarjeta de personas en Office 2013](media/ocom15_peoplecard.png "Tarjeta de personas en Office 2013")
  
Para habilitar la integración con Office, una aplicación cliente de MI debe implementar un conjunto de interfaces de conexión que proporciona Office. Se incluyen las API para esta integración en el espacio de nombre [UCCollborationLib](https://docs.microsoft.com/previous-versions/office/communications/ff398475(v=ocs.14)) contenido en el archivo Microsoft.Office.UC.dll, que se instala con las versiones de Office 2013 que incluyen Lync o Skype for Business. El espacio de nombre **UCCollaborationLib** incluye las interfaces que debes implementar para la integración con Office. 
  
> [!IMPORTANT] 
> La biblioteca de tipos para las interfaces necesarias está incrustada en Lync 2013 o Skype for Business. Para integradores de terceros, esto solo funciona cuando los equipos de destino tienen instalado Lync 2013 y en Skype for Business. Si realizas la integración con Office Standard, deberás extraer la biblioteca de tipos e instalarla en el equipo de destino. El [SDK de Lync 2013](https://www.microsoft.com/download/details.aspx?id=36824) incluye el archivo Microsoft.Office.UC.dll. 
  
> [!NOTE]
>  Algunas aplicaciones de Office 2010 puede integrarse de forma similar con una aplicación de proveedores de MI de terceros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 y SharePoint Server 2010 (con un control ActiveX). Muchos de los pasos necesarios para la integración con Office 2013 se aplican también a Office 2010. Hay varias diferencias clave en la forma en la que Office 2010 se integra con una aplicación de proveedor de MI: 
>  - Office 2010 no muestra la foto del contacto. 
>  - Debes descargar el archivo Microsoft.Office.Uc.dll por separado de Office 2010. El [SDK de Lync 2010](https://www.microsoft.com/en-us/download/details.aspx?id=18898) incluye el archivo Microsoft.Office.UC.dll para Office 2010. 
>  - Cuando la aplicación de Office llama al método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) en la aplicación cliente de MI, pasa la cadena "14.0.0.0". 
>  - Office 2010 enumera todos los grupos y contactos en cuanto se conecta a una aplicación cliente de MI. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>Integración de Office con una aplicación cliente de MI
<a name="off15_IMIntegration_How"> </a>

Cuando se inicia una aplicación de Office 2013 (y siguientes), atraviesa el siguiente proceso para integrarse con la aplicación cliente de MI predeterminada:
  
1. Comprueba el registro para descubrir la aplicación cliente de MI predeterminada y, a continuación, se conecta a ella.
    
2. Se autentica con la aplicación cliente de MI.
    
3. Se conecta a interfaces específicas expuestas por la aplicación cliente de MI.
    
4. Determina las funciones del usuario que inició sesión actualmente (usuario local), incluida la obtención de los contactos del usuario, la determinación de la presencia del usuario y la determinación de las capacidades de MI del usuario (mensajería instantánea, chat de video, VOIP, etc.).
    
5. Obtiene la información de presencia de los contactos del usuario local.
    
6. Cuando se cierra la aplicación cliente de MI, la aplicación de Office se desconecta de forma silenciosa.
    
### <a name="discovering-the-im-application"></a>Descubrir la aplicación de MI

La aplicación de Office busca varias teclas y entradas específicas en el registro para obtener información sobre la aplicación cliente de MI de forma predeterminada. Si detecta una aplicación cliente de MI de forma predeterminada, a continuación, intenta conectarse a ella.
  
El proceso que realiza la aplicación de Office para obtener información sobre la aplicación cliente de MI predeterminada es la siguiente:
  
1. La aplicación de Office intenta ver si se establece la subclave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp en el registro y lee el nombre de aplicación que aparece allí.
    
2. La aplicación de Office, a continuación, lee la clave HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning y controla el valor para detectar cambios.
    
3. La aplicación de Office a continuación lee la clave del registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ y obtiene los valores de ProcessName e identificador de clase (CLSID) almacenados allí. 
    
4. Una vez que la aplicación cliente de MI completó correctamente su secuencia de inicio y registró todas las clases correctamente para la integración de presencia, establece la clave HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning en "2", lo que indica que se está ejecutando la aplicación cliente.
    
5. Cuando la aplicación de Office detecta que la clave de HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning se estableció en "2", comprueba la lista de procesos en ejecución en el equipo para ver el nombre de la aplicación cliente de MI.
    
6. Una vez que la aplicación de Office encuentra el proceso que utiliza la aplicación cliente de MI, la aplicación de Office llama a **CoCreateInstance** mediante CLSID para establecer una conexión con la aplicación cliente de MI como servidor COM fuera del proceso. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Autenticación de la conexión a la aplicación de MI

Después de que la aplicación de Office establece una conexión con la aplicación cliente de MI, a continuación, hace lo siguiente:
  
1. La aplicación de Office llama al método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para comprobar la interfaz [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). 
    
2. La aplicación de Office, a continuación, llama al método **IUCOfficeIntegration.GetAuthenticationInfo**, pasando la versión más alta de integración compatible (por ejemplo, "15.0.0.0"). 
    
3. Si la aplicación cliente de MI es compatible con la versión de Office que se pasa como un parámetro, la aplicación devuelve la siguiente cadena XML codificada de forma rígida al código de llamada:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > Por motivos heredados, la aplicación cliente de MI debe devolver el valor exacto `<authenticationinfo>` a la llamada a **GetAuthenticationInfo** si se admite la versión de Office pasado como un parámetro. 
  
4. Si la aplicación cliente no puede devolver un valor, la aplicación de Office llama al método **GetAuthenticationInfo** nuevamente con la siguiente versión más alta compatible de Office (por ejemplo, "14.0.0.0"). 
    
5. Cuando Office determina que la aplicación cliente de MI es compatible con la integración de presencia y MI, se conecta a un conjunto requerido de interfaces para finalizar la inicialización. (Para obtener más información, consulta [Conectarse a interfaces necesarias](#off15_IMIntegration_HowConnect).)
    
Si la aplicación de Office, produce un error en cualquiera de los pasos anteriores, retrocede y no se establece la integración de presencia durante la sesión de la aplicación de Office. 
  
### <a name="connecting-to-required-interfaces"></a>Conexión a las interfaces necesarias
<a name="off15_IMIntegration_HowConnect"> </a>

Después de autenticar la conexión a la aplicación cliente de MI, la aplicación de Office intenta conectarse a un conjunto de interfaces necesarias que debe exponer la aplicación cliente de MI. La aplicación de Office lo logra de la siguiente manera:
  
- La aplicación de Office obtiene un objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) al llamar al método **IUCOfficeIntegration.GetInterface**, pasando la constante **oiInterfaceLyncClient** desde la enumeración [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). 
    
- La aplicación de Office obtiene un objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) al llamar al método **IUCOfficeIntegration.GetInterface**, pasando la constante **oiInterfaceAutomation** desde la enumeración **OIInterface**. 
    
- La aplicación de Office configura la escucha de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). 
    
- La aplicación de Office, configura la escucha de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). 
    
- La aplicación de Office obtiene el estado de inicio de sesión de la aplicación cliente de MI mediante el acceso a la propiedad **ILyncClient.State**. 
    
- La aplicación de Office obtiene las capacidades de la aplicación cliente de MI al llamar al método **IUCOfficeIntegration.GetSupportedFeatures**, que devuelve una marca de la enumeración [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). 
    
- La aplicación de Office, obtiene acceso a la propiedad **ILyncClient.Self** para obtener una referencia a un objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf). 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Recuperar las capacidades del usuario local
<a name="off15_IMIntegration_HowConnect"> </a>

La aplicación de Office obtiene las capacidades del usuario local mediante el siguiente procedimiento:
  
1. Si la aplicación cliente de MI es compatible con la interfaz **IClient2**, Office intenta obtener un objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) mediante el acceso a la propiedad **IClient2.PrivateContactManager**. 
    
2. Si la aplicación de MI no es compatible con la interfaz **IClient2**, la aplicación de Office intenta obtener un objeto **IContactManager** mediante el acceso a la propiedad **ILyncClient.ContactManager**. La aplicación cliente de MI debe devolver correctamente un objeto **IContactManager** antes de que se puedan establecer otras capacidades de MI. 
    
3. La aplicación de Office, obtiene acceso a la propiedad **ILyncClient.Uri** y después llama a **IContactManager.GetContactByUri** para obtener el objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) asociado con el usuario local. 
    
4. A continuación, la aplicación de Office hace varias llamadas a **IContact.CanStart** para establecer las capacidades del usuario local, al pasar los valores de **ModalityTypes.ucModalityInstantMessage** y ** ModalityTypes.ucModalityAudioVideo** sucesivamente. 
    
### <a name="retrieving-contact-presence"></a>Recuperar presencia de contactos
<a name="off15_IMIntegration_HowConnect"> </a>

La aplicación de Office obtiene la presencia de contactos, incluido el usuario local, mediante el siguiente procedimiento: 
  
1. La aplicación de Office llama a **IContact.GetContactInformation** para obtener un elemento de presencia del contacto. 
    
2. A continuación, la aplicación de Office se suscribe a los cambios de estado de presencia del contacto. Llama a **IContactManager.CreateSubscription** para obtener un objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription). A continuación, llama a **IContactSubscription.AddContact** para agregar el contacto a la suscripción y luego llama a **IContactSubscription.Subscribe** para obtener los cambios de estado del contacto. 
    
3. Si la aplicación de MI es compatible con **IContact2**, Office intenta obtener información de presencia llamando a **IContact2.BatchGetContactInformation2**.
    
4. A continuación, la aplicación de Office recupera las propiedades de la presencia del contacto llamando a **IContact.BatchGetContactInformation**. La aplicación de Office puede obtener un segundo conjunto de propiedades de presencia si obtiene acceso a la propiedad **IContact.Settings**. 
    
5. Por último, la aplicación de Office obtiene la pertenencia del grupo del contacto al acceder a la propiedad **IContact.CustomGroups**. Esto le devuelve una colección [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que incluye a todos los objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) a los que pertenece el contacto. 
    
### <a name="disconnecting-from-the-im-application"></a>Desconexión de la aplicación de MI
<a name="off15_IMIntegration_HowConnect"> </a>

Cuando la aplicación de Office detecta el evento **OnShuttingDown** desde la aplicación de MI, se desconecta silenciosamente. Sin embargo, si cierra la aplicación de Office antes de la aplicación de MI, la aplicación de Office no garantiza que la conexión se limpie. La aplicación de MI debe controlar pérdidas de conexión del cliente. 
  
## <a name="setting-registry-keys-and-entries"></a>Entradas y claves del registro de configuración
<a name="off15_IMIntegration_SetRegistry"> </a>

Como se indicó anteriormente, las aplicaciones de Office compatibles con MI buscan teclas, entradas y valores específicos en el registro para obtener información sobre la aplicación cliente de MI a la cual conectarse. Estos valores de registro le proporcionan a la aplicación de Office el nombre del proceso y CLSID de la clase que actúa como punto de entrada al modelo de objeto de la aplicación cliente de MI (es decir, la clase que implementa la interfaz **IUCOfficeIntegration**). La aplicación de Office crea conjuntamente la clase y se conecta como cliente al servidor COM fuera de proceso en la aplicación cliente de MI. 
  
Usa la tabla 1 para identificar las claves, entradas y valores que deben escribirse en el registro para integrar una aplicación cliente de MI con Office.
  
**Tabla 1. Claves del registro para configurar la aplicación cliente de MI predeterminada**

|**Clave**|**Entrada**|**Tipo**|**Valor**|**Ejemplo**|
|:-----|:-----|:-----|:-----|:-----|
|HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |El nombre de la aplicación cliente de MI de terceros.  <br/> |MI de Litware 2012  <br/> |
||ProcessName  <br/> |REG_SZ  <br/> |El nombre del proceso de la aplicación cliente de MI de terceros.  <br/> |litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Un identificador de clase (CLSID) para la clase de creación conjunta de raíz en la aplicación de MI (la clase que implementa la interfaz **IUCOfficeIntegration**).  <br/> |(Un GUID)  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |El nombre de la aplicación cliente de MI. Debe ser el mismo que el nombre de la clave del registro de nivel superior (subárbol) en HKEY_LOCAL_MACHINE.  <br/> |Litware  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers\\<Application name\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Valor entero entre 0 y 2:  <br/>  0—No en ejecución  <br/>  1—Iniciándose  <br/>  2—En ejecución  <br/> <br/>**NOTA**: la clave del registro de nombre de aplicación debe ser igual al valor de la entrada DefaultIMApp.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Implementar las interfaces necesarias para la integración con Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Hay tres interfaces del espacio de nombre **UCCollaborationLib** que debe implementar el archivo ejecutable (o servidor COM) de una aplicación cliente de MI para que se pueda integrar con Office. Si no se implementan estas interfaces, la aplicación de Office retrocede durante el proceso de inicialización y no se establece la conexión con la aplicación cliente de MI. 
  
Las interfaces necesarias son las siguientes:
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). Si bien no es necesaria, la interfaz **_IUCOfficeIntegrationEvents** también debe implementarse en la misma clase derivada. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). Si bien no es necesaria, la interfaz **_ILyncClientEvents** también debe implementarse en la misma clase derivada. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>Interfaz IUCOfficeIntegration
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

La interfaz **IUCOfficeIntegration** proporciona el punto de entrada para que una aplicación de Office se conecte a la aplicación cliente de MI. La interfaz define tres métodos que una aplicación de Office llama como parte del proceso de iniciar una conexión con la aplicación cliente de MI. La clase que implementa la interfaz **IUCOfficeIntegration** se debe poder cocrear para que Office pueda cocrear una instancia de ella. Además, debe exponer la CLSID que se introduce como el valor de la entrada de GUID en la clave de registro HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ 
  
La clase que hereda de **IUCOfficeIntegration** también debe implementar la interfaz **_IUCOfficeIntegrationEvents**. La interfaz **_IUCOfficeIntegrationEvents** contiene los miembros que exponen los controladores de eventos de la interfaz **IUCOfficeIntegration**. 
  
La Tabla 2 muestra los miembros que deben implementarse en la clase que hereda de **IUCOfficeIntegration** y **_IUCOfficeIntegration**.
  
> [!NOTE]
> Para más información sobre las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegrationEvents** y sus miembros, consulta [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) y [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**Tabla 2. Implementación de las interfaces IUCOfficeIntegration y _IUCOfficeIntegrationEvents interfaces**

|**Interfaz**|**Miembro**|**Descripción**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |Método **GetAuthenticationInfo**  <br/> |Obtiene la cadena de información de autenticación.  <br/> |
||Método **GetInterface**  <br/> |Obtiene la interfaz de una versión específica.  <br/> |
||Método **GetSupportedFeatures**  <br/> |Obtiene las características de integración de Office compatibles.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |Evento **OnShuttingDown**  <br/> |El evento que se produce cuando la aplicación cliente de MI está intentando cerrarse.  <br/> |
   
Usa el código siguiente para definir una clase que herede de las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegration** dentro de una aplicación cliente de MI. 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

El método **GetAuthenticationInfo** toma una cadena como argumento para el parámetro _version_. Cuando la aplicación de Office llama a este método, pasa una de las dos cadenas del argumento, según la versión de Office. Cuando la aplicación de Office proporciona el método con la versión de Office compatible con la aplicación cliente de MI (es decir, compatible con la funcionalidad), el método **GetAuthenticationInfo** devuelve una cadena XML codificada de forma rígida `<authenticationinfo>`. 
  
Usa el código siguiente para implementar un método **GetAuthentication** dentro del código de la aplicación cliente de MI. 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

El método **GetInterface** envía las referencias a clases al código de llamada, dependiendo de lo que se pasa como argumento para el parámetro de la _interface_. Cuando una aplicación de Office llama al método **GetInterface**, pasa uno de los dos valores para el parámetro de la interfaz: la constante **oiInterfaceILyncClient** (1) o ** la constante oiInterfaceIAutomation** (2) de la enumeración [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface). Si la aplicación de Office pasa la constante **oiInterfaceILyncClient**, el método **GetInterface** devuelve una referencia a una clase que implementa la interfaz **ILyncClient**. Si la aplicación de Office pasa la constante **oiInterfaceIAutomation**, el método **GetInterface** devuelve una clase que implementa la interfaz **IAutomation**. 
  
Usa el siguiente código de ejemplo para implementar el método **GetInterface** dentro del código de la aplicación cliente de MI. 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

El método **GetSupportedFeatures** devuelve información sobre las características de MI compatibles con la aplicación cliente de MI. Es necesaria una cadena para el único parámetro, _version_. Cuando la aplicación de Office llama al método **GetSupportedFeatures**, el método devuelve un valor de la enumeración [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature). El valor devuelto especifica las capacidades del cliente de MI, donde cada función de la aplicación cliente de MI se indica en la aplicación de Office mediante la adición de un marcador al valor. 
  
> [!NOTE]
>  Las aplicaciones de Office 2013 (y siguientes) ignoran las siguientes constantes en la enumeración**OIFeature**: 
> - **oiFeaturePictures** (2) 
> - **oiFeatureFreeBusyIntegration**
> - **oiFeaturePhoneNormalization**
  
Usa el siguiente código de ejemplo para implementar el método **GetSupportFeatures** dentro del código de la aplicación cliente de MI. 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a>Interfaz ILyncClient
<a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a>

La interfaz **ILyncClient** se aplica a las funcionalidades de la aplicación cliente de MI. Expone propiedades que hacen referencia a la persona que inició sesión en la aplicación (usuario local, representado por la interfaz [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), el estado de la aplicación, la lista de contactos del usuario local y otras configuraciones. Cuando está intentando conectarse a la aplicación cliente de MI, la aplicación de Office obtiene una referencia a un objeto que implementa la interfaz **ILyncClient**. Desde esa referencia, Office puede acceder a muchas de las funciones de la aplicación cliente de MI. 
  
Además, la clase que implementa la interfaz **ILyncClient** también debe implementar la interfaz **_ILyncClientEvents**. La interfaz **_ILyncClientEvents** expone muchos de los eventos que son necesarios para supervisar el estado de la aplicación cliente de MI. 
  
La Tabla 3 muestra los miembros que deben implementarse en la clase que hereda de **ILyncClient** y **_ILyncClientEvents**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **ILyncClient** o ** \_ILyncClientEvents** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E\_NOTIMPL**. 
> 
> Para más información sobre las interfaces **ILyncClient** y **_ILyncClientEvents** y sus miembros, consulta [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) y [ UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**Tabla 3. Implementación de interfaces ILyncClient e ILyncClientEvents**

|**Interfaz**|**Miembro**|**Descripción**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |Propiedad **ContactManager**  <br/> |Obtiene el administrador de grupo de contactos.  <br/> |
||Propiedad **ConversationManager**  <br/> |Obtiene el administrador de conversación.  <br/> |
||Propiedad **Self**  <br/> |Obtiene el objeto **Self**.  <br/> |
||Método **SignIn**  <br/> |Inicia el proceso de inicio de sesión de la aplicación cliente de MI con una disponibilidad específica.  <br/> |
||Propiedad **State**  <br/> |Obtiene el estado actual de la plataforma.  <br/> |
||Propiedad **Uri**  <br/> |Obtiene el URI de la aplicación cliente de MI.  <br/> |
|**_ILyncClientEvents** <br/> |Evento **OnStateChanged**  <br/> |Se produce cuando cambia el estado de la aplicación cliente de MI. Debes controlar este evento y obtener la propiedad **eventData.NewState**. Se produce el evento para todos los procesos vinculados a una instancia de una aplicación cliente de MI cuando cualquier subsistema de la aplicación hace que cambie el estado.  <br/> |
   
Durante el proceso de inicialización, Office obtiene acceso a la propiedad **ILyncClient.State**. Esta propiedad debe devolver un valor de la enumeración [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState). 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

La propiedad **State** almacena el estado actual de la aplicación cliente de MI. Se debe establecer y actualizar durante la sesión de la aplicación cliente de MI. Cuando la aplicación cliente de MI inicia sesión, cierra sesión o se apaga, debe establecer la propiedad **State**. Es mejor establecer esta propiedad dentro de los métodos **ILyncClient.SignIn** y **ILyncClient.SignOut**, como demuestra el siguiente ejemplo. 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

En el siguiente ejemplo de código se muestra cómo configurar la escucha de eventos con las interfaces _ **ILyncClientEvents** y _ **IUCOfficeIntegrationEvents**. 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a>Interfaz IAutomation
<a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a>

La interfaz **IAutomation** automatiza características de la aplicación cliente de MI. Puedes usarla para iniciar conversaciones, unirte a conferencias y proporcionar contexto de la ventana de extensibilidad. 
  
La Tabla 4 muestra los miembros que deben implementarse en la clase que hereda de **IAutomation**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **IAutomation**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**. 
> 
> Para más información sobre la interfaz **IAutomation** y sus miembros, consulta [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**Tabla 4. Implementación de interfaz IAutomation**

|**Miembro**|**Descripción**|
|:-----|:-----|
|Método **StartConversation**  <br/> |Inicia una conversación con la modalidad de conversación especificada. Se devuelve una instancia de **IConversationWindow**.  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Implementar la integración de presencia de los contactos
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

Además de las tres interfaces necesarias descritas anteriormente, hay varias otras interfaces que son importantes para habilitar la funcionalidad de presencia de los contactos en Office. Entre ellas se incluyen las siguientes:
  
- La interfaz de [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) o **IContact2**. 
    
- La interfaz [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf). 
    
- Las interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) y [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager). 
    
- Las interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) y [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup). 
    
- La interfaz [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription). 
    
- La interfaz [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint). 
    
- La interfaz [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) 
    
### <a name="icontact-interface"></a>Interfaz IContact
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

La interfaz **IContact** representa un usuario de una aplicación cliente de MI. La interfaz expone propiedades de presencia, modalidades disponibles, pertenencia a un grupo y tipo de contacto para un usuario. Para iniciar una conversación con otro usuario, necesitas especificar esa instancia de usuario de **IContact**.
  
La Tabla 5 muestra los miembros que deben implementarse en la clase que hereda de **IContact**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **IContact**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**. 
>
> Para más información sobre la interfaz **IContact** y sus miembros, consulta [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**Tabla 5. Implementación de interfaz IContact**

|**Miembro**|**Descripción**|
|:-----|:-----|
|Método **CanStart**  <br/> |Devuelve **true** si se puede iniciar un determinado tipo de modalidad en el contacto.  <br/> |
|Método **GetContactInformation**  <br/> |Obtiene un elemento de la presencia de un contacto de publicación.  <br/> |
|Método **BatchGetContactInformation**  <br/> |Obtiene un elemento de presencia de un contacto de publicación.  <br/> |
|Propiedad **Configuración**  <br/> |Obtiene una colección de propiedades del contacto.  <br/> |
|Propiedad **CustomGroups**  <br/> |Obtiene una colección de grupos de los que el contacto es miembro.  <br/> |
   
Durante el proceso de inicialización, la aplicación de Office llama al método **IContact.CanStart** para determinar las funcionalidades de MI para el usuario local. El método **CanStart** toma una marca de la enumeración [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como argumento para el parámetro __modalityTypes_. Si el usuario actual puede participar en la modalidad solicitada (es decir, el usuario puede utilizar mensajería instantánea, mensajes de audio y video y uso compartido de aplicaciones), el método **CanStart** devuelve **true**.
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

El método **GetContactInformation** recupera información sobre el contacto del objeto **IContact**. El código de llamada debe pasar un valor de la enumeración [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para el parámetro __contactInformationType_, que indica los datos que se deben recuperar. 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

Similar al método **GetContactInformation**, el método **BatchGetContactInformation** recupera varios elementos de presencia sobre el contacto del objeto **IContact**. El código de llamada debe pasar de una matriz de valores de la enumeración **ContactInformationType** para el parámetro __contactInformationTypes_. El método devuelve un objeto [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contiene los datos solicitados. 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

La propiedad **IContact.Settings** devuelve un objeto **IContactSettingDictionary** que contiene las propiedades personalizadas sobre el contacto. 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

La propiedad **IContact.CustomGroups** devuelve un objeto **IGroupCollection** que incluye todos los grupos de los que el contacto es miembro. 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a>Interfaz ISelf
<a name="off15_IMIntegration_ImplementRequired_ISelf"> </a>

Durante el proceso de inicialización, la aplicación de Office obtiene los datos del usuario actual al acceder a la propiedad **ILyncClient.Self**, que debe devolver un objeto **ISelf**. La interfaz **ISelf** representa al usuario de la aplicación cliente de MI conectado. 
  
La Tabla 6 muestra los miembros que deben implementarse en la clase que hereda de **ISelf**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **ISelf** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes, pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**. 
  
**Tabla 6. Implementación de interfaz ISelf**

|**Miembro**|**Descripción**|
|:-----|:-----|
|Propiedad **Contacto**  <br/> |Obtiene el objeto **IContact** asociado con el usuario local.  <br/> |
   
Las propiedades de presencia, modalidades disponibles, pertenencia a grupos y tipo de contacto del usuario local se exponen a través de la propiedad **ISelf.Contact** (que devuelve un objeto **IContact**). Durante el proceso de inicialización, la aplicación de Office tiene acceso a la propiedad **ISelf.Contact** para obtener una referencia a la información de contacto del usuario local. 
  
Usa el código siguiente para definir una clase que hereda de la interfaz **ISelf** que implementa la propiedad **Contact**. 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-_icontactmanagerevents-interfaces"></a>Las interfaces IContactManager y _IContactManagerEvents.
<a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a>

El objeto **IContactManager** administra los contactos del usuario local, con la información de contacto propia del usuario local. La aplicación de Office utiliza un objeto **IContactManager** para acceder a los objetos **IContact** que se corresponden con los contactos del usuario local. 
  
La Tabla 7 muestra los miembros que deben implementarse en la clase que hereda de **IContactManager** y **_IContactManagerEvents**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **IContactManager** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E\_NOTIMPL**. 
>
> Para más información sobre las interfaces **IContactManager** y **_IContactManagerEvents** y sus miembros, consulta [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) y [ UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**Tabla 7. Implementación de las interfaces IContactManager y _IContactManagerEvents**

|**Interfaz**|**Miembro**|**Descripción**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |Método **GetContactByUri**  <br/> |Busca o crea una nueva instancia de contacto usando el URI de contacto.  <br/> |
||Método **CreateSubscription**  <br/> |Crea un objeto **ISubscription** que puede usarse para suscripciones por lotes o consultas.  <br/> |
||Método **Lookup**  <br/> |Busca un contacto o grupo de distribución.  <br/> |
|**_IContactManagerEvents** <br/> |Evento **OnGroupAdded**  <br/> |Se produce cuando se agrega un grupo a una colección de grupos. La colección de grupo actualizada se puede obtener de la propiedad **IContactManager.Groups**.  <br/> |
||Evento **OnGroupRemoved**  <br/> |Se produce cuando se quita un grupo de una colección de grupos. La colección de grupo actualizada se puede obtener de la propiedad **IContactManager.Groups**.  <br/> |
||Evento **OnSearchProviderStateChanged**  <br/> |Se produce cuando cambia el estado de un proveedor de búsqueda.  <br/> |
   
Office llama a **IContactManager.GetContactByUri** para obtener información de presencia de un contacto mediante la dirección SIP del contacto. Cuando un contacto está configurado para una dirección SIP en Active Directory, Office determina esta dirección para un contacto y llama a **GetContactByUri**, al pasar la dirección SIP del contacto para el parámetro __contactUri_. 
  
Cuando Office no puede determinar la dirección SIP para un contacto, llama al método **IContactManager.Lookup** para encontrar el SIP mediante el servicio de MI. Aquí Office pasa los mejores datos que puede encontrar para el contacto (por ejemplo, solo la dirección de correo del contacto). El método **Lookup** devuelve de forma asincrónica un objeto **AsynchronousOperation**. Cuando invoca la retrollamada, el método **Lookup** debe devolver el éxito o fracaso de la operación además del URI del contacto. 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

La aplicación de Office debe suscribirse a los cambios de presencia de un contacto individual. Por lo tanto, cuando cambia el estado de presencia de un contacto, el servidor de MI le avisa a la aplicación cliente de MI, lo que alerta a la aplicación de Office. Para ello, la aplicación de Office llama al método **IContactManager.CreateSubscription** para crear un nuevo objeto **IContactSubscription** para esta solicitud. 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a>Interfaces IGroup e IGroupCollection.
<a name="off15_IMIntegration_ImplementRequired_IGroup"> </a>

El objeto **IGroup** representa una colección de contactos con propiedades adicionales para identificar la colección de contactos mediante un nombre de grupo colectivo. Un objeto **IGroupCollection** representa una colección de objetos **IGroup** definidos por el usuario local y la aplicación de cliente de MI. La aplicación de Office usa los objetos **IGroupCollection** y **IGroup** para tener acceso a los contactos del usuario local. 
  
La Tabla 9 muestra los miembros que deben implementarse en las clases que heredan de **IGroup** e **IGroupCollection** en la tabla siguiente. 
  
> [!NOTE]
> Cualquier miembro de la interfaz **IGroup** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**. 
>
> Para más información sobre las interfaces **IGroup** e **IGroupCollection** y sus miembros, consulta [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) y [ UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**Tabla 9. Implementación de las interfaces IGroup e IGroupCollection**

|**Interfaz**|**Miembro**|**Descripción**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |Propiedad **Count**  <br/> |Devuelve el número de objeto **IGroup** de la colección  <br/> |
||Propiedad **Item**  <br/> |Devuelve el objeto **IGroup** en el índice especificado en la colección.  <br/> |
|**IGroup** <br/> |Propiedad **Id**  <br/> |Devuelve el id. del grupo.  <br/> |
   
Cuando la aplicación de Office obtiene la información de usuario local, tiene acceso a la pertenencia del contacto (usuario local) al llamar a la propiedad **IContact.CustomGroups** que devuelve un objeto **IGroupCollection**. **IGroupCollection** debe contener una matriz (o **lista**) de objetos **IGroup**. La clase que se deriva de **IGroupCollection** debe exponer una propiedad **Count**, que devuelve el número de elementos de la colección y un método indizador, **this(int)**, que devuelve un objeto **IGroup** de la colección. 
  
### <a name="icontactsubscription-interface"></a>Interfaz IContactSubscription.
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

La interfaz **IContactSubscription** te permite especificar los contactos para recibir actualizaciones de la información de presencia y los tipos de información de presencia que activan una notificación. Las aplicaciones de Office utilizan un objeto **IContactSubscription** para registrar cambios al estado de presencia del contacto 
  
La Tabla 10 muestra los miembros que deben implementarse en las clases que heredan de **IContactSuscription**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **IContactSubscription** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.
>
> Para más información sobre la interfaz **IContactSubscription** y sus miembros, consulta [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**Tabla 10. Implementación de interfaz IContactSubscription**

|**Miembro**|**Descripción**|
|:-----|:-----|
|Método **AddContact**  <br/> |Agrega un contacto al objeto de la suscripción.  <br/> |
|Método **Subscribe**  <br/> |Ayuda de la aplicación cliente de MI a supervisar la presencia de un contacto.  <br/> |
   
La interfaz **IContactSubscription** debe contener una referencia a todos los objetos **IContact** que supervisa, mediante el uso de una matriz o una **Lista**. El método **IContactSubscription.AddContact** agrega un objeto **IContact** a la estructura de datos subyacente del objeto **IContactSubscription**, lo que agrega un contacto nuevo para supervisar los cambios de presencia. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

El método **IContactSubscription.Subscribe** permite que una aplicación cliente de MI acceda a observadores de presencia del contacto. Puede usar una estrategia de sondeo para obtener la presencia del servidor de los contactos para los que se haya suscrito la aplicación cliente de MI. El método **Subscribe** es útil en situaciones donde se solicita la presencia de alguien de fuera de la lista de contactos de un usuario (por ejemplo, de una red pública de mayor tamaño). 
  
### <a name="icontactendpoint-interface"></a>Interfaz IContactEndPoint.
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

**IContactEndPoint** representa un número de teléfono de la colección de números de teléfono de un contacto. 
  
La Tabla 11 muestra los miembros que deben implementarse en las clases que heredan de **IContactEndPoint**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **IContactEndPoint**. que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.
>
> Para más información sobre la interfaz **IContactEndPoint** y sus miembros, consulta [UCCollaborationLib.IContactEndPoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**Tabla 11. Implementación de la interfaz IContactEndPoint**

|**Miembro**|**Descripción**|
|:-----|:-----|
|Propiedad **DisplayName**  <br/> |Obtiene la cadena para mostrar  <br/> |
|Propiedad **Type**  <br/> |Obtiene el tipo de punto de contacto  <br/> |
|Propiedad **Uri**  <br/> |Obtiene el URI del contacto.  <br/> |
   
### <a name="ilocalestring-interface"></a>Interfaz ILocaleString
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

**ILocaleString** es una estructura de cadena localizada que contiene una cadena localizada y el ID de la localización de configuración regional. La interfaz **ILocaleString** se utiliza para dar formato a la cadena de estado personalizado en la tarjeta de contacto. 
  
La Tabla 12 muestra los miembros que deben implementarse en las clases que heredan de **ILocaleString**.
  
> [!NOTE]
> Cualquier miembro de la interfaz **ILocaleString** que no aparezca en la tabla debe estar presente pero no es necesario implementarlo. Los miembros que están presentes pero no implementados pueden producir un error **NotImplementedException** o **E_NOTIMPL**.
>
> Para más información sobre la interfaz **ILocaleString** y sus miembros, consulta [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**Tabla 12. Implementación de interfaz ILocaleString**

|**Miembro**|**Descripción**|
|:-----|:-----|
|Propiedad **LocaleId**  <br/> |Obtiene la id. de configuración regional.  <br/> |
|Propiedad **Value**  <br/> |Obtiene la cadena.  <br/> |
   
## <a name="see-also"></a>Ver también

- Espacio de nombre [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) 
    

