---
title: Ejemplo de XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de que llama al método ISocialProvider::GetCapabilities para una red social. El código XML muestra cómo especifica un proveedor de OSC sus capacidades y los requisitos para el OSC.
ms.openlocfilehash: 5cafd6d29de8b4357e9e0ce6dab30b125f53b8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821089"
---
# <a name="capabilities-xml-example"></a>Ejemplo de XML de capacidades

El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de que llama al método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para una red social. El código XML muestra cómo especifica un proveedor de OSC sus capacidades y los requisitos para el OSC. 
  
## <a name="capabilities-for-friends"></a>Capacidades de amigos

En este ejemplo, el proveedor de OSC especifica los siguientes elementos para mostrar sus capacidades en compatibilidad con la característica de amigos:
  
- **getFriends** como **true** para indicar que el proveedor de OSC es compatible con el método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener información de amigos mediante programación. 
    
- **cacheFriends** como **true** para admitir la información sobre amigos de almacenamiento en caché en una carpeta de contactos de Outlook. 
    
- **contactSyncRestartInterval** como 60 para indicar que on error, el OSC debe volver a intentar actualizar la caché de cada 60 minutos. 
    
- **followPerson** como **true** para indicar la capacidad de agregar a amigos en la red social. 
    
- **doNotFollowPerson** como **false** para indicar que el proveedor de OSC no es compatible con la eliminación de una persona como amigo en la red social. 
    
- **dynamicContactsLookup** como **false** para indicar que el OSC no debe almacenar información de amigos en la memoria. 
    
## <a name="capabilities-for-activities"></a>Capacidades de actividades

El proveedor de OSC especifica los siguientes elementos para mostrar su capacidad para admitir actividades:
  
- **getActivities** como **true** para indicar que el proveedor OSC admite el método [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para obtener las actividades de amigos mediante programación. 
    
- **cacheActivities** como **false** para admitir las actividades de almacenamiento en caché de amigos en la carpeta oculta de suministro de noticias de Outlook. 
    
- **dynamicActivitiesLookupEx** como **true** para indicar que el OSC debería almacenar las actividades de amigos en la memoria. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Capacidades de configuración de autenticación y cuenta

El proveedor de OSC especifica los siguientes elementos para mostrar su compatibilidad con la autenticación y la configuración de la cuenta:
  
- **useLogonWebAuth** como **false** para indicar que el proveedor OSC admite la autenticación básica. 
    
- **supportsAutoConfigure** como **false** para indicar que no debe tratar el OSC configurar automáticamente e inicie sesión en la red social para el usuario. 
    
- **useLogonCached** y **hideRememberMyPassword** como **false** para indicar que el OSC debe solicitar una contraseña cada vez y no se debe usar en la caché de credenciales de inicio de sesión para iniciar sesión. 
    
- **URL de presentación** como **false** para indicar que el OSC no debe mostrar la dirección URL de la red social en el cuadro de diálogo de configuración de cuenta. 
    
- **hideHyperlinks** como **false** para indicar que el proveedor de OSC admite sólo las cuentas existentes con contraseñas conocidas y no debe mostrar el OSC **haga clic aquí para crear una cuenta** y **¿Olvidó su contraseña?** hipervínculos en la cuadro de diálogo de configuración de cuenta. 
    
## <a name="xml-example"></a>Ejemplo de XML

En el ejemplo siguiente se muestra el XML de las **capacidades** de un proveedor de OSC. 
  
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
  <createAccountUrl>http://contoso.com/createAccount</createAccountUrl>
  <forgotPasswordUrl>http://contoso.com/forgotPassword</forgotPasswordUrl>
</capabilities>

```

## <a name="see-also"></a>Vea también

- [Ejemplos XML de proveedor OSC](osc-provider-xml-examples.md)  
- [XML de capacidades](xml-for-capabilities.md)  
- [Ejemplo de XML de amigos](friends-xml-example.md)  
- [Ejemplo de XML de fuentes de actividades](activity-feed-xml-example.md)  
- [Esquema XML de proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

