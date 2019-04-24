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
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336445"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="b6b5f-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b6b5f-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="b6b5f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b5f-105">Describe un objeto status que se ha visto afectado por un cambio.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6b5f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b6b5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="b6b5f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b6b5f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="b6b5f-108">Members</span><span class="sxs-lookup"><span data-stu-id="b6b5f-108">Members</span></span>

 <span data-ttu-id="b6b5f-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="b6b5f-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="b6b5f-110">Número de bytes en el identificador de entrada al que apunta el miembro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="b6b5f-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="b6b5f-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="b6b5f-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="b6b5f-112">Puntero al identificador de entrada del objeto de estado Changed.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="b6b5f-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b6b5f-113">**cValues**</span></span>
  
> <span data-ttu-id="b6b5f-114">Número de estructuras [SPropValue](spropvalue.md) en la matriz señalada por el miembro **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="b6b5f-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="b6b5f-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="b6b5f-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="b6b5f-116">Puntero a una matriz de estructuras **SPropValue** que describen las propiedades del objeto status modificado.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b6b5f-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6b5f-117">Remarks</span></span>

<span data-ttu-id="b6b5f-118">La estructura **STATUS_OBJECT_NOTIFICATION** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b5f-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b6b5f-119">La estructura **STATUS_OBJECT_NOTIFICATION** se incluye con una notificación de objeto de estado para un evento de tipo _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="b6b5f-120">La notificación de objeto de estado es una notificación de MAPI interna; los clientes y los proveedores de servicios no pueden registrarse para ti y los proveedores de servicios no pueden generarlos.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="b6b5f-121">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b6b5f-122">**Tema**</span><span class="sxs-lookup"><span data-stu-id="b6b5f-122">**Topic**</span></span>|<span data-ttu-id="b6b5f-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6b5f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6b5f-124">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b5f-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b6b5f-125">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b6b5f-126">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="b6b5f-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b6b5f-127">Descripción de cómo deben administrar los clientes las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b6b5f-128">Admitir notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="b6b5f-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b6b5f-129">Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b6b5f-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6b5f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6b5f-130">See also</span></span>



[<span data-ttu-id="b6b5f-131">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="b6b5f-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="b6b5f-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b6b5f-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b6b5f-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b5f-133">MAPI Structures</span></span>](mapi-structures.md)

