---
title: Propiedad Hacer tipo de almacén privado
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
ms.openlocfilehash: 7f60d9524af18bb7f2e876386c45b84f207d42bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818068"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="b6ac8-103">Propiedad Hacer tipo de almacén privado</span><span class="sxs-lookup"><span data-stu-id="b6ac8-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="b6ac8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6ac8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6ac8-105">Se trata de un almacén secundario como privada.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b6ac8-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b6ac8-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6ac8-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="b6ac8-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="b6ac8-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="b6ac8-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-109">Created by:</span></span>  <br/> |<span data-ttu-id="b6ac8-110">Proveedor de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="b6ac8-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="b6ac8-111">Tener acceso a ella:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="b6ac8-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="b6ac8-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="b6ac8-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-113">Property type:</span></span>  <br/> |<span data-ttu-id="b6ac8-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b6ac8-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b6ac8-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-115">Access type:</span></span>  <br/> |<span data-ttu-id="b6ac8-116">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6ac8-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6ac8-117">Remarks</span></span>

<span data-ttu-id="b6ac8-118">Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="b6ac8-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="b6ac8-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="b6ac8-120">Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="b6ac8-121">Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="b6ac8-122">Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6ac8-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="b6ac8-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="b6ac8-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="b6ac8-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-125">ulKind:</span></span>  <br/> |<span data-ttu-id="b6ac8-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="b6ac8-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="b6ac8-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="b6ac8-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="b6ac8-128">L "urn: schemas-microsoft-com:office:outlook #storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="b6ac8-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="b6ac8-129">Un proveedor de almacén puede utilizar esta propiedad para que Outlook lo tratan como privadas cuando se trata de un almacén secundario para un usuario.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="b6ac8-130">De forma predeterminada, Outlook trata un almacén secundario de la misma forma como un almacén delegado y los elementos en el almacén secundario son privados sólo si el usuario marca específicamente como privado.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="b6ac8-131">Cuando esta propiedad es **true**, los elementos eliminados de un almacén secundario se mueven a la carpeta **Elementos eliminados** en el almacén principal.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="b6ac8-132">No se muestran los elementos marcados como privados.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-132">Items marked private are not displayed.</span></span> <span data-ttu-id="b6ac8-133">Borradores se almacenan en la carpeta Borradores en el almacén principal.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="b6ac8-134">Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1, o si su valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="b6ac8-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

