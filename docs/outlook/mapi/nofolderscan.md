---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436814"
---
# <a name="nofolderscan"></a><span data-ttu-id="47fa5-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="47fa5-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="47fa5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47fa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47fa5-105">Especifica si Microsoft Office Outlook examinar carpetas de contactos en un almacén.</span><span class="sxs-lookup"><span data-stu-id="47fa5-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="47fa5-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="47fa5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47fa5-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="47fa5-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="47fa5-108">[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="47fa5-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="47fa5-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="47fa5-109">Created by:</span></span>  <br/> |<span data-ttu-id="47fa5-110">Proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="47fa5-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="47fa5-111">Al que se accede mediante:</span><span class="sxs-lookup"><span data-stu-id="47fa5-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="47fa5-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="47fa5-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="47fa5-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="47fa5-113">Property type:</span></span>  <br/> |<span data-ttu-id="47fa5-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47fa5-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47fa5-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="47fa5-115">Access type:</span></span>  <br/> |<span data-ttu-id="47fa5-116">Solo lectura o lectura y escritura según el proveedor de la tienda</span><span class="sxs-lookup"><span data-stu-id="47fa5-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47fa5-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47fa5-117">Remarks</span></span>

<span data-ttu-id="47fa5-118">Para proporcionar cualquiera de las funciones del almacén, el proveedor de la tienda debe implementar [IMAPIProp : IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="47fa5-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="47fa5-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de propiedad correcto.</span><span class="sxs-lookup"><span data-stu-id="47fa5-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="47fa5-120">Los proveedores de almacenamiento [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp para](hrsetoneprop.md) obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47fa5-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="47fa5-121">Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="47fa5-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="47fa5-122">Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="47fa5-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47fa5-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="47fa5-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="47fa5-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="47fa5-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="47fa5-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="47fa5-125">ulKind:</span></span>  <br/> |<span data-ttu-id="47fa5-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="47fa5-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="47fa5-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="47fa5-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="47fa5-128">L"NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="47fa5-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="47fa5-129">Esta propiedad proporciona una forma de que los proveedores de almacenes especifiquen Outlook para no examinar carpetas de contactos en el almacén para evitar la degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="47fa5-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="47fa5-130">Se usa en operaciones de combinación de correspondencia durante las cuales Outlook comprueba la presencia y el valor de esta propiedad antes de iniciar el examen.</span><span class="sxs-lookup"><span data-stu-id="47fa5-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="47fa5-131">De forma predeterminada, esta propiedad no se expone en un almacén, lo que significa Outlook puede examinar la carpeta Contactos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="47fa5-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="47fa5-132">Si se expone la propiedad, los siguientes son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="47fa5-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="47fa5-133">Cero (0): Outlook puede llevar a cabo el examen.</span><span class="sxs-lookup"><span data-stu-id="47fa5-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="47fa5-134">Valor distinto de cero: Outlook no debe examinar carpetas de contactos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="47fa5-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

