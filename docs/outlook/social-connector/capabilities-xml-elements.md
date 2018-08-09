---
title: Elementos XML de capacidades
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1951643d-e3ca-4d04-bc0c-10d9d0b35dad
description: Las tablas de este tema describen los elementos secundarios de las capacidades de XML y se agrupan por las áreas que admiten.
ms.openlocfilehash: 53bce69bbe22f6e950302a92b0ada21ed0f5a1f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821082"
---
# <a name="capabilities-xml-elements"></a>Elementos XML de capacidades

Las tablas de este tema describen los elementos secundarios de las **capacidades de** XML y se agrupan por las áreas que admiten. El valor predeterminado de cada elemento **capabilities** es **false**. Si el elemento no está especificado en el XML de las **capacidades de** devuelto por el método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , el valor del elemento es igual a **false**.
  
Para una descripción general de **las capacidades** de XML, consulte [XML para las funciones](xml-for-capabilities.md). Para obtener un ejemplo de XML de las **capacidades** , vea [Ejemplo de XML de las capacidades](capabilities-xml-example.md). Para ver una definición completa del esquema XML de proveedor de Microsoft Outlook Social Connector (OSC), incluidos los elementos que son obligatorios u opcionales, vea [Esquema de XML de Outlook Social Connector proveedor](outlook-social-connector-provider-xml-schema.md).
  
## <a name="capabilities-for-supporting-friends"></a>Capacidades para soportar amigos

En la siguiente tabla muestra los elementos que se aplican a cualquier formulario de sincronización de amigos o que no sean de amigos.
  
|**Element**|**Descripción**|
|:-----|:-----|
|**doNotFollowPerson** <br/> |Indica si el proveedor admite la llamada al método [ISocialSession::UnFollowPerson](isocialsession-unfollowperson.md) .  <br/> **followPerson** y **doNotFollowPerson** son características independientes de un proveedor de OSC. Un proveedor de OSC puede indicar la capacidad de ser capaz de agregar a una persona como amigo (configuración **followPerson** en **true**) o para poder quitar a una persona como amigo en una cuenta de red social (configuración **doNotFollowPerson** en **true**). En general, la posibilidad de que se deben seguir no implica la posibilidad de dejar de seguir. **followPerson** es una función, y no es para ser interpretado como una acción que se deben seguir a una persona específica o cada persona en la cuenta de redes sociales. **followPerson** sea **true** no implica **doNotFollowPerson** es **false**.  <br/> |
|**followPerson** <br/> |Indica si el proveedor admite la llamada al método [ISocialSession::FollowPerson](isocialsession-followperson.md) . El OSC comprueba **followPerson** si **cacheFriends** es **true** (sincronización de caché de amigos), **dynamicContactsLookup** es **true** (sincronización a petición de amigos y amigos que no sean), o ambos cacheFriends ** **y **dynamicContactsLookup** son true (sincronización de híbrido de amigos y amigos que no sean). Si el proveedor establece **followPerson** como **true**, el OSC muestra una tarjeta de red en el panel de personas para las personas que sigue el usuario y que permite el **en \<NetworkName\> ** comando en el menú **Agregar (+)** de las personas Panel. Si el proveedor establece **followPerson** como **false**, no se muestra la tarjeta de red y el **en \<NetworkName\> ** comando está oculto.  <br/> |
|**getFriends** <br/> |Indica si el proveedor admite la llamada al método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) o [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . Si el proveedor establece **getFriends** como **true**, el OSC usa el valor de **cacheFriends** o **dynamicContactsLookup** para determinar si la red social permite almacenar amigos como elementos de contactos de Outlook o en la memoria. Si el proveedor establece **getFriends** como **false**, la red social no es compatible con amigos y los métodos de **ISocialSession2::GetPeopleDetails** y **ISocialPerson::GetFriendsAndColleagues** , y el OSC omite los valores de **cacheFriends** y **dynamicContactsLookup**.  <br/> |
   
Los siguientes elementos se aplican únicamente a la sincronización de caché de amigos o sincronización de híbrido de amigos y amigos que no sean. Para obtener más información sobre la sincronización de amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).
  
