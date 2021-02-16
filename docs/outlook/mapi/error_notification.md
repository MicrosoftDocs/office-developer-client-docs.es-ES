---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425445"
---
# <a name="error_notification"></a><span data-ttu-id="2b785-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2b785-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="2b785-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b785-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b785-105">Describe la información relacionada con un error crítico.</span><span class="sxs-lookup"><span data-stu-id="2b785-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="2b785-106">Esto hace que se genere una notificación de error.</span><span class="sxs-lookup"><span data-stu-id="2b785-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b785-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2b785-107">Header file:</span></span>  <br/> |<span data-ttu-id="2b785-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b785-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a><span data-ttu-id="2b785-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b785-109">Members</span></span>

 <span data-ttu-id="2b785-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="2b785-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="2b785-111">Recuento de bytes en el identificador de entrada al que apunta **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="2b785-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="2b785-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="2b785-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="2b785-113">Puntero al identificador de entrada del objeto que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="2b785-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="2b785-114">**scode**</span><span class="sxs-lookup"><span data-stu-id="2b785-114">**scode**</span></span>
  
> <span data-ttu-id="2b785-115">Valor de error del error crítico.</span><span class="sxs-lookup"><span data-stu-id="2b785-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="2b785-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2b785-116">**ulFlags**</span></span>
  
> <span data-ttu-id="2b785-117">Máscara de bits de marcas usadas para designar el formato del texto al que apunta el miembro **lpszError** en la estructura a la que apunta **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="2b785-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="2b785-118">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="2b785-118">The following flag can be set:</span></span>
    
<span data-ttu-id="2b785-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b785-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2b785-120">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b785-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="2b785-121">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2b785-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="2b785-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="2b785-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="2b785-123">Puntero a una [estructura MAPIERROR](mapierror.md) que describe el error.</span><span class="sxs-lookup"><span data-stu-id="2b785-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2b785-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b785-124">Remarks</span></span>

<span data-ttu-id="2b785-125">La **ERROR_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de información** de la estructura [de](notification.md) notificación.</span><span class="sxs-lookup"><span data-stu-id="2b785-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="2b785-126">Cuando el **miembro**  de información de una estructura notification contiene una estructura **ERROR_NOTIFICATION,** el miembro **ulEventType** de la estructura **NOTIFICATION** se establece en _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="2b785-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="2b785-127">El valor del **miembro cbEntryID** y **el miembro lpEntryID** puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2b785-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="2b785-128">Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2b785-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="2b785-129">**Tema**</span><span class="sxs-lookup"><span data-stu-id="2b785-129">**Topic**</span></span>|<span data-ttu-id="2b785-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b785-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b785-131">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="2b785-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="2b785-132">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="2b785-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="2b785-133">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="2b785-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="2b785-134">Discusión sobre cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2b785-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="2b785-135">Notificación de eventos de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="2b785-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="2b785-136">Discusión sobre cómo los proveedores de servicios pueden usar **el método IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2b785-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b785-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2b785-137">See also</span></span>



[<span data-ttu-id="2b785-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2b785-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2b785-139">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="2b785-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="2b785-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="2b785-140">MAPI Structures</span></span>](mapi-structures.md)

