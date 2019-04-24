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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281595"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="51c06-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="51c06-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="51c06-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51c06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51c06-105">Especifica si Microsoft Office Outlook debe analizar las carpetas de un almacén y archivarlas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="51c06-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="51c06-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="51c06-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51c06-107">Expuesto el:</span><span class="sxs-lookup"><span data-stu-id="51c06-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="51c06-108">[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="51c06-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="51c06-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="51c06-109">Created by:</span></span>  <br/> |<span data-ttu-id="51c06-110">Proveedor de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="51c06-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="51c06-111">Se obtiene acceso mediante:</span><span class="sxs-lookup"><span data-stu-id="51c06-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="51c06-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="51c06-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="51c06-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="51c06-113">Property type:</span></span>  <br/> |<span data-ttu-id="51c06-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51c06-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51c06-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="51c06-115">Access type:</span></span>  <br/> |<span data-ttu-id="51c06-116">De solo lectura o de lectura y escritura según el proveedor de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="51c06-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51c06-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51c06-117">Remarks</span></span>

<span data-ttu-id="51c06-118">Para proporcionar cualquiera de las funciones de la tienda, el proveedor de almacenamiento debe implementar [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades que se pasan a una llamada a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="51c06-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="51c06-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp:: GetProps](imapiprop-getprops.md), el proveedor de almacén también debe devolver el valor de propiedad correcto.</span><span class="sxs-lookup"><span data-stu-id="51c06-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="51c06-120">Los proveedores de almacenamiento pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="51c06-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="51c06-121">Para recuperar el valor de esta propiedad, el cliente debe usar primero [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="51c06-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="51c06-122">Al llamar a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) a la que apunta el parámetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="51c06-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51c06-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="51c06-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="51c06-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="51c06-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="51c06-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="51c06-125">ulKind:</span></span>  <br/> |<span data-ttu-id="51c06-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="51c06-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="51c06-127">Kind. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="51c06-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="51c06-128">L "ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="51c06-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="51c06-129">Esta propiedad permite que los proveedores de almacenamiento especifiquen si Outlook debe analizar las carpetas de un almacén y archivarlas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="51c06-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="51c06-130">De forma predeterminada, esta propiedad no se expone en un almacén, lo que significa que Outlook puede examinar carpetas en el almacén.</span><span class="sxs-lookup"><span data-stu-id="51c06-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="51c06-131">Si la propiedad está expuesta, los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="51c06-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="51c06-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="51c06-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="51c06-133">Outlook puede examinar carpetas en la tienda.</span><span class="sxs-lookup"><span data-stu-id="51c06-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="51c06-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="51c06-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="51c06-135">Outlook no debe analizar las carpetas de la tienda.</span><span class="sxs-lookup"><span data-stu-id="51c06-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="51c06-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="51c06-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="51c06-137">No permita que los clientes cambien esta propiedad en el almacén.</span><span class="sxs-lookup"><span data-stu-id="51c06-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="51c06-138">Tenga en cuenta que la constante **ASM_CLIENT_DO_NOT_CHANGE** es para futuras referencias y actualmente no está implementada.</span><span class="sxs-lookup"><span data-stu-id="51c06-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="51c06-139">Por ahora, un almacén puede evitar que los clientes cambien esta marca hardcoding el valor que el almacén devuelve para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="51c06-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

