---
title: Hacer que el tipo de tienda sea propiedad privada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428546"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="edb42-103">Hacer que el tipo de tienda sea propiedad privada</span><span class="sxs-lookup"><span data-stu-id="edb42-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="edb42-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edb42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edb42-105">Trata un almacén secundario como privado.</span><span class="sxs-lookup"><span data-stu-id="edb42-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="edb42-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="edb42-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="edb42-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="edb42-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="edb42-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="edb42-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="edb42-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="edb42-109">Created by:</span></span>  <br/> |<span data-ttu-id="edb42-110">Proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="edb42-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="edb42-111">Al que se accede mediante:</span><span class="sxs-lookup"><span data-stu-id="edb42-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="edb42-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="edb42-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="edb42-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="edb42-113">Property type:</span></span>  <br/> |<span data-ttu-id="edb42-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="edb42-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="edb42-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="edb42-115">Access type:</span></span>  <br/> |<span data-ttu-id="edb42-116">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="edb42-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edb42-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edb42-117">Remarks</span></span>

<span data-ttu-id="edb42-118">Para proporcionar cualquiera de las funciones del almacén, el proveedor del almacén debe implementar [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="edb42-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="edb42-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de propiedad correcto.</span><span class="sxs-lookup"><span data-stu-id="edb42-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="edb42-120">Los proveedores de almacenamiento [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp para](hrsetoneprop.md) obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="edb42-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="edb42-121">Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="edb42-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="edb42-122">Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="edb42-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="edb42-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="edb42-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="edb42-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="edb42-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="edb42-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="edb42-125">ulKind:</span></span>  <br/> |<span data-ttu-id="edb42-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="edb42-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="edb42-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="edb42-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="edb42-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="edb42-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="edb42-129">Un proveedor de almacenamiento puede usar esta propiedad para Outlook tratarla como privada cuando es un almacén secundario para un usuario.</span><span class="sxs-lookup"><span data-stu-id="edb42-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="edb42-130">De forma predeterminada, Outlook trata un almacén secundario del mismo modo que un almacén delegado y los elementos del almacén secundario son privados solo si el usuario los marca específicamente como privados.</span><span class="sxs-lookup"><span data-stu-id="edb42-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="edb42-131">Cuando esta propiedad es **true,** los elementos eliminados de un almacén secundario se mueven a la **carpeta Elementos eliminados** del almacén principal.</span><span class="sxs-lookup"><span data-stu-id="edb42-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="edb42-132">Los elementos marcados como privados no se muestran.</span><span class="sxs-lookup"><span data-stu-id="edb42-132">Items marked private are not displayed.</span></span> <span data-ttu-id="edb42-133">Los borradores se almacenan en la carpeta Borradores del almacén principal.</span><span class="sxs-lookup"><span data-stu-id="edb42-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="edb42-134">Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1 o si su valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="edb42-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

