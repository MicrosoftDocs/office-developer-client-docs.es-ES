---
title: Integración de aplicaciones de mensajería instantánea con Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: En este artículo se describe cómo configurar una aplicación cliente de mensaje instantáneo (IM) para que se integra con las características sociales en Office 2013, incluyendo mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contacto.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821453"
---
# <a name="integrating-im-applications-with-office"></a>Integración de aplicaciones de mensajería instantánea con Office

En este artículo se describe cómo configurar una aplicación cliente de mensaje instantáneo (IM) para que se integra con las características sociales en Office 2013, incluyendo mostrar la presencia y enviar mensajes instantáneos desde la tarjeta de contacto.
  
Si tiene alguna pregunta o comentarios sobre este artículo técnico o los procesos que describe, puede ponerse en contacto con Microsoft directamente mediante el envío de un correo electrónico a [docthis@microsoft.com](mailto:docthis@microsoft.com).
  
## <a name="introduction"></a>Introducción
<a name="off15_IMIntegration_Intro"> </a>

Office 2013 proporciona integración enriquecida con el cliente de mensajería instantánea a las aplicaciones, incluido Lync 2013. Esta integración proporciona a los usuarios con funciones de mensajería instantánea desde dentro de Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 y OneNote 2013, así como proporcionar integración de presencia en las páginas de SharePoint 2013. Los usuarios pueden ver la foto, el nombre, el estado de presencia y datos de contacto para las personas de su lista de contactos. Puede iniciar una sesión de mensajería instantánea, llamada de vídeo o llamada telefónica directamente desde la tarjeta de contacto (el elemento de la interfaz de usuario en Office 2013 que superficies, póngase en contacto con las opciones de información y comunicación). Office 2013 facilita permanezcan conectados a sus contactos sin tener fuera de su correo electrónico o documentos. 
  
> [!NOTE]
> En este artículo se utiliza el término aplicación de cliente de mensajería instantánea para hacer referencia específicamente a la aplicación instalada en el equipo del usuario que se comunica con el servicio de mensajería instantánea. Por ejemplo, Lync 2013 se considera una aplicación de cliente de mensajería instantánea. En este artículo no proporciona información detallada acerca de cómo se comunica la aplicación de cliente de mensajería instantánea para el servicio de mensajería instantánea o el propio servicio de mensajería instantánea. 
  
Puede personalizar una aplicación de cliente de mensajería instantánea, por lo que se comunica con Office. En concreto, puede modificar la aplicación de mensajería instantánea para que muestre la información siguiente dentro de la interfaz de usuario de Office:
  
- Foto del contacto.
    
- Nombre del contacto.
    
- Póngase en contacto con nota de estado personal.
    
- Póngase en contacto con el estado de presencia.
    
- Póngase en contacto con la cadena de disponibilidad (por ejemplo, "Disponible" o "fuera de la oficina").
    
- Póngase en contacto con la cadena de capacidad (por ejemplo, "vídeo listo").
    
- Inicio de mensajería instantánea de un solo clic.
    
- Inicio de la llamada de vídeo de un solo clic.
    
- Inicio de llamadas de teléfono de un solo clic (incluidos SIP, número de teléfono, correo de voz y nuevo número de llamada).
    
- Administración de contactos (agregar al grupo de mensajería instantánea).
    
- Póngase en contacto con ubicación y zona horaria.
    
- Datos de contacto, número de teléfono, dirección de correo electrónico, título y nombre de la compañía.
    
**En la figura 1. Tarjeta de contacto de Office 2013**

![La tarjeta de personas en Office 2013] (media/ocom15_peoplecard.png "La tarjeta de personas en Office 2013")
  
Para habilitar esta integración con Office, una aplicación de cliente de mensajería instantánea debe implementar un conjunto de interfaces que proporciona Office para conectarse a ella. Las API para esta integración se incluyen en el espacio de nombres [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) que se encuentra en el archivo Microsoft.Office.UC.dll, que se instala con las versiones de Office 2013 que incluyen Lync / Skype para la empresa. El espacio de nombres **UCCollaborationLib** incluye las interfaces que debe implementar para integrar con Office. 
  
> [!IMPORTANT] 
> La biblioteca de tipos para las interfaces necesarias está incrustada en Lync 2013/Skype para la empresa. Para integradores de sistemas de terceros, esto funciona sólo cuando Lync 2013 y Skype para la empresa están instalados en el equipo de destino. Si va a integrar con Office Standard, debe extraer la biblioteca de tipos e instalarlo en el equipo de destino. El [SDK de Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) incluye el archivo Microsoft.Office.UC.dll. 
  
