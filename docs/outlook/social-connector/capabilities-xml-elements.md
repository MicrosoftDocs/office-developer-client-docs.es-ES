---
title: Elementos XML de capacidades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: Las tablas de este tema describen los elementos secundarios de las capacidades XML y se agrupan por las áreas que admiten.
ms.openlocfilehash: 6816bbdcd24eceffc47d6b9d0835a90c7089c039
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281199"
---
# <a name="capabilities-xml-elements"></a>Elementos XML de capacidades

Las tablas de este tema describen los elementos secundarios de las **capacidades** XML y se agrupan por las áreas que admiten. El valor predeterminado de cada **elemento capabilities** es **false**. Si el elemento no se especifica en el **XML** de capacidades devuelto por el método [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) el valor del elemento es igual a **false**.
  
Para obtener una descripción general de **las capacidades** XML, vea [XML para funcionalidades.](xml-for-capabilities.md) Para obtener un ejemplo de XML **de** funcionalidades, vea [el ejemplo XML de funcionalidades.](capabilities-xml-example.md) Para obtener una definición completa del esquema XML del proveedor de Microsoft Outlook Social Connector (OSC), incluidos los elementos necesarios u opcionales, vea Esquema XML del proveedor de Outlook [Social Connector](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Funcionalidades para dar soporte a amigos

En la tabla siguiente se muestran los elementos que se aplican a cualquier forma de sincronización de amigos o no amigos.
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indica si el proveedor admite la llamada al método [ISocialSession::UnFollowPerson.](isocialsession-unfollowperson.md)  <br/> **followPerson** y **doNotFollowPerson son** características independientes de un proveedor de OSC. Un proveedor de OSC puede indicar la capacidad de agregar a una persona como un amigo (establecer **followPerson** en **true)** o poder quitar a una persona como un amigo en una cuenta de red social (estableciendo **doNotFollowPerson** en **true**). En general, poder seguir no implica poder dejar de seguir. **followPerson** es una funcionalidad y no debe interpretarse de forma errónea como una acción para seguir a una persona específica o a todas las personas de la cuenta de la red social. **el hecho de** que followPerson **sea true** no implica que **doNotFollowPerson** sea **false**.  <br/> |
|**followPerson** <br/> |Indica si el proveedor admite la llamada al método [ISocialSession::FollowPerson.](isocialsession-followperson.md) El OSC  comprueba si **cacheFriends** es **true** (sincronización en caché de amigos), **dynamicContactsLookup** es **true** (sincronización a petición de amigos y no amigos) o **tanto cacheFriends** como **dynamicContactsLookup** son verdaderos (sincronización híbrida de amigos y no amigos). Si el proveedor establece **followPerson** como **true,** el OSC muestra un distintivo de red en el panel de personas para las personas que el usuario está siguiendo y habilita el comando **\< NetworkName \>** en el menú Agregar **(+)** en el panel de personas. Si el proveedor establece **followPerson** como **false,** no se muestra el distintivo de red y el comando **On \< NetworkName \>** está oculto.  <br/> |
|**getFriends** <br/> |Indica si el proveedor admite la llamada al método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) o [ISocialSession2::GetPeopleDetails.](isocialsession2-getpeopledetails.md) Si el proveedor establece **getFriends** como **true,** el OSC usa el valor **de cacheFriends** o **dynamicContactsLookup** para determinar si la red social permite almacenar amigos como elementos de contacto de Outlook o en la memoria. Si el proveedor establece **getFriends** como **falso,** la red social no admite amigos y los métodos **ISocialPerson::GetFriendsAndColleagues** e **ISocialSession2::GetPeopleDetails,** y el OSC omite los valores de **cacheFriends** y **dynamicContactsLookup**.  <br/> |
   
