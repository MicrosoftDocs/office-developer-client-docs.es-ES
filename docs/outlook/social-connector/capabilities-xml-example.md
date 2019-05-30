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
ms.openlocfilehash: 3340f5b1e0718edd1a062ab817c6621c338bee42
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542264"
---
# <a name="capabilities-xml-example"></a><span data-ttu-id="0e2a6-104">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="0e2a6-104">Capabilities XML example</span></span>

<span data-ttu-id="0e2a6-105">El ejemplo de XML de este tema es una cadena XML devuelta a Outlook Social Connector (OSC) después de llamar al método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para una red social.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-105">The XML example in this topic is an XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method for a social network.</span></span> <span data-ttu-id="0e2a6-106">El código XML muestra cómo un proveedor OSC especifica sus capacidades y requisitos para OSC.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-106">The XML shows how an OSC provider specifies its capabilities and requirements for the OSC.</span></span> 
  
## <a name="capabilities-for-friends"></a><span data-ttu-id="0e2a6-107">Capacidades para amigos</span><span class="sxs-lookup"><span data-stu-id="0e2a6-107">Capabilities for friends</span></span>

<span data-ttu-id="0e2a6-108">En este ejemplo, el proveedor OSC especifica los siguientes elementos para mostrar sus funciones para admitir la característica de amigos:</span><span class="sxs-lookup"><span data-stu-id="0e2a6-108">In this example, the OSC provider specifies the following elements to show its capabilities in supporting the friends feature:</span></span>
  
- <span data-ttu-id="0e2a6-109">**getFriends** como **true** para indicar que el proveedor de OSC admite el método [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) para obtener información de los amigos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-109">**getFriends** as **true** to indicate the OSC provider supports the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method to get friends' information programmatically.</span></span> 
    
- <span data-ttu-id="0e2a6-110">**cacheFriends** como **true** para permitir el almacenamiento en caché de la información de amigos en una carpeta de contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-110">**cacheFriends** as **true** to support caching friends' information in an Outlook contacts folder.</span></span> 
    
- <span data-ttu-id="0e2a6-111">**contactSyncRestartInterval** como 60 para indicar que, en caso de error, el OSC debe volver a intentar actualizar la caché cada 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-111">**contactSyncRestartInterval** as 60 to indicate that on error, the OSC should retry refreshing the cache every 60 minutes.</span></span> 
    
- <span data-ttu-id="0e2a6-112">**followPerson** como **true** para indicar la capacidad de agregar amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-112">**followPerson** as **true** to indicate the ability to add friends on the social network.</span></span> 
    
- <span data-ttu-id="0e2a6-113">**doNotFollowPerson** como **false** para indicar que el proveedor de OSC no admite la eliminación de una persona como amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-113">**doNotFollowPerson** as **false** to indicate the OSC provider does not support removing a person as a friend on the social network.</span></span> 
    
- <span data-ttu-id="0e2a6-114">**dynamicContactsLookup** como **false** para indicar que el OSC no debe almacenar la información de los amigos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-114">**dynamicContactsLookup** as **false** to indicate that the OSC should not store friends' information in memory.</span></span> 
    
## <a name="capabilities-for-activities"></a><span data-ttu-id="0e2a6-115">Capacidades para actividades</span><span class="sxs-lookup"><span data-stu-id="0e2a6-115">Capabilities for activities</span></span>

<span data-ttu-id="0e2a6-116">El proveedor OSC especifica los siguientes elementos para mostrar su capacidad para admitir actividades:</span><span class="sxs-lookup"><span data-stu-id="0e2a6-116">The OSC provider specifies the following elements to show its capability to support activities:</span></span>
  
- <span data-ttu-id="0e2a6-117">**getActivities** como **true** para indicar que el proveedor de OSC admite el método [ISocialProfile:: GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) para obtener las actividades de amigos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-117">**getActivities** as **true** to indicate that the OSC provider supports the [ISocialProfile::GetActivitiesOfFriendsAndColleagues](isocialprofile-getactivitiesoffriendsandcolleagues.md) method to get friends' activities programmatically.</span></span> 
    
