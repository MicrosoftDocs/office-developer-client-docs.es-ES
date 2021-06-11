---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418095"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="ea731-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="ea731-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="ea731-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea731-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea731-105">Especifica si Microsoft Office Outlook examinar carpetas de un almacén y archivarlas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ea731-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ea731-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ea731-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea731-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="ea731-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="ea731-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="ea731-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="ea731-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="ea731-109">Created by:</span></span>  <br/> |<span data-ttu-id="ea731-110">Proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="ea731-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="ea731-111">Al que se accede mediante:</span><span class="sxs-lookup"><span data-stu-id="ea731-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="ea731-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="ea731-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="ea731-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ea731-113">Property type:</span></span>  <br/> |<span data-ttu-id="ea731-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea731-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea731-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="ea731-115">Access type:</span></span>  <br/> |<span data-ttu-id="ea731-116">Solo lectura o lectura y escritura según el proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="ea731-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea731-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea731-117">Remarks</span></span>

<span data-ttu-id="ea731-118">Para proporcionar cualquiera de las funciones del almacén, el proveedor de la tienda debe implementar [IMAPIProp : IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="ea731-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="ea731-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de propiedad correcto.</span><span class="sxs-lookup"><span data-stu-id="ea731-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="ea731-120">Los proveedores de almacenamiento [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp para](hrsetoneprop.md) obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea731-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="ea731-121">Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="ea731-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="ea731-122">Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="ea731-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea731-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="ea731-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="ea731-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ea731-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ea731-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="ea731-125">ulKind:</span></span>  <br/> |<span data-ttu-id="ea731-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="ea731-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="ea731-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="ea731-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="ea731-128">L"ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="ea731-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="ea731-129">Esta propiedad permite a los proveedores de almacenamiento especificar si Outlook examinar carpetas de un almacén y archivarlas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ea731-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="ea731-130">De forma predeterminada, esta propiedad no se expone en un almacén, lo que significa Outlook puede examinar carpetas en el almacén.</span><span class="sxs-lookup"><span data-stu-id="ea731-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="ea731-131">Si se expone la propiedad, los siguientes son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="ea731-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="ea731-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ea731-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="ea731-133">Outlook puede examinar carpetas en la tienda.</span><span class="sxs-lookup"><span data-stu-id="ea731-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="ea731-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="ea731-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="ea731-135">Outlook examinar carpetas en el almacén.</span><span class="sxs-lookup"><span data-stu-id="ea731-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="ea731-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ea731-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="ea731-137">No permitir que los clientes cambien esta propiedad en la tienda.</span><span class="sxs-lookup"><span data-stu-id="ea731-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="ea731-138">Tenga en cuenta que la **constante ASM_CLIENT_DO_NOT_CHANGE** es para referencia futura y no se implementa actualmente.</span><span class="sxs-lookup"><span data-stu-id="ea731-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="ea731-139">Por ahora, un almacén puede impedir que los clientes cambien esta marca al establecer de forma hardcoding el valor que el almacén devuelve para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ea731-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

