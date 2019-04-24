---
title: Depurar un proveedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Hay varias formas en las que puede depurar un proveedor de Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281072"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="203e9-103">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="203e9-103">Debugging a provider</span></span>

<span data-ttu-id="203e9-104">Hay varias formas en las que puede depurar un proveedor de Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="203e9-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="203e9-105">Mediante comandos de depuración en el componente de la cinta de la interfaz de usuario de Office Fluent en Outlook o la aplicación cliente de Office auxiliar para hacer que el OSC lleve a cabo diversas acciones.</span><span class="sxs-lookup"><span data-stu-id="203e9-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="203e9-106">Mediante el uso de Fiddler para realizar un seguimiento de las llamadas a la API y el XML enviado entre una red social y su proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="203e9-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="203e9-107">Botones de dePuración</span><span class="sxs-lookup"><span data-stu-id="203e9-107">Debug buttons</span></span>

<span data-ttu-id="203e9-108">La extensibilidad del proveedor de OSC proporciona la capacidad de depurar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="203e9-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="203e9-109">Para depurar un proveedor, `DebugProviders` cree un valor de tipo DWORD en el registro de `SocialConnector` Windows en la clave (como se muestra en la siguiente línea) `DebugProviders` y establezca el valor en 1.</span><span class="sxs-lookup"><span data-stu-id="203e9-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="203e9-110">De forma predeterminada, la depuración del proveedor está desactivada.</span><span class="sxs-lookup"><span data-stu-id="203e9-110">By default, provider debugging is off.</span></span> <span data-ttu-id="203e9-111">Si el `DebugProviders` valor no está presente, o está presente y se establece en un valor de 0, la depuración del proveedor se desactiva.</span><span class="sxs-lookup"><span data-stu-id="203e9-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="203e9-112">Si está activada la depuración del proveedor, OSC muestra un cuadro de diálogo de alerta con información de error detallada cuando se produce un error y valida cualquier XML del proveedor OSC con el esquema XML del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="203e9-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="203e9-113">Basándose en el espacio de nombres especificado para una cadena XML, un proveedor OSC desarrollado con OSC 1,0 se valida con el archivo de esquema OSC 1,0, OutlookSocialProvider. xsd.</span><span class="sxs-lookup"><span data-stu-id="203e9-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="203e9-114">Un proveedor OSC desarrollado con OSC 1,1 o posterior se valida con el archivo de esquema, OutlookSocialProvider_ 1.1. xsd.</span><span class="sxs-lookup"><span data-stu-id="203e9-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="203e9-115">Cuando se usa el `DebugProviders` valor, la alerta de depuración aparece para todos los proveedores cargados en lugar de un proveedor específico.</span><span class="sxs-lookup"><span data-stu-id="203e9-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="203e9-116">Para mostrar los botones de depuración que pueden ayudarle a depurar un proveedor, cree un `ShowDebugButtons` valor de tipo `SocialConnector` DWORD en el registro de `ShowDebugButtons` Windows bajo la clave y establezca el valor en 1.</span><span class="sxs-lookup"><span data-stu-id="203e9-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="203e9-117">Para ocultar los botones de la barra de comandos de `ShowDebugButtons` depuración, establezca el valor en 0.</span><span class="sxs-lookup"><span data-stu-id="203e9-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="203e9-118">Para Outlook 2010 y aplicaciones cliente desde Office 2013, los botones de depuración \*\*\*\* aparecen en la ficha complementos de la cinta de la Explorer.</span><span class="sxs-lookup"><span data-stu-id="203e9-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="203e9-119">Para Outlook 2007 y Outlook 2003, los botones de depuración aparecen en la barra de comandos estándar de la ventana del explorador de Outlook.</span><span class="sxs-lookup"><span data-stu-id="203e9-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="203e9-120">En la tabla siguiente se describen los botones de depuración.</span><span class="sxs-lookup"><span data-stu-id="203e9-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="203e9-121">**Botón dePurar**</span><span class="sxs-lookup"><span data-stu-id="203e9-121">**Debug button**</span></span>|<span data-ttu-id="203e9-122">**Función**</span><span class="sxs-lookup"><span data-stu-id="203e9-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="203e9-123">Sincronizar contactos</span><span class="sxs-lookup"><span data-stu-id="203e9-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="203e9-124">Hace que el OSC pregunte sólo a los contactos almacenados en caché al proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="203e9-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="203e9-125">Sincronización de GAL</span><span class="sxs-lookup"><span data-stu-id="203e9-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="203e9-126">Hace que OSC rellene los datos de la lista global de direcciones de Exchange a los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="203e9-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="203e9-127">Caché de la categoría invalidar</span><span class="sxs-lookup"><span data-stu-id="203e9-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="203e9-128">Hace que OSC vuelva a cargar la lista de categorías de cada almacén cuando se actualiza la fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="203e9-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="203e9-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="203e9-129">Fiddler</span></span>

<span data-ttu-id="203e9-130">Fiddler es una herramienta de depuración en el cable para comprobar las llamadas a la API enviadas desde el proveedor a la red social y el XML enviado por la red social a su proveedor.</span><span class="sxs-lookup"><span data-stu-id="203e9-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="203e9-131">Fiddler está disponible para su descarga en el proxy de dePuración [Web de Fiddler](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="203e9-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="203e9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="203e9-132">See also</span></span>

- [<span data-ttu-id="203e9-133">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="203e9-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="203e9-134">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="203e9-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="203e9-135">Procedimientos recomendados para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="203e9-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="203e9-136">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="203e9-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="203e9-137">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="203e9-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="203e9-138">Preparación para la publicación de un proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="203e9-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

