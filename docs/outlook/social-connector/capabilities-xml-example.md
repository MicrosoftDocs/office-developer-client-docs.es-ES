---
title: Ejemplo de XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: El ejemplo XML de este tema es una cadena XML devuelta al conector social (OSC) de Outlook después de llamar al método ISocialProvider::GetCapabilities para una red social. El XML muestra cómo un proveedor de OSC especifica sus capacidades y requisitos para el OSC.
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542264"
---
# <a name="capabilities-xml-example"></a>Ejemplo de XML de capacidades

El ejemplo XML de este tema es una cadena XML devuelta al conector social (OSC) de Outlook después de llamar al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para una red social. El XML muestra cómo un proveedor de OSC especifica sus capacidades y requisitos para el OSC. 
  
## <a name="capabilities-for-friends"></a>Capacidades para amigos

En este ejemplo, el proveedor de OSC especifica los siguientes elementos para mostrar sus capacidades al admitir la característica de amigos:
  
- **getFriends** como **true** para indicar que el proveedor de OSC admite el método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener información de los amigos mediante programación. 
    
- **cacheFriends** como **true para** admitir el almacenamiento en caché de información de amigos en una Outlook contactos. 
    
- **contactSyncRestartInterval** como 60 para indicar que, si se produce un error, el OSC debe volver a intentar actualizar la memoria caché cada 60 minutos. 
    
- **followPerson** como **true** para indicar la capacidad de agregar amigos en la red social. 
    
- **doNotFollowPerson** como **false** para indicar que el proveedor de OSC no admite la eliminación de una persona como amigo en la red social. 
    
- **dynamicContactsLookup** como **false** para indicar que el OSC no debe almacenar la información de los amigos en la memoria. 
    
## <a name="capabilities-for-activities"></a>Capacidades para actividades

El proveedor de OSC especifica los siguientes elementos para mostrar su capacidad para admitir actividades:
  
- **getActivities** como **true** para indicar que el proveedor de OSC admite el método [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para obtener actividades de amigos mediante programación. 
    
- **cacheActivities** como **false para admitir** actividades de almacenamiento en caché de amigos en la carpeta Outlook noticias oculta. 
    
- **dynamicActivitiesLookupEx** como **true** para indicar que el OSC debe almacenar las actividades de los amigos en la memoria. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Capacidades para la autenticación y la configuración de cuentas

El proveedor de OSC especifica los siguientes elementos para mostrar su compatibilidad con la autenticación y la configuración de cuentas:
  
- **useLogonWebAuth** como **false** para indicar que el proveedor de OSC admite la autenticación básica. 
    
- **supportsAutoConfigure** como **false** para indicar que el OSC no debe intentar configurar e iniciar sesión automáticamente en la red social del usuario. 
    
- **useLogonCached** y **hideRememberMyPassword** como **false** para indicar que el OSC debe solicitar contraseña cada vez y no debe usar credenciales de inicio de sesión almacenadas en caché para iniciar sesión. 
    
- **displayUrl** como **false** para indicar que el OSC no debe mostrar la dirección URL de la red social en el cuadro de diálogo configuración de la cuenta. 
    
- **hideHyperlinks** como **false** para indicar que el proveedor de OSC solo admite cuentas  existentes con contraseñas conocidas y el OSC no debe mostrar los hipervínculos Haga clic aquí para crear una cuenta y ¿Ha olvidado la **contraseña?** en el cuadro de diálogo configuración de la cuenta. 
    
## <a name="xml-example"></a>Ejemplo XML

En el ejemplo siguiente se muestra el XML **de funcionalidades** de un proveedor de OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <getFriends>true</getFriends>
  <cacheFriends>true</cacheFriends>
  <followPerson>true</followPerson>
  <doNotFollowPerson>false</doNotFollowPerson>
  <getActivities>true</getActivities>
  <cacheActivities>false</cacheActivities>
  <displayUrl>false</displayUrl>
  <useLogonWebAuth>false</useLogonWebAuth>
  <hideHyperlinks>false</hideHyperlinks>
  <supportsAutoConfigure>false</supportsAutoConfigure>
  <contactSyncRestartInterval>60</contactSyncRestartInterval>
  <dynamicActivitiesLookupEx>true</dynamicActivitiesLookupEx>
  <dynamicContactsLookup>false</dynamicContactsLookup>
  <useLogonCached>false</useLogonCached>
  <hideRememberMyPassword>false</hideRememberMyPassword>
  <createAccountUrl>https://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>https://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Vea también

- [Ejemplos XML del proveedor de OSC](osc-provider-xml-examples.md)  
- [XML para funcionalidades](xml-for-capabilities.md)  
- [Ejemplo de XML de amigos](friends-xml-example.md)  
- [Ejemplo XML de fuente de actividad](activity-feed-xml-example.md)  
- [Outlook Esquema XML del proveedor de Social Connector](outlook-social-connector-provider-xml-schema.md)