> [!NOTE]
>  Un conjunto de aplicaciones de Office 2010 puede integrar de forma similar con una aplicación de proveedor de mensajería instantánea de terceros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 y SharePoint Server 2010 (mediante un control ActiveX). Muchos de los pasos necesarios para la integración con Office 2013 aplican también a Office 2010. Hay varias diferencias claves en cómo se integra Office 2010 con una aplicación de proveedor de mensajería instantánea: 
>  - Office 2010 no mostrar fotografía del contacto. 
>  - Debe descargar el archivo Microsoft.Office.Uc.dll por separado desde Office 2010. El [SDK de Lync 2010](http://www.microsoft.com/en-us/download/details.aspx?id=18898) incluye el archivo Microsoft.Office.UC.dll para Office 2010. 
>  - Cuando la aplicación de Office, llama al método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) en la aplicación de cliente de mensajería instantánea, se pasa en la cadena "14.0.0.0". 
>  - Office 2010 enumera todos los grupos y contactos tan pronto como se conecta a una aplicación de cliente de mensajería instantánea. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>¿Cómo se integra Office con una aplicación de cliente de mensajería instantánea
<a name="off15_IMIntegration_How"> </a>

Cuando se inicia una aplicación de Office 2013, pasa por el siguiente proceso para integrarse con la aplicación de cliente de mensajería instantánea predeterminada:
  
1. Comprueba el registro para descubrir la aplicación de cliente de mensajería instantánea de forma predeterminada y, a continuación, se conecta a él.
    
2. Se autentica con la aplicación de cliente de mensajería instantánea.
    
3. Se conecta a interfaces específicas que se exponen con la aplicación de cliente de mensajería instantánea.
    
4. Determina las capacidades del usuario ha iniciado sesión actualmente (usuario local), incluida la introducción de los contactos del usuario, determinar la presencia del usuario y determinar las capacidades de mensajería instantánea del usuario (mensajería instantánea, chat de vídeo, VOIP y así sucesivamente).
    
5. Obtiene información de presencia de los contactos del usuario local.
    
6. Cuando se cierra la aplicación de cliente de mensajería instantánea, la aplicación de Office 2013 se desconecta en modo silencioso.
    
### <a name="discovering-the-im-application"></a>Detección de la aplicación de mensajería instantánea

La aplicación de Office busca varias teclas específicas y las entradas del registro para detectar la aplicación de cliente de mensajería instantánea de forma predeterminada. Si detecta una aplicación de cliente de mensajería instantánea de forma predeterminada, a continuación, intenta conectarse a ella.
  
El proceso que realiza la aplicación de Office para detectar la aplicación de cliente de mensajería instantánea predeterminada es la siguiente:
  
1. La aplicación de Office comprueba si se establece la subclave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp en el registro y lee el nombre de la aplicación enumerados ahí.
    
2. A continuación, la aplicación de Office lee la clave de _nombre de la aplicación_de proveedores de contenido\ HKEY_CURRENT_USER\Software\IM \UpAndRunning y supervisa el valor para que los cambios.
    
3. A continuación, la aplicación de Office lee la clave del registro de proveedores de contenido\ HKEY_LOCAL_MACHINE\Software\IM _nombre de la aplicación_ y obtiene los valores de identificador (CLSID) de nombre de proceso y la clase almacenados en ella. 
    
4. Una vez que la aplicación de cliente de mensajería instantánea ha completado correctamente la secuencia de inicio y registrado todas las clases correctamente para la integración de presencia, se establece la clave de _nombre de la aplicación_de proveedores de contenido\ HKEY_CURRENT_USER\Software\IM \UpAndRunning a "2", que indica que se está ejecutando la aplicación cliente.
    
5. Cuando la aplicación de Office detecta que se ha establecido la clave de _nombre de la aplicación_de proveedores de contenido\ HKEY_CURRENT_USER\Software\IM \UpAndRunning a "2", se revisa la lista de procesos en ejecución en el equipo para el nombre del proceso de la aplicación de cliente de mensajería instantánea.
    
6. Una vez que la aplicación de Office encuentra el proceso que utiliza la aplicación de cliente de mensajería instantánea, la aplicación de Office llama a **CoCreateInstance** utilizando el CLSID para establecer una conexión a la aplicación de cliente de mensajería instantánea como un servidor COM fuera de proceso. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Autenticar la conexión a la aplicación de mensajería instantánea

Después de la aplicación de Office establece una conexión a la aplicación de cliente de mensajería instantánea, a continuación, hace lo siguiente:
  
1. La aplicación de Office llama a método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) para comprobar si la interfaz [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) . 
    
2. La aplicación de Office, a continuación, llama al método **IUCOfficeIntegration.GetAuthenticationInfo** , pasando la versión más alta de integración compatibles (por ejemplo, "15.0.0.0"). 
    
3. Si la aplicación de cliente de mensajería instantánea es compatible con la versión de Office que se pasó como un parámetro, la aplicación devuelve la siguiente cadena XML codificado de forma rígida al código de llamada:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > Por razones de herencia, la aplicación de cliente de mensajería instantánea debe devolver el valor exacto `<authenticationinfo>` a la llamada a **GetAuthenticationInfo** si es compatible con la versión de Office que se pasó como un parámetro. 
  
4. Si se produce un error en la aplicación de cliente de mensajería instantánea devolver un valor, la aplicación de Office llama al método **GetAuthenticationInfo** con la última versión compatible de Office (por ejemplo, "14.0.0.0"). 
    
