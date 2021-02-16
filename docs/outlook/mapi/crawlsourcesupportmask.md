---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420916"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="c2b57-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="c2b57-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="c2b57-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2b57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2b57-105">Especifica si los Microsoft Office Outlook deben examinar las carpetas de un almacén, incluidas las carpetas Contactos, Calendario y Tareas, en el inicio para rellenar el panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="c2b57-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c2b57-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c2b57-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2b57-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="c2b57-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="c2b57-108">[IMsgStore : IMAPIProp (objeto)](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="c2b57-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="c2b57-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="c2b57-109">Created by:</span></span>  <br/> |<span data-ttu-id="c2b57-110">Proveedor de la Tienda</span><span class="sxs-lookup"><span data-stu-id="c2b57-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="c2b57-111">Acceso mediante:</span><span class="sxs-lookup"><span data-stu-id="c2b57-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="c2b57-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="c2b57-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="c2b57-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="c2b57-113">Property type:</span></span>  <br/> |<span data-ttu-id="c2b57-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c2b57-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c2b57-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="c2b57-115">Access type:</span></span>  <br/> |<span data-ttu-id="c2b57-116">Solo lectura o lectura y escritura según el proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="c2b57-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2b57-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2b57-117">Remarks</span></span>

<span data-ttu-id="c2b57-118">Para proporcionar cualquiera de las funciones del almacén, el proveedor del almacén debe implementar [IMAPIProp : IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="c2b57-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="c2b57-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor del almacén también debe devolver el valor de propiedad correcto.</span><span class="sxs-lookup"><span data-stu-id="c2b57-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="c2b57-120">Los proveedores de almacén [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2b57-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="c2b57-121">Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="c2b57-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="c2b57-122">Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) señalada por el parámetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="c2b57-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2b57-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="c2b57-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="c2b57-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c2b57-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c2b57-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="c2b57-125">ulKind:</span></span>  <br/> |<span data-ttu-id="c2b57-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="c2b57-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="c2b57-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="c2b57-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="c2b57-128">L"CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="c2b57-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="c2b57-129">Esta propiedad permite a los proveedores de almacenamiento especificar si Outlook debe examinar varias carpetas de un almacén.</span><span class="sxs-lookup"><span data-stu-id="c2b57-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="c2b57-130">Se usa en el inicio cuando Outlook examina las carpetas existentes en cada almacén abierto para rellenar el **panel de** navegación; Outlook comprueba la presencia y el valor de esta propiedad en un almacén antes de iniciar el examen.</span><span class="sxs-lookup"><span data-stu-id="c2b57-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="c2b57-131">De forma predeterminada, esta propiedad no se expone en un almacén, lo que significa que Outlook puede examinar las carpetas del almacén.</span><span class="sxs-lookup"><span data-stu-id="c2b57-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="c2b57-132">Si se expone la propiedad, los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2b57-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="c2b57-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c2b57-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="c2b57-134">Outlook puede examinar las carpetas del almacén.</span><span class="sxs-lookup"><span data-stu-id="c2b57-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="c2b57-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="c2b57-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="c2b57-136">Outlook no debe examinar las carpetas del almacén.</span><span class="sxs-lookup"><span data-stu-id="c2b57-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="c2b57-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="c2b57-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="c2b57-138">No permita que los clientes cambien esta propiedad en el almacén.</span><span class="sxs-lookup"><span data-stu-id="c2b57-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="c2b57-139">Tenga en cuenta que **la CSM_CLIENT_DO_NOT_CHANGE** es para referencia futura y no está implementada actualmente.</span><span class="sxs-lookup"><span data-stu-id="c2b57-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="c2b57-140">Por ahora, un almacén puede impedir que los clientes cambien esta marca mediante la configuración del valor que devuelve el almacén para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c2b57-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