Los siguientes elementos solo se aplican a la sincronización en caché de amigos o la sincronización híbrida de amigos y no amigos. Para obtener más información acerca de la sincronización de amigos, [consulta Sincronizar amigos y actividades.](synchronizing-friends-and-activities.md)
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**cacheFriends** <br/> |Indica si el proveedor de OSC permite almacenar amigos como elementos de contacto de Outlook. El OSC comprueba **cacheFriends solo** si **getFriends** es **true**. Si el proveedor establece **cacheFriends** como **true,** el OSC sincroniza amigos mediante el almacenamiento en caché y crea una carpeta de contactos específicos de red en el almacén predeterminado del usuario para contactos amigos. El nombre de la carpeta de contactos específica de la red es el valor de la propiedad [ISocialProvider::SocialNetworkName.](isocialprovider-socialnetworkname.md) Si el proveedor establece **cacheFriends** como **false,** el OSC no crea una carpeta de contactos específica de red para que los contactos amigos almacenen amigos.  <br/> |
|**contactSyncRestartInterval** <br/> |Determina el intervalo de reintentos, en minutos, entre intentos de sincronizar la información de amigos desde la red social, si se produce un error de sincronización. El OSC usa este elemento solo si el proveedor de OSC admite la sincronización en caché o la sincronización híbrida de amigos a una carpeta de contactos específica de la red social **(cacheFriends** es **true**).  <br/> El intervalo de reintentos predeterminado es de 30 minutos, a menos que la clave debajo invalide el  `ContactSyncRestartInterval` valor  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` predeterminado. Si el proveedor establece **contactSyncRestartInterval,** el valor del proveedor invalidará el intervalo de reintentos predeterminado de 30 minutos o el valor de la clave del Registro.  <br/> Para obtener más información sobre cómo sincronizar la información de amigos y no amigos a petición, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md)  <br/> |
   
Los siguientes elementos solo se aplican a la sincronización a petición o a la sincronización híbrida de amigos y no amigos.
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indica si el proveedor de OSC admite la llamada [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) para la sincronización a petición de amigos y no amigos.  <br/> El OSC comprueba **dynamicContactsLookup** solo si **getFriends** es **true**. El valor predeterminado de **dynamicContactsLookup** es **false**.  <br/> Si el proveedor de OSC especifica **dynamicContactsLookup** como **true** y **getFriends** como **true,** el OSC llama a **ISocialSession2::GetPeopleDetails** cada vez que se actualiza el panel de personas. El panel de personas se actualiza cuando el usuario selecciona otro usuario en el panel de personas u otro elemento de la ventana del explorador de Outlook, o abre una ventana del inspector de Outlook. La búsqueda dinámica de contactos garantiza que el usuario siempre vea las imágenes de usuario e información de perfil más recientes en el panel de personas, pero aumenta el número de llamadas desde el proveedor a la red social.  <br/> Si el proveedor establece **dynamicContactsLookup** como **false,** el OSC no llama a **ISocialSession2::GetPeopleDetails** para actualizar el panel de personas.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Indica si el OSC debe realizar la sincronización a petición para amigos y no amigos cuando se minimiza el panel de personas.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Capacidades para admitir actividades

El siguiente elemento se aplica a cualquier forma de sincronización de actividades admitidas por el proveedor de OSC.
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**getActivities** <br/> |Indica si el proveedor admite las llamadas al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) o [ISocialPerson::GetActivities.](isocialperson-getactivities.md) Si el proveedor establece **getActivities** como **true**, el OSC usa el valor **de cacheActivities** o **dynamicActivitiesLookupEx** para determinar si el sitio de red social permite almacenar actividades como elementos RSS de Outlook o como actividades en memoria. Si el proveedor establece **getActivities** como **false**, la red social no admite actividades y los métodos **ISocialSession2::GetActivitiesEx** **e ISocialPerson::GetActivities,** y el OSC omite los valores de **cacheActivities** y **dynamicActivitiesLookupEx**.  <br/> |
   
El siguiente elemento solo se aplica a la sincronización almacenada en caché o a la sincronización híbrida de actividades.
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**cacheActivities** <br/> |A partir de Outlook Social Connector 2013, el OSC omite este elemento, ya que los proveedores ya no pueden sincronizar actividades al almacenarlas en caché en una carpeta oculta del almacén del usuario.  <br/> Si el proveedor admite actividades, el proveedor debe admitir la sincronización de actividades a petición. El proveedor establece **cacheActivities** como **false** y **establece dynamicActivitesLookupEx** como **true**. El OSC sincroniza las actividades a petición y almacena en caché las actividades en la memoria. La memoria caché de actividades se actualiza en un intervalo de 30 minutos.  <br/> |
   
Los siguientes elementos solo se aplican a la sincronización a petición o a la sincronización híbrida de actividades.
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |En desuso en OSC 1.1.  <br/> A partir de OSC 1.1, el OSC ya no llama a [ISocialSession::GetActivities](isocialsession-getactivities.md) y omite el valor **de dynamicActivitiesLookup**. Para admitir la búsqueda de actividades a petición, establezca **cacheActivities** como **false** y **getActivities** y **dynamicActivitiesLookupEx** como **true** y el OSC llamará a **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Indica si el proveedor de OSC admite la llamada **ISocialSession2::GetActivitiesEx** para la sincronización a petición de actividades.  <br/> Si el proveedor de OSC admite la sincronización de actividades a petición, establece **getActivities** y **dynamicActivitiesLookupEx** como **true** y **cacheActivities** como **false**. El OSC llama **a ISocialSession2::GetActivitiesEx** cada vez que se actualiza el panel de personas. El panel de personas se actualiza cuando el usuario cambia el elemento seleccionado en la ventana del explorador de Outlook o abre una ventana del inspector de Outlook. La búsqueda de actividades dinámicas garantiza que el usuario siempre verá las actividades más recientes en el panel de personas, pero aumentará el número de llamadas desde el proveedor a la red social.  <br/> Si el proveedor establece **dynamicActivitiesLookupEx** como **false,** el OSC no llama a **ISocialSession2::GetActivitiesEx** para las personas que se muestran en el panel de personas.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indica si el OSC debe realizar la sincronización a petición para las actividades cuando se minimiza el panel de personas.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Funcionalidades comunes para admitir la sincronización a petición o híbrida de amigos, no amigos y actividades

|**Elemento**|**Descripción**|
|:-----|:-----|
|**hashFunction** <br/> | Especifica la función hash que admite el proveedor de OSC. Para proteger la información de identificación personal de los usuarios que no están en la red social o la aplicación de línea de negocio del proveedor, el OSC pasa direcciones de correo electrónico con hash a **ISocialSession2::GetPeopleDetails** e **ISocialSession2::GetActivitiesEx**.  <br/>  Si **dynamicContactsLookup** se establece en **true** o **dynamicActivitiesLookupEx** se establece en **true**, el proveedor debe establecer **hashFunction** en uno de los valores permitidos: **SHA1**, **MD5** o **CRC32MD5**. Si **falta hashFunction** o especifica un valor incorrecto, el OSC devuelve un error.  <br/> **SHA1** es el Algoritmo de hash seguro 1 de Internet Engineering Task Force (IETF) us definido por [[RFC3174]](https://www.rfc-editor.org/rfc/rfc3174.txt). Por ejemplo, el **valor hash SHA1** de la dirección de melissa@contoso.com es  `bb81577b567262a21a4df5f6e335c1250acd7b50` .  <br/> **MD5** es el algoritmo de grupo de trabajo de ingeniería de Internet (IETF) MD5 Message-Digest definido por [[RFC1321]](https://www.rfc-editor.org/rfc/rfc1321.txt). Por ejemplo, el valor con hash **MD5** de la dirección de melissa@contoso.com es  `c8c39e61ca1662477b39b83d7b0a0615` .  <br/> **CRC32MD5** es una combinación de **CRC32** y **MD5** definida de la siguiente manera:  <br/>  Normalice la dirección de correo electrónico quitando los espacios en blanco iniciales y finales y convirtiendo todos los caracteres en minúsculas.  <br/>  Calcule **el valor CRC32** de la dirección de correo electrónico normalizada y use la representación de entero decimal de este valor. Si la implementación devuelve enteros firmados, debe convertir el entero firmado en un entero sin signo.  <br/>  Calcule **el valor MD5** de la dirección de correo electrónico normalizada y use la representación hexadecimal de este valor (usando minúsculas para A a F).  <br/>  Combine estos dos valores con un carácter de subrayado.  <br/>  Por ejemplo, el valor con hash **CRC32MD5** de la dirección de melissa@contoso.com es  `2149665315_c8c39e61ca1662477b39b83d7b0a0615` .  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Funcionalidades para admitir la autenticación y la configuración de cuentas

|**Elemento**|**Descripción**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indica si la red social permite al usuario cambiar las opciones de configuración automática, como proporcionar una dirección URL diferente para iniciar sesión.  <br/> |
|**createAccountUrl** <br/> |Si el proveedor establece **hideHyperlinks** como **false**, cuando el usuario  hace clic en Hacer clic aquí para crear una cuenta en el cuadro de diálogo Configuración de la cuenta, la dirección URL especificada por **createAccountUrl** se abre en el explorador predeterminado.   <br/> |
|**displayUrl** <br/> |Indica si el OSC debe mostrar el cuadro de texto Dirección **URL** de la red social en el cuadro de diálogo de configuración de la cuenta.  <br/> |
|**forgotPasswordUrl** <br/> |Si el proveedor establece **hideHyperlinks** como **false**, cuando el  usuario hace clic en ¿Ha olvidado la **contraseña?** en el cuadro de diálogo Configuración de la cuenta, la dirección URL especificada por **forgotPasswordUrl** se abre en el explorador predeterminado.  <br/> |
|**hideHyperlinks** <br/> |Indica si el OSC  debe ocultar el botón Hacer clic aquí para crear una cuenta y ¿Ha olvidado la **contraseña?** Hipervínculos en el cuadro de diálogo de configuración de la cuenta.  <br/> OSC 1.0 omite esta configuración y los hipervínculos siempre están ocultos. OSC 1.1 observa el valor de esta configuración.  <br/> |
|**hideRememberMyPassword** <br/> |Indica si el OSC debe ocultar la casilla Recordar **mi** contraseña en el cuadro de diálogo de configuración de la cuenta.  <br/> Si el proveedor establece **hideRememberMyPassword** como **true,** el  OSC actuará como si la casilla Recordar mi contraseña esté desactivada y no guardará la contraseña.  <br/> Si el proveedor establece **hideRememberMyPassword** como **false,**  el OSC mostrará la casilla Recordar mi contraseña en el cuadro de diálogo de configuración de la cuenta.  <br/> |
|**supportsAutoConfigure** <br/> |Indica si el OSC debe llamar a la función **GetAutoConfiguredSession** en la interfaz **ISocialProvider** para intentar la configuración automática e iniciar sesión en la red social del usuario.  <br/> |
|**useLogonCached** <br/> |Indica si el proveedor de OSC admite la llamada [ISocialSession2::LogonCached](isocialsession2-logoncached.md) para iniciar sesión con credenciales almacenadas en caché.  <br/> Si el proveedor establece **useLogonCached** como **true,** el OSC omite la configuración de **useLogonWebAuth** y el OSC llama a **ISocialSession2::LogonCached** para la autenticación.  <br/> Si el proveedor establece **dynamicActivitiesLookupEx** como **false,** el OSC no llama a **ISocialSession2::LogonCached** para la autenticación.  <br/> |
|**useLogonWebAuth** <br/> |Indica si el OSC debe usar la autenticación basada en formularios y el [método ISocialSession::LogonWeb.](isocialsession-logonweb.md) Si el proveedor establece **useLogonWebAuth** como **false,** el OSC usa la autenticación básica y llama al método [ISocialSession::Logon.](isocialsession-logon.md) Si el proveedor establece **useLogonWebAuth** como **true**, el OSC usa la autenticación basada en formularios y llama **a ISocialSession::LogonWeb**.  <br/> |
   
Según las **capacidades** XML devueltas por el proveedor en el método **ISocialProvider::GetCapabilities,** cambia el cuadro de diálogo de configuración de la cuenta. Por ejemplo, la figura 1 muestra el cuadro de diálogo de configuración de la cuenta para un ejemplo de TestProvider. 
  
**Figura 1. Ejemplo de TestProvider en el cuadro de diálogo de configuración de la cuenta**

![Información de configuración de ejemplo de TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Consulte también

- [XML para funcionalidades](xml-for-capabilities.md)