5. Una vez que Office determina que la aplicación de cliente de mensajería instantánea admite la integración de mensajería instantánea y presencia, se conecta a un conjunto de interfaces para finalizar la inicialización requerido. (Para obtener más información, consulte [Connecting to interfaces necesarias](#off15_IMIntegration_HowConnect)).
    
Si la aplicación de Office detecta un error en cualquiera de los pasos anteriores, deshace los y no se ha establecido la integración de presencia de nuevo durante la sesión de la aplicación de Office. 
  
### <a name="connecting-to-required-interfaces"></a>Que se conectan a interfaces necesarias
<a name="off15_IMIntegration_HowConnect"> </a>

Después de la autenticación de la conexión a la aplicación de cliente de mensajería instantánea, la aplicación de Office intenta conectarse a un conjunto de interfaces necesarias que debe exponer la aplicación de cliente de mensajería instantánea. La aplicación de Office se lleva a cabo mediante el siguiente procedimiento:
  
- La aplicación de Office obtiene que un objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) llamando al método **IUCOfficeIntegration.GetInterface** , pasando el **oiInterfaceLyncClient** constante de la enumeración [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) . 
    
- La aplicación de Office obtiene que un objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) llamando al método **IUCOfficeIntegration.GetInterface** , pasando el **oiInterfaceAutomation** constante de la enumeración **OIInterface** . 
    
- La aplicación de Office se configura el agente de escucha de eventos de [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) . 
    
- La aplicación de Office se configura el agente de escucha de eventos de [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) . 
    
- La aplicación de Office, obtiene el estado de inicio de sesión de la aplicación de cliente de mensajería instantánea mediante el acceso a la propiedad **ILyncClient.State** . 
    
- La aplicación de Office obtiene las capacidades de la aplicación de cliente de mensajería instantánea llamando al método **IUCOfficeIntegration.GetSupportedFeatures** , que devuelve un indicador de la enumeración [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) . 
    
- La aplicación de Office tiene acceso a la propiedad **ILyncClient.Self** para obtener una referencia a un objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) . 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Recuperación de las capacidades del usuario local
<a name="off15_IMIntegration_HowConnect"> </a>

La aplicación de Office obtiene las capacidades del usuario local haciendo lo siguiente:
  
1. Si la aplicación de cliente de mensajería instantánea es compatible con la interfaz **IClient2** , Office intenta obtener un objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) mediante el acceso a la propiedad **IClient2.PrivateContactManager** . 
    
2. Si la aplicación de mensajería instantánea no es compatible con la interfaz **IClient2** , aplicación de Office obtiene un objeto **IContactManager** mediante el acceso a la propiedad **ILyncClient.ContactManager** . La aplicación de cliente de mensajería instantánea correctamente debe devolver un objeto **IContactManager** antes de pueden establecer cualquier otras funciones de mensajería instantánea. 
    
3. La aplicación de Office se tiene acceso a la propiedad **ILyncClient.Uri** y, a continuación, llama a **IContactManager.GetContactByUri** para obtener el objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) asociado con el usuario local. 
    
4. A continuación, la aplicación de Office realiza varias llamadas a **IContact.CanStart** para establecer las capacidades del usuario local, pasando los valores para **ModalityTypes.ucModalityInstantMessage** y **ModalityTypes.ucModalityAudioVideo** sucesivamente. 
    
### <a name="retrieving-contact-presence"></a>Recuperación de presencia de los contactos
<a name="off15_IMIntegration_HowConnect"> </a>

La aplicación de Office obtiene la presencia de los contactos, incluido el usuario local, haciendo lo siguiente: 
  
1. La aplicación de Office llama a **IContact.GetContactInformation** para obtener un elemento de presencia del contacto. 
    
2. A continuación, la aplicación de Office se suscribe a los cambios de estado de presencia del contacto. Se llama **IContactManager.CreateSubscription** para obtener un objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) . A continuación, llama a **IContactSubscription.AddContact** para agregar el contacto a la suscripción y, a continuación, llama a **IContactSubscription.Subscribe** para obtener los cambios en el estado del contacto. 
    
3. Si la aplicación de mensajería instantánea admite **IContact2**, Office intenta obtener información de presencia mediante una llamada a **IContact2.BatchGetContactInformation2**.
    
4. A continuación, la aplicación de Office recupera las propiedades de presencia del contacto mediante una llamada a **IContact.BatchGetContactInformation**. La aplicación de Office puede obtener un segundo conjunto de propiedades de presencia mediante el acceso a la propiedad **IContact.Settings** . 
    
