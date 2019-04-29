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
# <a name="errornotification"></a><span data-ttu-id="8c12f-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8c12f-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="8c12f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c12f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c12f-105">Describe la información relacionada con un error crítico.</span><span class="sxs-lookup"><span data-stu-id="8c12f-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="8c12f-106">Esto hace que se genere una notificación de error.</span><span class="sxs-lookup"><span data-stu-id="8c12f-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c12f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8c12f-107">Header file:</span></span>  <br/> |<span data-ttu-id="8c12f-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8c12f-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="8c12f-109">Members</span><span class="sxs-lookup"><span data-stu-id="8c12f-109">Members</span></span>

 <span data-ttu-id="8c12f-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="8c12f-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="8c12f-111">Número de bytes en el identificador de entrada al que apunta **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="8c12f-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="8c12f-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="8c12f-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="8c12f-113">Puntero al identificador de entrada del objeto que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="8c12f-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="8c12f-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="8c12f-114">**scode**</span></span>
  
> <span data-ttu-id="8c12f-115">Valor de error para el error crítico.</span><span class="sxs-lookup"><span data-stu-id="8c12f-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="8c12f-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="8c12f-116">**ulFlags**</span></span>
  
> <span data-ttu-id="8c12f-117">Máscara de la máscara usada para designar el formato del texto al que señala el miembro **lpszError** en la estructura a la que apunta **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="8c12f-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="8c12f-118">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="8c12f-118">The following flag can be set:</span></span>
    
<span data-ttu-id="8c12f-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8c12f-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8c12f-120">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8c12f-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8c12f-121">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8c12f-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8c12f-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="8c12f-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="8c12f-123">Puntero a una estructura [MAPIERROR](mapierror.md) que describe el error.</span><span class="sxs-lookup"><span data-stu-id="8c12f-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8c12f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c12f-124">Remarks</span></span>

<span data-ttu-id="8c12f-125">La estructura **ERROR_NOTIFICATION** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="8c12f-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="8c12f-126">Cuando el miembro de **información** de una estructura de **notificación** contiene una estructura **ERROR_NOTIFICATION** , el miembro **ulEventType** de la estructura de **notificación** se establece en _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="8c12f-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="8c12f-127">El valor del miembro **cbEntryID** y el miembro **LPENTRYID** puede ser null.</span><span class="sxs-lookup"><span data-stu-id="8c12f-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="8c12f-128">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c12f-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="8c12f-129">**Tema**</span><span class="sxs-lookup"><span data-stu-id="8c12f-129">**Topic**</span></span>|<span data-ttu-id="8c12f-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c12f-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c12f-131">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="8c12f-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="8c12f-132">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="8c12f-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="8c12f-133">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="8c12f-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="8c12f-134">Descripción de cómo deben administrar los clientes las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c12f-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="8c12f-135">Admitir notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="8c12f-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="8c12f-136">Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c12f-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c12f-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="8c12f-137">See also</span></span>



[<span data-ttu-id="8c12f-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8c12f-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8c12f-139">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="8c12f-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="8c12f-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8c12f-140">MAPI Structures</span></span>](mapi-structures.md)