|**Element**|**Descripción**|
|:-----|:-----|
|**cacheFriends** <br/> |Indica si el proveedor OSC permite almacenar amigos como elementos de contactos de Outlook. El OSC comprueba **cacheFriends** sólo si **getFriends** es **true**. Si el proveedor establece **cacheFriends** como **true**, el OSC sincroniza a amigos mediante el almacenamiento en caché y crea una carpeta de contactos específica de la red en el almacén del usuario de forma predeterminada para los contactos de amigo. El nombre de la carpeta de contactos específica de la red es el valor de la propiedad [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . Si el proveedor establece **cacheFriends** como **false**, el OSC no crea una carpeta de contactos específica de la red para contactos de amigo almacenar a amigos.  <br/> |
|**contactSyncRestartInterval** <br/> |Determina el intervalo de reintento, en minutos, entre los intentos para sincronizar la información de amigos desde la red social, si se produce un error de sincronización. El OSC usa este elemento sólo si el proveedor de OSC admite la sincronización en caché o carpeta de contactos de sincronización híbrido de amigos a una determinada de red social (**cacheFriends** es **true**).  <br/> El intervalo de reintento predeterminado es 30 minutos, a menos que el valor predeterminado se reemplaza por el `ContactSyncRestartInterval` clave en `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`. Si el proveedor establece **contactSyncRestartInterval**, el valor de proveedor invalidará el intervalo de reintento predeterminado de 30 minutos o el valor de clave del registro.  <br/> Para obtener más información acerca de cómo sincronizar información de amigos que no sean a petición y amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).  <br/> |
   
Los siguientes elementos se aplican únicamente a petición sincronización o sincronización híbrido de amigos y amigos que no sean.
  
|**Element**|**Descripción**|
|:-----|:-----|
|**dynamicContactsLookup** <br/> |Indica si el proveedor de OSC admite la llamada [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) para la sincronización a petición de amigos y amigos que no sean.  <br/> El OSC comprueba **dynamicContactsLookup** sólo si **getFriends** es **true**. El valor predeterminado de **dynamicContactsLookup** es **false**.  <br/> Si el proveedor de OSC especifica **dynamicContactsLookup** como **true** y **getFriends** como **true**, el OSC llama **ISocialSession2::GetPeopleDetails** cada vez que se actualiza el panel de personas. El panel de personas se actualiza cuando el usuario selecciona otro usuario en el panel de personas u otro elemento en la ventana del explorador de Outlook, o abre una ventana de inspector de Outlook. La búsqueda de contactos dinámico se asegura de que el usuario siempre ve la información de perfil en el panel de personas y las imágenes de usuario más recientes, pero aumenta el número de llamadas desde el proveedor a la red social.  <br/> Si el proveedor establece **dynamicContactsLookup** como **false**, el OSC no llama a **ISocialSession2::GetPeopleDetails** para actualizar el panel de personas.  <br/> |
|**showOnDemandContactsWhenMinimized** <br/> |Indica si el OSC debe llevar a cabo la sincronización a petición de amigos y amigos que no sean cuando el panel de personas esté minimizado.  <br/> |
   
## <a name="capabilities-for-supporting-activities"></a>Capacidades de las actividades de soporte

El siguiente elemento se aplica a cualquier forma de sincronización de actividades admitidos por el proveedor OSC.
  
|**Element**|**Descripción**|
|:-----|:-----|
|**getActivities** <br/> |Indica si el proveedor admite las llamadas al método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) o [ISocialPerson::GetActivities](isocialperson-getactivities.md) . Si el proveedor establece **getActivities** como **true**, el OSC usa el valor de **cacheActivities** o **dynamicActivitiesLookupEx** para determinar si el sitio de red social permite almacenar las actividades como elementos RSS de Outlook o como actividades en memoria. Si el proveedor establece **getActivities** como **false**, la red social no es compatible con las actividades y los métodos de **ISocialPerson::GetActivities** y **ISocialSession2::GetActivitiesEx** , y el OSC omite los valores de ** cacheActivities** y **dynamicActivitiesLookupEx**.  <br/> |
   
El siguiente elemento se aplica a sólo en caché de sincronización o sincronización híbrido de actividades.
  
|**Element**|**Descripción**|
|:-----|:-----|
|**cacheActivities** <br/> |A partir de Outlook Social Connector 2013, el OSC ignora este elemento, ya que los proveedores ya no pueden sincronizar actividades mediante el almacenamiento en memoria caché en una carpeta oculta en el almacén del usuario.  <br/> Si las actividades de admite de proveedor, el proveedor deben admitir sincronizar actividades a petición. El proveedor establece **cacheActivities** como **false** y **dynamicActivitesLookupEx** como **true**. El OSC sincroniza las actividades a petición y se almacena en caché las actividades en la memoria. Se actualiza la memoria caché de las actividades en un intervalo de 30 minutos.  <br/> |
   