5. Por último, la aplicación de Office obtiene la pertenencia a un grupo del contacto mediante el acceso a la propiedad **IContact.CustomGroups** . Esto devuelve una colección de [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que todos los objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que pertenece el contacto incluye. 
    
### <a name="disconnecting-from-the-im-application"></a>Desconectar de la aplicación de mensajería instantánea
<a name="off15_IMIntegration_HowConnect"> </a>

Cuando la aplicación de Office 2013 detecta el evento **OnShuttingDown** desde la aplicación de mensajería instantánea, desconecta en modo silencioso. Sin embargo, si la aplicación de Office se cierra antes de la aplicación de mensajería instantánea, la aplicación de Office no garantiza que la conexión se limpien. La aplicación de mensajería instantánea debe controlar pérdidas de conexión de cliente. 
  
## <a name="setting-registry-keys-and-entries"></a>Las entradas y las claves del registro de configuración
<a name="off15_IMIntegration_SetRegistry"> </a>

Como se mencionó anteriormente, las aplicaciones de mensajería instantánea capaz de Office 2013 buscan teclas específicas, entradas y valores del registro para detectar la aplicación de cliente de mensajería instantánea para conectarse a. Estos valores del registro proporcionan la aplicación de Office con el nombre del proceso y el CLSID de la clase que actúa como el punto de entrada al modelo de objetos de la aplicación de cliente de mensajería instantánea (es decir, la clase que implementa la interfaz **IUCOfficeIntegration** ). La aplicación de Office crea co-autoría dicha clase y se conecta como un cliente para el servidor COM fuera de proceso en la aplicación de cliente de mensajería instantánea. 
  
Use la tabla 1 para identificar las claves, las entradas y los valores que deben escribirse en el registro para integrar una aplicación de cliente de mensajería instantánea con Office.
  
**La tabla 1. Claves de registro para la configuración de la aplicación de cliente de mensajería instantánea predeterminada**

|**Clave**|**Entry**|**Tipo**|**Valor**|**Ejemplo**|
|:-----|:-----|:-----|:-----|:-----|
|Proveedores de HKEY_LOCAL_MACHINE\Software\IM\\< nombre de la aplicación\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |El nombre de la aplicación de cliente de mensajería instantánea de otro fabricante.  <br/> |Mensajería instantánea de Litware 2012  <br/> |
||Nombre de proceso  <br/> |REG_SZ  <br/> |El nombre del proceso de la aplicación de cliente de mensajería instantánea de otro fabricante.  <br/> |Litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Un identificador de clase (CLSID) para la raíz, clase cocreatable en la aplicación de mensajería instantánea (es decir, la clase que implementa la interfaz **IUCOfficeIntegration** ).  <br/> |(GUID)  <br/> |
|Proveedores de HKEY_CURRENT_USER\Software\IM  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |El nombre de la aplicación de cliente de mensajería instantánea. Esto debe ser el mismo que el nombre en la clave de registro de nivel superior (subárbol) en HKEY_LOCAL_MACHINE.  <br/> |Litware  <br/> |
|Proveedores de HKEY_CURRENT_USER\Software\IM\\< nombre de la aplicación\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Un valor entero entre 0 y 2:  <br/>  0: no está ejecutando  <br/>  1: inicio  <br/>  2: ejecuta  <br/> <br/>**Nota**: la clave del registro de nombre de aplicación debe ser el mismo que el valor de la entrada DefaultIMApp.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Implementar las interfaces necesarias para la integración con Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Existen tres interfaces desde el espacio de nombres **UCCollaborationLib** que debe implementar el archivo ejecutable (o servidor COM) de una aplicación de cliente de mensajería instantánea para que puede integrar con Office. Si no se implementan estas interfaces, deshace la aplicación de Office durante el proceso de inicialización y no se establece la conexión con la aplicación de cliente de mensajería instantánea. 
  
Las interfaces necesarias son los siguientes:
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration), aunque no es necesario, la interfaz de **_IUCOfficeIntegrationEvents** también debe implementarse en la misma clase derivada. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient), aunque no es necesario, la interfaz de **_ILyncClientEvents** también debe implementarse en la misma clase derivada. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>Interfaz IUCOfficeIntegration
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

La interfaz de **IUCOfficeIntegration** proporciona el punto de entrada para una aplicación de Office para conectarse a la aplicación de cliente de mensajería instantánea. La interfaz define tres métodos que llama una aplicación de Office como parte del proceso de inicio de una conexión con la aplicación de cliente de mensajería instantánea. La clase que implementa la interfaz **IUCOfficeIntegration** debe ser co-autoría creable para que Office co-autoría puede crear una instancia de él. Además, debe exponer el CLSID que se escribe como el valor de la entrada de GUID en la clave del registro de proveedores de contenido\ HKEY_LOCAL_MACHINE\Software\IM _nombre de la aplicación_ . 
  
La clase que hereda de **IUCOfficeIntegration** también debe implementar la interfaz **_IUCOfficeIntegrationEvents** . La interfaz **_IUCOfficeIntegrationEvents** contiene a los miembros que exponen los controladores de eventos de la interfaz **IUCOfficeIntegration** . 
  
La tabla 2 muestra a los miembros que deben implementarse en la clase que hereda de **IUCOfficeIntegration** y **_IUCOfficeIntegration**.
  
