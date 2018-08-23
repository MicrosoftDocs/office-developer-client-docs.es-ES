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
ms.openlocfilehash: c320b2c42b9a14c6dc428fc3df59991528cdbe36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592573"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="5c62f-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c62f-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="5c62f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c62f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c62f-105">Proporciona la capacidad para recuperar y cambiar el acceso para las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="5c62f-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c62f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5c62f-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c62f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5c62f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5c62f-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="5c62f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5c62f-109">Objeto de datos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5c62f-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="5c62f-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="5c62f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c62f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c62f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c62f-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5c62f-112">Called by:</span></span>  <br/> |<span data-ttu-id="5c62f-113">Proveedores de servicios y aplicaciones de cliente</span><span class="sxs-lookup"><span data-stu-id="5c62f-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="5c62f-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="5c62f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5c62f-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="5c62f-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="5c62f-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="5c62f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5c62f-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="5c62f-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="5c62f-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="5c62f-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="5c62f-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="5c62f-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5c62f-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="5c62f-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5c62f-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="5c62f-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="5c62f-122">Establece el nivel de acceso para el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c62f-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="5c62f-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="5c62f-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="5c62f-124">Establece el nivel de acceso y el estado de una o varias de las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c62f-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="5c62f-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="5c62f-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="5c62f-126">Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c62f-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="5c62f-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="5c62f-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="5c62f-128">Agrega una o más propiedades de tipo pt Object para el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c62f-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c62f-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c62f-129">Remarks</span></span>

<span data-ttu-id="5c62f-130">La interfaz de **IPropData::IMAPIProp** se implementa mediante MAPI y resultan de utilidad para los proveedores de servicios que tienen acceso a esta implementación mediante una llamada a la función [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="5c62f-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="5c62f-131">Para obtener más información acerca de los niveles de acceso en los objetos y propiedades, vea [los permisos de objetos y propiedades](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5c62f-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c62f-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5c62f-132">See also</span></span>



[<span data-ttu-id="5c62f-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5c62f-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