- <span data-ttu-id="0e2a6-118">**cacheActivities** como **false** para admitir el almacenamiento en caché de actividades de amigos en la carpeta ocultada de la fuente de noticias de Outlook.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-118">**cacheActivities** as **false** to support caching activities of friends in the hidden Outlook News Feed folder.</span></span> 
    
- <span data-ttu-id="0e2a6-119">**dynamicActivitiesLookupEx** como **true** para indicar que el OSC debe almacenar las actividades de los amigos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-119">**dynamicActivitiesLookupEx** as **true** to indicate that the OSC should store friends' activities in memory.</span></span> 
    
## <a name="capabilities-for-authentication-and-account-configuration"></a><span data-ttu-id="0e2a6-120">Capacidades para la autenticación y la configuración de cuentas</span><span class="sxs-lookup"><span data-stu-id="0e2a6-120">Capabilities for authentication and account configuration</span></span>

<span data-ttu-id="0e2a6-121">El proveedor OSC especifica los siguientes elementos para mostrar su compatibilidad con la autenticación y la configuración de la cuenta:</span><span class="sxs-lookup"><span data-stu-id="0e2a6-121">The OSC provider specifies the following elements to show its support for authentication and account configuration:</span></span>
  
- <span data-ttu-id="0e2a6-122">**useLogonWebAuth** como **false** para indicar que el proveedor de OSC admite la autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-122">**useLogonWebAuth** as **false** to indicate that the OSC provider supports basic authentication.</span></span> 
    
- <span data-ttu-id="0e2a6-123">**supportsAutoConfigure** como **false** para indicar que OSC no debe intentar configurar e iniciar sesión automáticamente en la red social para el usuario.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-123">**supportsAutoConfigure** as **false** to indicate that the OSC should not attempt to automatically configure and log on to the social network for the user.</span></span> 
    
- <span data-ttu-id="0e2a6-124">**useLogonCached** y **hideRememberMyPassword** como **false** para indicar que el OSC debe solicitar la contraseña cada vez y no debe usar las credenciales de inicio de sesión en caché para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-124">**useLogonCached** and **hideRememberMyPassword** as **false** to indicate that the OSC should prompt for password every time and should not use cached logon credentials to log on.</span></span> 
    
- <span data-ttu-id="0e2a6-125">**displayUrl** como **false** para indicar que el OSC no debe mostrar la dirección URL de la red social en el cuadro de diálogo Configuración de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-125">**displayUrl** as **false** to indicate that the OSC should not display the URL for the social network in the account configuration dialog box.</span></span> 
    
- <span data-ttu-id="0e2a6-126">**hideHyperlinks** como **false** para indicar que el proveedor de OSC solo admite cuentas existentes con contraseñas conocidas y que OSC no debe mostrar los hipervínculos **haga clic aquí para crear una cuenta** y haber **olvidado la contraseña?** hipervínculos en el cuadro de diálogo Configuración de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-126">**hideHyperlinks** as **false** to indicate that the OSC provider supports only existing accounts with known passwords, and the OSC should not display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> 
    
## <a name="xml-example"></a><span data-ttu-id="0e2a6-127">Ejemplo de XML</span><span class="sxs-lookup"><span data-stu-id="0e2a6-127">XML example</span></span>

<span data-ttu-id="0e2a6-128">En el ejemplo siguiente se muestran las **funciones** XML de un proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="0e2a6-128">The following example shows the **capabilities** XML of an OSC provider.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="0e2a6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e2a6-129">See also</span></span>

- [<span data-ttu-id="0e2a6-130">Ejemplos de XML del proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="0e2a6-130">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="0e2a6-131">XML para funcionalidades</span><span class="sxs-lookup"><span data-stu-id="0e2a6-131">XML for Capabilities</span></span>](xml-for-capabilities.md)  
- [<span data-ttu-id="0e2a6-132">Ejemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="0e2a6-132">Friends XML Example</span></span>](friends-xml-example.md)  
- [<span data-ttu-id="0e2a6-133">Ejemplo de XML de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="0e2a6-133">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)  
- [<span data-ttu-id="0e2a6-134">Esquema XML del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="0e2a6-134">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

