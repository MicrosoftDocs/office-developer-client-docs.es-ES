---
title: Ejemplo de XML de capacidades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ae1abafe-160c-47c0-b4d5-4a689c8c4cb1
description: 'El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de llamar al método ISocialProvider:: GetCapabilities para una red social. El código XML muestra cómo un proveedor OSC especifica sus capacidades y requisitos para OSC.'
ms.openlocfilehash: 53bd250432e7b27d984a846d206adc812c47898f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281233"
---
# <a name="capabilities-xml-example"></a>Ejemplo de XML de capacidades

El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de llamar al método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para una red social. El código XML muestra cómo un proveedor OSC especifica sus capacidades y requisitos para OSC. 
  
## <a name="capabilities-for-friends"></a>Capacidades para amigos

En este ejemplo, el proveedor OSC especifica los siguientes elementos para mostrar sus funciones para admitir la característica de amigos:
  
- **getFriends** como **true** para indicar que el proveedor de OSC admite el método [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener información de los amigos mediante programación. 
    
- **cacheFriends** como **true** para permitir el almacenamiento en caché de la información de amigos en una carpeta de contactos de Outlook. 
    
- **contactSyncRestartInterval** como 60 para indicar que, en caso de error, el OSC debe volver a intentar actualizar la caché cada 60 minutos. 
    
- **followPerson** como **true** para indicar la capacidad de agregar amigos en la red social. 
    
- **doNotFollowPerson** como **false** para indicar que el proveedor de OSC no admite la eliminación de una persona como amigo en la red social. 
    
- **dynamicContactsLookup** como **false** para indicar que el OSC no debe almacenar la información de los amigos en la memoria. 
    
## <a name="capabilities-for-activities"></a>Capacidades para actividades

El proveedor OSC especifica los siguientes elementos para mostrar su capacidad para admitir actividades:
  
- **getActivities** como **true** para indicar que el proveedor de OSC admite el método [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para obtener las actividades de amigos mediante programación. 
    
- **cacheActivities** como **false** para admitir el almacenamiento en caché de actividades de amigos en la carpeta ocultada de la fuente de noticias de Outlook. 
    
- **dynamicActivitiesLookupEx** como **true** para indicar que el OSC debe almacenar las actividades de los amigos en la memoria. 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a>Capacidades para la autenticación y la configuración de cuentas

El proveedor OSC especifica los siguientes elementos para mostrar su compatibilidad con la autenticación y la configuración de la cuenta:
  
- **useLogonWebAuth** como **false** para indicar que el proveedor de OSC admite la autenticación básica. 
    
- **supportsAutoConfigure** como **false** para indicar que OSC no debe intentar configurar e iniciar sesión automáticamente en la red social para el usuario. 
    
- **useLogonCached** y **hideRememberMyPassword** como **false** para indicar que el OSC debe solicitar la contraseña cada vez y no debe usar las credenciales de inicio de sesión en caché para iniciar sesión. 
    
- **displayUrl** como **false** para indicar que el OSC no debe mostrar la dirección URL de la red social en el cuadro de diálogo Configuración de la cuenta. 
    
- **hideHyperlinks** como **false** para indicar que el proveedor de OSC solo admite cuentas existentes con contraseñas conocidas y que OSC no debe mostrar los hipervínculos **haga clic aquí para crear una cuenta** y haber **olvidado la contraseña?** hipervínculos en el cuadro de diálogo Configuración de la cuenta. 
    
## <a name="xml-example"></a>Ejemplo de XML

En el ejemplo siguiente se muestran las **funciones** XML de un proveedor OSC. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<capabilities xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

- [Ejemplos de XML del proveedor OSC](osc-provider-xml-examples.md)  
- [XML para funcionalidades](xml-for-capabilities.md)  
- [Ejemplo de XML de amigos](friends-xml-example.md)  
- [Ejemplo de XML de fuente de actividades](activity-feed-xml-example.md)  
- [Esquema XML del proveedor de Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