Los siguientes elementos se aplican únicamente a petición sincronización o sincronización híbrido de actividades.
  
|**Element**|**Descripción**|
|:-----|:-----|
|**dynamicActivitiesLookup** <br/> |En desuso en OSC 1.1.  <br/> A partir de OSC 1.1, el OSC ya no llama a [ISocialSession::GetActivities](isocialsession-getactivities.md) y omite el valor de **dynamicActivitiesLookup**. Para admitir la búsqueda de actividades a petición, establezca **cacheActivities** como **false** y **getActivities** y **dynamicActivitiesLookupEx** como **true**y el OSC llamará **ISocialSession2::GetActivitiesEx**.  <br/> |
|**dynamicActivitiesLookupEx** <br/> |Indica si el proveedor de OSC admite la llamada **ISocialSession2::GetActivitiesEx** para la sincronización a petición de actividades.  <br/> Si el proveedor de OSC admite la sincronización de actividades a petición, establece **getActivities** y **dynamicActivitiesLookupEx** como **true**y **cacheActivities** como **false**. El OSC llama a **ISocialSession2::GetActivitiesEx** cada vez que se actualiza el panel de personas. El panel de personas se actualiza cuando el usuario cambia el elemento seleccionado en la ventana del explorador de Outlook o abre una ventana de inspector de Outlook. Búsqueda de actividades dinámico se asegura de que el usuario siempre verá las actividades más recientes en el panel de personas, pero aumentará el número de llamadas desde el proveedor a la red social.  <br/> Si el proveedor establece **dynamicActivitiesLookupEx** como **false**, el OSC no llama a **ISocialSession2::GetActivitiesEx** para las personas que se muestra en el panel de personas.  <br/> |
|**showOnDemandActivitiesWhenMinimized** <br/> |Indica si el OSC debe llevar a cabo la sincronización a petición para actividades cuando el panel de personas esté minimizado.  <br/> |
   
## <a name="common-capabilities-for-supporting-on-demand-or-hybrid-synchronization-of-friends-non-friends-and-activities"></a>Funciones comunes para admitir la sincronización a petición o híbrida de amigos, que no sean de amigos y actividades

