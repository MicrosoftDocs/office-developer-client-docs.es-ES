---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ba93cd0343121751ab12514fe3f09e5a480d5b23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582276"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="1baa9-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1baa9-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="1baa9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1baa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1baa9-105">Describe un objeto de estado que se ha visto afectado por un cambio.</span><span class="sxs-lookup"><span data-stu-id="1baa9-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1baa9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1baa9-106">Header file:</span></span>  <br/> |<span data-ttu-id="1baa9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1baa9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="1baa9-108">Members</span><span class="sxs-lookup"><span data-stu-id="1baa9-108">Members</span></span>

 <span data-ttu-id="1baa9-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="1baa9-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="1baa9-110">Recuento de bytes en el identificador de entrada que señala el miembro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="1baa9-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="1baa9-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="1baa9-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="1baa9-112">Puntero al identificador de entrada del objeto estado cambiado.</span><span class="sxs-lookup"><span data-stu-id="1baa9-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="1baa9-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="1baa9-113">**cValues**</span></span>
  
> <span data-ttu-id="1baa9-114">Recuento de las estructuras de [SPropValue](spropvalue.md) en la matriz indicada por el miembro **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="1baa9-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="1baa9-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="1baa9-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="1baa9-116">Puntero a una matriz de estructuras **SPropValue** que describen las propiedades del objeto de estado cambiado.</span><span class="sxs-lookup"><span data-stu-id="1baa9-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1baa9-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1baa9-117">Remarks</span></span>

<span data-ttu-id="1baa9-118">La estructura **STATUS_OBJECT_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1baa9-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="1baa9-119">La estructura **STATUS_OBJECT_NOTIFICATION** se incluye con una notificación de objeto de estado para un evento de tipo _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="1baa9-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="1baa9-120">Notificación de estado de objeto es una notificación de MAPI interno; los clientes y proveedores de servicios no se pueden registrar para él y proveedores de servicios lo no pueden generar.</span><span class="sxs-lookup"><span data-stu-id="1baa9-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="1baa9-121">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1baa9-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="1baa9-122">**Tema**</span><span class="sxs-lookup"><span data-stu-id="1baa9-122">**Topic**</span></span>|<span data-ttu-id="1baa9-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1baa9-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1baa9-124">Notificación de eventos de MAPI</span><span class="sxs-lookup"><span data-stu-id="1baa9-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="1baa9-125">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="1baa9-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="1baa9-126">Administrar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="1baa9-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="1baa9-127">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1baa9-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="1baa9-128">Admitir notificaciones de eventos</span><span class="sxs-lookup"><span data-stu-id="1baa9-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="1baa9-129">Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1baa9-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1baa9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1baa9-130">See also</span></span>



[<span data-ttu-id="1baa9-131">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="1baa9-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="1baa9-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1baa9-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1baa9-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="1baa9-133">MAPI Structures</span></span>](mapi-structures.md)

