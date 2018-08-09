---
title: Depurar un proveedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Hay varias maneras puede depurar un proveedor de Outlook Social Connector (OSC):'
ms.openlocfilehash: ada439ca3b038ca9a0e849b47ff6a5f54e5016f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821091"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="2d251-103">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="2d251-103">Debugging a provider</span></span>

<span data-ttu-id="2d251-104">Hay varias maneras puede depurar un proveedor de Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="2d251-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="2d251-105">Mediante el uso de comandos de depuración en el componente de la cinta de opciones de la interfaz de usuario Office Fluent en Outlook o en la aplicación de cliente de Office auxiliar para hacer que el OSC para realizar diversas acciones.</span><span class="sxs-lookup"><span data-stu-id="2d251-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="2d251-106">Mediante el uso de Fiddler para las llamadas de API de seguimiento y XML enviados entre una red social y su proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="2d251-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="2d251-107">Depurar los botones</span><span class="sxs-lookup"><span data-stu-id="2d251-107">Debug buttons</span></span>

<span data-ttu-id="2d251-108">La extensibilidad del proveedor OSC proporciona la capacidad de depuración de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="2d251-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="2d251-109">Para depurar un proveedor, cree un `DebugProviders` el valor de tipo DWORD en el registro de Windows en el `SocialConnector` clave (como se muestra en la siguiente línea) y establecer el `DebugProviders` valor a 1.</span><span class="sxs-lookup"><span data-stu-id="2d251-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="2d251-110">De forma predeterminada, el proveedor de depuración está desactivada.</span><span class="sxs-lookup"><span data-stu-id="2d251-110">By default, provider debugging is off.</span></span> <span data-ttu-id="2d251-111">Si el `DebugProviders` valor no está presente, o está presente y establecido en un valor de 0, el proveedor de depuración está desactivada.</span><span class="sxs-lookup"><span data-stu-id="2d251-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="2d251-112">Si el proveedor de depuración está activado, el OSC muestra un cuadro de diálogo de alerta con información detallada del error cuando se produce un error y valida cualquier proveedor de OSC XML con el esquema XML de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="2d251-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="2d251-113">Según el espacio de nombres especificado para una cadena XML, un proveedor de OSC desarrollado mediante el uso de OSC 1.0 se valida con el archivo de esquema de OSC 1.0, OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="2d251-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="2d251-114">Un proveedor de OSC desarrollado mediante el uso de OSC 1.1 o posterior se valida con el archivo de esquema, OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="2d251-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="2d251-115">Cuando se utiliza la `DebugProviders` de valor, aparece la alerta de depuración para cargados todos los proveedores en lugar de un proveedor específico.</span><span class="sxs-lookup"><span data-stu-id="2d251-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="2d251-116">Para mostrar los botones de depuración que pueden ayudar a depurar un proveedor, cree un `ShowDebugButtons` el valor de tipo DWORD en el registro de Windows en el `SocialConnector` clave y establecer el `ShowDebugButtons` valor a 1.</span><span class="sxs-lookup"><span data-stu-id="2d251-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="2d251-117">Para ocultar los botones de barra de comandos de depuración, establecer el `ShowDebugButtons` valor en 0.</span><span class="sxs-lookup"><span data-stu-id="2d251-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="2d251-118">Para Outlook 2010 y las aplicaciones de cliente con respecto a Office 2013, los botones de depuración aparecen en la ficha **complementos** de la cinta de opciones del explorador.</span><span class="sxs-lookup"><span data-stu-id="2d251-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="2d251-119">Para Outlook 2007 y Outlook 2003, los botones de depuración aparecen en la barra de comandos estándar de la ventana del explorador de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2d251-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="2d251-120">En la siguiente tabla se describe los botones de depuración.</span><span class="sxs-lookup"><span data-stu-id="2d251-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="2d251-121">**Botón de depuración**</span><span class="sxs-lookup"><span data-stu-id="2d251-121">**Debug button**</span></span>|<span data-ttu-id="2d251-122">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="2d251-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d251-123">Sincronizar contactos</span><span class="sxs-lookup"><span data-stu-id="2d251-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="2d251-124">Hace que el OSC para solicitar al proveedor de OSC sólo los contactos almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="2d251-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="2d251-125">Sincronización de GAL</span><span class="sxs-lookup"><span data-stu-id="2d251-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="2d251-126">Hace que el OSC rellenar los datos desde la lista Global de direcciones de Exchange para los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2d251-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="2d251-127">Invalidar la memoria caché de categoría</span><span class="sxs-lookup"><span data-stu-id="2d251-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="2d251-128">Hace que el OSC volver a cargar la lista de categorías para cada almacén cuando se actualiza la fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="2d251-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="2d251-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="2d251-129">Fiddler</span></span>

<span data-ttu-id="2d251-130">Fiddler es una herramienta de depuración sobre el cable para comprobar el llamadas a la API enviados desde su proveedor a la red social y XML que se envían por la red social a su proveedor.</span><span class="sxs-lookup"><span data-stu-id="2d251-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="2d251-131">Fiddler está disponible para su descarga en el [Proxy de depuración de Web de Fiddler](http://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="2d251-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](http://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d251-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d251-132">See also</span></span>

- [<span data-ttu-id="2d251-133">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="2d251-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="2d251-134">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="2d251-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="2d251-135">Prácticas recomendadas para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="2d251-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="2d251-136">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="2d251-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="2d251-137">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="2d251-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="2d251-138">Prepararse liberar un proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="2d251-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

