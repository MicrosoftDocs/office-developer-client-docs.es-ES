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
ms.openlocfilehash: 3477104cc254ea5f22158b9791d7fd3bd776d819
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818414"
---
# <a name="nofolderscan"></a><span data-ttu-id="9c00b-103">NoFolderScan</span><span class="sxs-lookup"><span data-stu-id="9c00b-103">NoFolderScan</span></span>

  
  
<span data-ttu-id="9c00b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c00b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c00b-105">Especifica si Microsoft Office Outlook debe examinar las carpetas de contactos en un almacén.</span><span class="sxs-lookup"><span data-stu-id="9c00b-105">Specifies whether Microsoft Office Outlook should scan Contacts folders on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9c00b-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9c00b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c00b-107">Expuesto en:</span><span class="sxs-lookup"><span data-stu-id="9c00b-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="9c00b-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto</span><span class="sxs-lookup"><span data-stu-id="9c00b-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="9c00b-109">Creado por:</span><span class="sxs-lookup"><span data-stu-id="9c00b-109">Created by:</span></span>  <br/> |<span data-ttu-id="9c00b-110">Proveedor de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9c00b-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="9c00b-111">Tener acceso a ella:</span><span class="sxs-lookup"><span data-stu-id="9c00b-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="9c00b-112">Outlook y otros clientes</span><span class="sxs-lookup"><span data-stu-id="9c00b-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="9c00b-113">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="9c00b-113">Property type:</span></span>  <br/> |<span data-ttu-id="9c00b-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9c00b-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9c00b-115">Tipo de acceso:</span><span class="sxs-lookup"><span data-stu-id="9c00b-115">Access type:</span></span>  <br/> |<span data-ttu-id="9c00b-116">Sólo lectura o lectura y escritura según el proveedor de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9c00b-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c00b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9c00b-117">Remarks</span></span>

<span data-ttu-id="9c00b-118">Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="9c00b-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="9c00b-119">Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta.</span><span class="sxs-lookup"><span data-stu-id="9c00b-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="9c00b-120">Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c00b-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="9c00b-121">Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="9c00b-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="9c00b-122">Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="9c00b-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c00b-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="9c00b-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="9c00b-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9c00b-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9c00b-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="9c00b-125">ulKind:</span></span>  <br/> |<span data-ttu-id="9c00b-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="9c00b-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="9c00b-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="9c00b-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="9c00b-128">L "NoFolderScan"</span><span class="sxs-lookup"><span data-stu-id="9c00b-128">L"NoFolderScan"</span></span>  <br/> |
   
<span data-ttu-id="9c00b-129">Esta propiedad proporciona una manera para los proveedores de almacén especificar a Outlook no para examinar las carpetas de contactos en el almacén para evitar la degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9c00b-129">This property provides a way for store providers to specify to Outlook not to scan Contacts folders in the store to avoid performance degradation.</span></span> <span data-ttu-id="9c00b-130">Se utiliza en las operaciones de combinación de correspondencia durante el cual Outlook comprueba la presencia y el valor de esta propiedad antes de iniciar el análisis.</span><span class="sxs-lookup"><span data-stu-id="9c00b-130">It is used in mail merge operations during which Outlook checks for the presence and value of this property before initiating the scan.</span></span>
  
<span data-ttu-id="9c00b-131">De forma predeterminada, esta propiedad no se expone en un repositorio, lo que significa que Outlook puede examinar la carpeta de contactos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="9c00b-131">By default, this property is not exposed on a store, which means Outlook can scan the Contacts folder on the store.</span></span> <span data-ttu-id="9c00b-132">Si la propiedad se expone, los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c00b-132">If the property is exposed, the following are the possible values:</span></span>
  
- <span data-ttu-id="9c00b-133">Cero (0): Outlook puede llevar a cabo el examen.</span><span class="sxs-lookup"><span data-stu-id="9c00b-133">Zero (0): Outlook can carry out the scan.</span></span>
    
- <span data-ttu-id="9c00b-134">Valor distinto de cero: Outlook no debe examinar las carpetas de contactos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="9c00b-134">Non-zero value: Outlook should not scan Contacts folders on the store.</span></span>
    