|**Element**|**Descripción**|
|:-----|:-----|
|**hashFunction** <br/> | Especifica la función de hash que admite el proveedor de OSC. Para proteger la información personal identificable de los usuarios que no estén en el proveedor de la red social o aplicación de línea de negocio, el OSC pasa las direcciones de correo electrónico con hash a **ISocialSession2::GetPeopleDetails** y **ISocialSession2:: GetActivitiesEx**.  <br/>  Si **dynamicContactsLookup** se establece en **true** o **dynamicActivitiesLookupEx** se establece en **true**, el proveedor debe establecer **hashFunction** en uno de los valores permitidos: **SHA1**, **MD5**o **CRC32MD5**. Si falta **hashFunction** o si especifica un valor incorrecto, el OSC devuelve un error.  <br/> **SHA1** es Internet Engineering Task Force (IETF) US algoritmo de Hash seguro 1 definido por [[RFC3174]](http://www.rfc-editor.org/rfc/rfc3174.txt). Por ejemplo, el valor de **SHA1** un algoritmo hash de correo electrónico dirección melissa@contoso.com es `bb81577b567262a21a4df5f6e335c1250acd7b50`.  <br/> **MD5** es el algoritmo de síntesis de mensajes MD5 de ingeniería de Internet (IETF) definido por [[RFC1321]](http://www.rfc-editor.org/rfc/rfc1321.txt). Por ejemplo, el valor de **MD5** un algoritmo hash de correo electrónico dirección melissa@contoso.com es `c8c39e61ca1662477b39b83d7b0a0615`.  <br/> **CRC32MD5** es una combinación de **CRC32** y **MD5** se definen como sigue:  <br/>  Normalizar la dirección de correo electrónico quitando iniciales y los espacios en blanco y convertir todos los caracteres a minúsculas.  <br/>  Calcular el valor de **CRC32** para la dirección de correo electrónico normalizado y utilice la representación decimal entero de este valor. Si su implementación devuelve enteros con signo, debe convertir el entero con signo en un entero sin signo.  <br/>  Calcular el valor **MD5** para la dirección de correo electrónico normalizado y usar la representación hexadecimal de este valor (mediante en minúsculas de la A la F).  <br/>  Combinar estos dos valores con un carácter de subrayado.  <br/>  Por ejemplo, el valor de **CRC32MD5** un algoritmo hash de correo electrónico dirección melissa@contoso.com es `2149665315_c8c39e61ca1662477b39b83d7b0a0615`.  <br/> |
   
## <a name="capabilities-for-supporting-authentication-and-account-configuration"></a>Capacidades para admitir la autenticación y la configuración de la cuenta

|**Element**|**Descripción**|
|:-----|:-----|
|**allowChangesToAutoConfigure** <br/> |Indica si la red social permite al usuario cambiar las opciones de configuración automática, como proporcionar una dirección URL diferente para iniciar sesión.  <br/> |
|**createAccountUrl** <br/> |Si el proveedor establece **hideHyperlinks** como **false**, cuando el usuario hace clic en **haga clic aquí para crear una cuenta** en el cuadro de diálogo de **configuración de la cuenta** , la dirección URL especificada por **createAccountUrl** se abre en el explorador predeterminado.  <br/> |
|**URL de presentación** <br/> |Indica si el OSC debe mostrar el cuadro de texto **Dirección URL** para la red social en el cuadro de diálogo de configuración de cuenta.  <br/> |
|**forgotPasswordUrl** <br/> |Si el proveedor establece **hideHyperlinks** como **false**, cuando el usuario hace clic en **¿Olvidó su contraseña?** en el cuadro de diálogo **configuración de la cuenta** , la dirección URL especificada por **forgotPasswordUrl** se abre en el explorador predeterminado.  <br/> |
|**hideHyperlinks** <br/> |Indica si el OSC debe ocultar, **haga clic aquí para crear una cuenta** y **¿Olvidó su contraseña?** hipervínculos en el cuadro de diálogo de configuración de cuenta.  <br/> OSC 1.0 pasa por alto esta configuración, y los hipervínculos siempre están ocultos. OSC 1.1 se observa el valor de esta configuración.  <br/> |
|**hideRememberMyPassword** <br/> |Indica si el OSC debe ocultar la casilla de verificación **Recordar mi contraseña** en el cuadro de diálogo de configuración de cuenta.  <br/> Si el proveedor establece **hideRememberMyPassword** como **true**, el OSC van a actuar como si la casilla **Recordar mi contraseña** está desactivada y no guardará la contraseña.  <br/> Si el proveedor establece **hideRememberMyPassword** como **false**, el OSC mostrará la casilla de verificación **Recordar mi contraseña** en el cuadro de diálogo de configuración de cuenta.  <br/> |
|**supportsAutoConfigure** <br/> |Indica si el OSC debe llamar a la función **GetAutoConfiguredSession** en la interfaz de **ISocialProvider** para intentar la configuración automática e iniciar sesión en la red social para el usuario.  <br/> |
|**useLogonCached** <br/> |Indica si el proveedor de OSC admite la llamada [ISocialSession2::LogonCached](isocialsession2-logoncached.md) para iniciar sesión con credenciales almacenadas en caché.  <br/> Si el proveedor establece **useLogonCached** como **true**, el OSC ignora la configuración de **useLogonWebAuth** y el OSC llama a **ISocialSession2::LogonCached** para la autenticación.  <br/> Si el proveedor establece **dynamicActivitiesLookupEx** como **false**, el OSC no llama a **ISocialSession2::LogonCached** para la autenticación.  <br/> |
|**useLogonWebAuth** <br/> |Indica si el OSC debe usar la autenticación basada en formularios y el método [ISocialSession::LogonWeb](isocialsession-logonweb.md) . Si el proveedor establece **useLogonWebAuth** como **false**, el OSC usa la autenticación básica y llama al método [ISocialSession::Logon](isocialsession-logon.md) . Si el proveedor establece **useLogonWebAuth** como **true**, el OSC usa la autenticación basada en formularios y llama a **ISocialSession::LogonWeb**.  <br/> |
   
Dependiendo de las **capacidades de** XML devuelto por el proveedor en el método **ISocialProvider::GetCapabilities** , la configuración de la cuenta cambios del cuadro de diálogo. Por ejemplo, en la figura 1 se muestra el cuadro de diálogo de configuración de cuenta para obtener un ejemplo de TestProvider. 
  
**En la figura 1. Ejemplo de TestProvider en el cuadro de diálogo de configuración de cuenta**

![Información de configuración de ejemplo de TestProvider](media/odc_ol14_ta_OSCFigure4.jpg)
  
## <a name="see-also"></a>Vea también

- [XML de capacidades](xml-for-capabilities.md)

