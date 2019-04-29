---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435148"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="be7aa-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="be7aa-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="be7aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be7aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be7aa-105">Proporciona la capacidad de recuperar y cambiar el acceso de las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="be7aa-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be7aa-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="be7aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="be7aa-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="be7aa-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="be7aa-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="be7aa-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="be7aa-109">Objeto de datos de propiedad</span><span class="sxs-lookup"><span data-stu-id="be7aa-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="be7aa-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="be7aa-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="be7aa-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="be7aa-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="be7aa-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="be7aa-112">Called by:</span></span>  <br/> |<span data-ttu-id="be7aa-113">Proveedores de servicios y aplicaciones de cliente</span><span class="sxs-lookup"><span data-stu-id="be7aa-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="be7aa-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="be7aa-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="be7aa-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="be7aa-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="be7aa-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="be7aa-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="be7aa-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="be7aa-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="be7aa-118">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="be7aa-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="be7aa-119">No transactd</span><span class="sxs-lookup"><span data-stu-id="be7aa-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="be7aa-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="be7aa-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="be7aa-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="be7aa-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="be7aa-122">Establece el nivel de acceso para el objeto.</span><span class="sxs-lookup"><span data-stu-id="be7aa-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="be7aa-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="be7aa-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="be7aa-124">Establece el nivel de acceso y el estado de una o varias de las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="be7aa-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="be7aa-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="be7aa-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="be7aa-126">Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="be7aa-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="be7aa-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="be7aa-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="be7aa-128">Agrega una o más propiedades de tipo PT Object al objeto.</span><span class="sxs-lookup"><span data-stu-id="be7aa-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be7aa-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be7aa-129">Remarks</span></span>

<span data-ttu-id="be7aa-130">MAPI implementa la interfaz **IPropData:: IMAPIProp** y la usan principalmente los proveedores de servicios que tienen acceso a esta implementación mediante una llamada a la función [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="be7aa-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="be7aa-131">Para obtener más información acerca de los niveles de acceso en objetos y propiedades, consulte [permisos para objetos y propiedades](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="be7aa-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be7aa-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="be7aa-132">See also</span></span>



[<span data-ttu-id="be7aa-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="be7aa-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