> [!NOTE]
> Para obtener más información acerca de la **IUCOfficeIntegration** y **_IUCOfficeIntegrationEvents** interfaces y sus miembros, vea [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) y [UCCollaborationLib._IUCOfficeIntegrationEvents ](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**Tabla 2. Implementación de las interfaces IUCOfficeIntegration y _IUCOfficeIntegrationEvents**

|**Interfaz**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |**GetAuthenticationInfo** (método)  <br/> |Obtiene la cadena de información de autenticación.  <br/> |
||**GetInterface** (método)  <br/> |Obtiene la interfaz de una versión concreta.  <br/> |
||**GetSupportedFeatures** (método)  <br/> |Obtiene las características de integración de Office admitidas.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |**OnShuttingDown** (evento)  <br/> |El evento que se produce cuando la aplicación de cliente de mensajería instantánea está intentando apagar.  <br/> |
   
Use el siguiente código para definir una clase que hereda de las interfaces **IUCOfficeIntegration** y **_IUCOfficeIntegration** dentro de una aplicación de cliente de mensajería instantánea. 
  
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

El método **GetAuthenticationInfo** toma una cadena como un argumento para el parámetro de _versión_ . Cuando la aplicación de Office llama a este método, se pasa en uno de dos cadenas para el argumento, según la versión de Office. Cuando la aplicación de Office proporciona el método con la versión de Office que admite la aplicación de cliente de mensajería instantánea (es decir, admite la funcionalidad), el método **GetAuthenticationInfo** devuelve una cadena XML codificado de forma rígida `<authenticationinfo>`. 
  
Use el siguiente código para implementar el método **GetAuthentication** dentro del código de aplicación de cliente de mensajería instantánea. 
  
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

El método **GetInterface** referencias a las clases desplazará al código de llamada, dependiendo de lo que se pasa como un argumento para el parámetro de _interfaz_ . Cuando una aplicación de Office llama el método **GetInterface** , se pasa en uno de dos valores para el parámetro de interfaz: la constante **oiInterfaceILyncClient** (1) o bien la constante **oiInterfaceIAutomation** (2) de la [ UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) (enumeración). Si la aplicación de Office pasa la constante **oiInterfaceILyncClient** , el método **GetInterface** devuelve una referencia a una clase que implementa la interfaz **ILyncClient** . Si la aplicación de Office pasa la constante **oiInterfaceIAutomation** , el método **GetInterface** devuelve una clase que implementa la interfaz **IAutomation** . 
  
Use el siguiente ejemplo de código para implementar el método **GetInterface** dentro del código de aplicación de cliente de mensajería instantánea. 
  
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

El método **GetSupportedFeatures** devuelve información acerca de las características de mensajería instantánea que admite la aplicación de cliente de mensajería instantánea. Toma una cadena para su único parámetro, _versión_. Cuando la aplicación de Office llama al método de **GetSupportFeatures** , el método devuelve un valor de la enumeración [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) . El valor devuelto especifica las funciones del cliente de mensajería instantánea, donde cada función de la aplicación de cliente de mensajería instantánea se indica a la aplicación de Office mediante la adición de un marcador para el valor. 
  
> [!NOTE]
>  Aplicaciones de Office 2013 omitir las siguientes constantes en la enumeración **OIFeature** : 
> - **oiFeaturePictures** (2) 
> - **oiFeatureFreeBusyIntegration**
> - **oiFeaturePhoneNormalization**
  
Use el siguiente ejemplo de código para implementar el método **GetSupportFeatures** dentro del código de aplicación de cliente de mensajería instantánea. 
  
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

La interfaz de **ILyncClient** se asigna a las capacidades de la propia aplicación de cliente de mensajería instantánea. Expone propiedades que hacen referencia a la persona que ha iniciado sesión en la aplicación (el usuario local, representado por la interfaz de [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) ), el estado de la aplicación, la lista de contactos para el usuario local y varias opciones de configuración. Cuando intenta conectarse a la aplicación de cliente de mensajería instantánea, la aplicación de Office obtiene una referencia a un objeto que implementa la interfaz **ILyncClient** . Desde esa referencia, Office puede tener acceso a gran parte de la funcionalidad de la aplicación de cliente de mensajería instantánea. 
  
Además, la clase que implementa la interfaz **ILyncClient** también debe implementar la interfaz **_ILyncClientEvents** . La interfaz **_ILyncClientEvents** expone algunos de los eventos que son necesarios para supervisar el estado de la aplicación de cliente de mensajería instantánea. 
  
Tabla 3 se muestran a los miembros que deben implementarse en la clase que hereda de **ILyncClient** y **_ILyncClientEvents**.
  
> [!NOTE]
> Cualquier miembro de la **ILyncClient** o ** \_ILyncClientEvents** interfaz no aparece en la tabla debe estar presente pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir una **NotImplementedException** o **E\_NOTIMPL** error. 
> 
> Para obtener más información acerca de la **ILyncClient** y **_ILyncClientEvents** interfaces y sus miembros, vea [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) y [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**Tabla 3. Implementación de interfaces ILyncClient y ILyncClientEvents**

|**Interfaz**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |**ContactManager** (propiedad)  <br/> |Obtiene el Administrador de grupo de contactos.  <br/> |
||**ConversationManager** (propiedad)  <br/> |Obtiene el Administrador de conversaciones.  <br/> |
||**Self** (propiedad)  <br/> |Obtiene el objeto **Self** .  <br/> |
||**Inicio de sesión** (método)  <br/> |Inicia el aplicación de cliente de mensajería instantánea inicio de sesión de proceso con una disponibilidad específica.  <br/> |
||**Estado** (propiedad)  <br/> |Obtiene el estado actual de la plataforma.  <br/> |
||**URI** (propiedad)  <br/> |Obtiene el identificador URI de la aplicación de cliente de mensajería instantánea.  <br/> |
|**_ILyncClientEvents** <br/> |**OnStateChanged** (evento)  <br/> |Se produce cuando cambia el estado de aplicación de cliente de mensajería instantánea. Debe controlar este evento y obtenga la propiedad **eventData.NewState** . El evento se desencadena para todos los procesos vinculados a una instancia de una aplicación de cliente de mensajería instantánea cuando cualquier subsistema en la aplicación hace que el cambio de estado.  <br/> |
   
Durante el proceso de inicialización, Office obtiene acceso a la propiedad **ILyncClient.State** . Esta propiedad debe devolver un valor de la enumeración [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) . 
  
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

La propiedad **State** almacena el estado actual de la aplicación de cliente de mensajería instantánea. Debe establecer y actualizan a lo largo de la sesión de aplicación de cliente de mensajería instantánea. Cuando el mensaje instantáneo aplicación cliente inicia sesión, cierra la sesión, o se apaga, debe establecer la propiedad **State** . Es mejor establecer esta propiedad dentro de los métodos **ILyncClient.SignIn** y **ILyncClient.SignOut** , tal y como se muestra en el siguiente ejemplo. 
  
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

En el ejemplo de código siguiente se muestra cómo configurar el agente de escucha de eventos mediante el _ **ILyncClientEvents** y _ **IUCOfficeIntegrationEvents** interfaces. 
  
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

La interfaz de **IAutomation** automatiza las características de la aplicación de cliente de mensajería instantánea. Se puede usar para iniciar conversaciones, participar en conferencias y proporcionar contexto de ventana de extensibilidad. 
  
La tabla 4 muestra a los miembros que deben implementarse en la clase que hereda de **IAutomation**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **IAutomation** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** . 
> 
> Para obtener más información acerca de la interfaz de **IAutomation** y sus miembros, vea [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**Tabla 4. Implementación de interfaz IAutomation**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**StartConversation** (método)  <br/> |Inicia una conversación mediante la modalidad de conversación especificado. Se devuelve una instancia de **IConversationWindow** .  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Implementación de la integración de presencia de los contactos
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

Además de las tres interfaces necesarias que se ha mencionado anteriormente, hay varias otras interfaces que son importantes para habilitar la funcionalidad de presencia de los contactos en Office. Estos son los siguientes:
  
- La interfaz [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) o **IContact2** . 
    
- La interfaz [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) . 
    
- Las interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) y [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) . 
    
- Las interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) y [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) . 
    
- La interfaz [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) . 
    
- La interfaz [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) . 
    
- La interfaz de [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) 
    
### <a name="icontact-interface"></a>Interfaz IContact
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

La interfaz **IContact** representa un usuario de aplicación de cliente de mensajería instantánea. La interfaz expone la presencia, modalidades disponibles, pertenencia a grupos y las propiedades de tipo de contacto de un usuario. Para iniciar una conversación con otro usuario, debe proporcionar esa instancia de usuario de **IContact**.
  
Tabla 5 se muestran a los miembros que deben implementarse en la clase que hereda de **IContact**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **IContact** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** . 
>
> Para obtener más información acerca de la interfaz de **IContact** y sus miembros, vea [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**Tabla 5. Implementación de la interfaz de IContact**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**CanStart** (método)  <br/> |Devuelve **true** si se puede iniciar un tipo determinado de modalidad en el contacto.  <br/> |
|**GetContactInformation** (método)  <br/> |Obtiene un elemento de la presencia de un contacto de la publicación.  <br/> |
|**BatchGetContactInformation** (método)  <br/> |Obtiene varios elementos de la presencia de un contacto de la publicación.  <br/> |
|**Settings** (propiedad)  <br/> |Obtiene una colección de propiedades de contacto.  <br/> |
|**CustomGroups** (propiedad)  <br/> |Obtiene una colección de grupos que el contacto es un miembro de.  <br/> |
   
Durante el proceso de inicialización, la aplicación de Office llama al método de **IContact.CanStart** para determinar las capacidades de mensajería instantánea para el usuario local. El método **CanStart** utiliza un indicador de la enumeración [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como un argumento para el parámetro de_modalityTypes_ _. Si el usuario actual puede integrarse en la modalidad solicitada (es decir, el usuario es capaz de mensajería instantánea, audio y vídeo de mensajería o uso compartido de aplicaciones), el método **CanStart** devuelve **true**.
  
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

El método **GetContactInformation** recupera información sobre el contacto desde el objeto **IContact** . El código de llamada debe pasar un valor de la enumeración [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para el parámetro_contactInformationType_ _, que indica los datos que se va a recuperar. 
  
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

Al igual que el **GetContactInformation**, el método **BatchGetContactInformation** recupera varios elementos de presencia sobre el contacto desde el objeto **IContact** . El código de llamada debe pasar en una matriz de valores de la enumeración **ContactInformationType** para el parámetro de_contactInformationTypes_ _. El método devuelve un objeto [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contiene los datos solicitados. 
  
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

La propiedad **IContact.Settings** devuelve un objeto **IContactSettingDictionary** que contiene propiedades personalizadas sobre el contacto. 
  
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

La propiedad **IContact.CustomGroups** devuelve un objeto **IGroupCollection** que incluye todos los grupos del que el contacto es un miembro de. 
  
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

Durante el proceso de inicialización, la aplicación de Office obtiene los datos para el usuario actual mediante el acceso a la propiedad **ILyncClient.Self** , que debe devolver un objeto **ISelf** . La interfaz **ISelf** representa el usuario de aplicación de cliente de mensajería instantánea local, ha iniciado sesión. 
  
Tabla 6 se muestran a los miembros que deben implementarse en la clase que hereda de **ISelf**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **ISelf** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** . 
  
**Tabla 6. Implementación de la interfaz de ISelf**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**Contacto** (propiedad)  <br/> |Obtiene el objeto **IContact** asociado con el usuario local.  <br/> |
   
Presencia, modalidades disponibles, pertenencia a grupos y las propiedades de tipo de contacto para el usuario local se exponen a través de la propiedad **ISelf.Contact** (que devuelve un objeto **IContact** ). Durante el proceso de inicialización, la aplicación de Office tiene acceso a la propiedad **ISelf.Contact** para obtener una referencia a la información de contacto para el usuario local. 
  
Use el siguiente código para definir una clase que hereda de la interfaz **ISelf** que implementa la propiedad de **contacto** . 
  
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

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a>Interfaces de IContactManager y _IContactManagerEvents
<a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a>

El objeto **IContactManager** administra los contactos del usuario local, incluida la información de contacto del usuario local propia. La aplicación de Office, usa un objeto **IContactManager** para tener acceso a los objetos **IContact** que corresponden a los contactos del usuario local. 
  
Tabla 7 se muestran a los miembros que deben implementarse en la clase que hereda de **IContactManager** y **_IContactManagerEvents**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **IContactManager** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir una **NotImplementedException** o **E\_NOTIMPL** error. 
>
> Para obtener más información acerca de la **IContactManager** y **_IContactManagerEvents** interfaces y sus miembros, vea [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) y [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**Tabla 7. Implementación de las interfaces IContactManager y _IContactManagerEvents**

|**Interfaz**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |**GetContactByUri** (método)  <br/> |Busca o crea una nueva instancia de contacto con el URI del contacto.  <br/> |
||**CreateSubscription** (método)  <br/> |Crea un objeto **ISubscription** que se puede usar para el procesamiento por lotes suscripciones o consultas.  <br/> |
||**Lookup** (método)  <br/> |Busca un contacto o grupo de distribución.  <br/> |
|**_IContactManagerEvents** <br/> |**OnGroupAdded** (evento)  <br/> |Se produce cuando se agrega un grupo a una colección de grupos. La colección de grupos actualizado puede obtenerse de la propiedad **IContactManager.Groups** .  <br/> |
||**OnGroupRemoved** (evento)  <br/> |Se produce cuando se quita un grupo de una colección de grupos. La colección de grupos actualizado puede obtenerse de la propiedad **IContactManager.Groups** .  <br/> |
||**OnSearchProviderStateChanged** (evento)  <br/> |Se produce cuando cambia el estado de un proveedor de búsqueda.  <br/> |
   
Office llama a **IContactManager.GetContactByUri** para obtener información de presencia de un contacto, mediante el uso de la dirección SIP del contacto. Cuando un contacto está configurado para una dirección SIP en Active Directory, Office determina esta dirección para un contacto y las llamadas **GetContactByUri**, pasando la dirección SIP del contacto en el parámetro_contactUri_ _. 
  
Cuando Office no puede determinar la dirección SIP del contacto, llama al método **IContactManager.Lookup** para encontrar el SIP mediante el servicio de mensajería instantánea. Aquí Office pasa los datos mejor que pueden encontrar el contacto (por ejemplo, la dirección de correo electrónico del contacto). El método de **búsqueda** de forma asincrónica devuelve un objeto **AsynchronousOperation** . Cuando invoca la devolución de llamada, el método de **búsqueda** debe devolver el éxito o el fracaso de la operación además del URI del contacto. 
  
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

La aplicación de Office que se necesita para suscribirse a los cambios de presencia de un contacto individual. Por lo tanto, cuando el estado de presencia de un contacto cambia, la aplicación de cliente de mensajería instantánea de las alertas del servidor de mensajería instantánea, con lo que las alertas a la aplicación de Office. Para ello, la aplicación de Office llama el método **IContactManager.CreateSubscription** para crear un nuevo objeto **IContactSubscription** para esta solicitud. 
  
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

### <a name="igroup-and-igroupcollection-interfaces"></a>Interfaces de IGroup y IGroupCollection
<a name="off15_IMIntegration_ImplementRequired_IGroup"> </a>

El objeto **IGroup** representa una colección de los contactos con propiedades adicionales para la identificación de la colección de contacto por un nombre de grupo colectiva. Un objeto **IGroupCollection** representa una colección de objetos de **IGroup** definido por un usuario local y la aplicación de cliente de mensajería instantánea. La aplicación de Office usa los objetos **IGroupCollection** y **IGroup** para tener acceso a los contactos del usuario local. 
  
Tabla 9 se muestran a los miembros que deben implementarse en las clases que heredan de **IGroup** y **IGroupCollection** en la siguiente tabla. 
  
> [!NOTE]
> Cualquier miembro de la interfaz de **IGroup** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** . 
>
> Para obtener más información acerca de las interfaces **IGroup** y **IGroupCollection** y sus miembros, vea [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) y [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**Tabla 9. Implementación de las interfaces IGroup y IGroupCollection**

|**Interfaz**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |**Count** (propiedad)  <br/> |Devuelve el número de objetos de **IGroup** en la colección  <br/> |
||**Elemento** (propiedad)  <br/> |Devuelve el objeto **IGroup** en el índice especificado de la colección.  <br/> |
|**IGroup** <br/> |**ID** (propiedad)  <br/> |Devuelve el identificador del grupo.  <br/> |
   
Cuando la aplicación de Office obtiene la información para el usuario local, que obtiene acceso a las pertenencias a grupos del contacto (usuario local) mediante una llamada a la propiedad **IContact.CustomGroups** , que devuelve un objeto **IGroupCollection** . El **IGroupCollection** debe contener una matriz (o **lista**) de objetos de **IGroup** . La clase que se deriva de **IGroupCollection** debe exponer una propiedad **Count** , que devuelve el número de elementos de la colección y un método de indizador, **this(int)**, que devuelve un objeto **IGroup** de la colección. 
  
### <a name="icontactsubscription-interface"></a>Interfaz IContactSubscription
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

La interfaz de **IContactSubscription** permite especificar los contactos para recibir actualizaciones de la información de presencia de y los tipos de información de presencia que desencadenan una notificación. Aplicaciones de Office utilizan un objeto **IContactSubscription** para registrar los cambios realizados en el estado de presencia del contacto. 
  
Tabla 10 se muestran a los miembros que deben implementarse en las clases que heredan de **IContactSubscription**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **IContactSubscription** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .
>
> Para obtener más información acerca de la interfaz de **IContactSubscription** y sus miembros, vea [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**Tabla 10. Implementación de la interfaz de IContactSubscription**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**AddContact** (método)  <br/> |Agrega un contacto para el objeto de suscripción.  <br/> |
|**SUBSCRIBE** (método)  <br/> |Ayuda a la aplicación de cliente de mensajería instantánea para supervisar la presencia de un contacto.  <br/> |
   
La interfaz **IContactSubscription** debe contener una referencia a todos los objetos **IContact** que supervisa, utilizando una matriz o una **lista**. El método **IContactSubscription.AddContact** agrega un objeto **IContact** para el a la estructura de datos subyacente del objeto **IContactSubscription** , con lo que se agrega un contacto nuevo para supervisar los cambios de presencia. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

El método **IContactSubscription.Subscribe** permite que una aplicación de cliente de mensajería instantánea tener acceso a observadores de presencia del contacto. Puede usar una estrategia de sondeo para obtener que la presencia desde el servidor para los contactos para que se ha suscrito a la aplicación de cliente de mensajería instantánea. El método **Subscribe** es útil en situaciones donde se solicita la presencia de una persona ajena a la lista de contactos de un usuario (por ejemplo, de una red pública mayor). 
  
### <a name="icontactendpoint-interface"></a>Interfaz IContactEndPoint
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

El **IContactEndPoint** representa un número de teléfono de colección de un contacto de números de teléfono. 
  
La tabla 11 se muestran a los miembros que deben implementarse en las clases que heredan de **IContactEndPoint**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **IContactEndPoint** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .
>
> Para obtener más información acerca de la interfaz de **IContactEndPoint** y sus miembros, vea [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**Tabla 11. Implementación de la interfaz de IContactEndPoint**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**DisplayName** (propiedad)  <br/> |Obtiene la cadena para mostrar.  <br/> |
|**Tipo** (propiedad)  <br/> |Obtiene el tipo de contacto de extremo  <br/> |
|**URI** (propiedad)  <br/> |Obtiene el identificador URI del contacto.  <br/> |
   
### <a name="ilocalestring-interface"></a>Interfaz ILocaleString
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

El **ILocaleString** es una estructura de cadena localizada que contiene una cadena localizada y el identificador de configuración regional de la localización. La interfaz de **ILocaleString** se usa para dar formato a la cadena de estado personalizado en la tarjeta de contacto. 
  
La tabla 12 se muestran a los miembros que deben implementarse en las clases que heredan de **ILocaleString**.
  
> [!NOTE]
> Cualquier miembro de la interfaz de **ILocaleString** no aparece en la tabla debe estar presente, pero no es necesario que se va a implementar. Los miembros que están presentes, pero no implementado pueden producir un error **NotImplementedException** o **E_NOTIMPL** .
>
> Para obtener más información acerca de la interfaz de **ILocalString** y sus miembros, vea [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**Tabla 12. Implementación de la interfaz de ILocaleString**

|**Elemento**|**Descripción**|
|:-----|:-----|
|**LocaleId** (propiedad)  <br/> |Obtiene el identificador de configuración regional.  <br/> |
|**Valor** (propiedad)  <br/> |Obtiene la cadena.  <br/> |
   
## <a name="see-also"></a>Ver también

- Espacio de nombres [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) 
    

