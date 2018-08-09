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
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816774"
---
# <a name="errornotification"></a><span data-ttu-id="d801c-103">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d801c-103">ERROR_NOTIFICATION</span></span>

  
  
<span data-ttu-id="d801c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d801c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d801c-105">Describe la información que se relacionan con un error crítico.</span><span class="sxs-lookup"><span data-stu-id="d801c-105">Describes information that relate to a critical error.</span></span> <span data-ttu-id="d801c-106">Esto hace que se genere una notificación de error.</span><span class="sxs-lookup"><span data-stu-id="d801c-106">This causes an error notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d801c-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d801c-107">Header file:</span></span>  <br/> |<span data-ttu-id="d801c-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d801c-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d801c-109">Members</span><span class="sxs-lookup"><span data-stu-id="d801c-109">Members</span></span>

 <span data-ttu-id="d801c-110">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="d801c-110">**cbEntryID**</span></span>
  
> <span data-ttu-id="d801c-111">Recuento de bytes en el identificador de entrada que señala **lpEntryID**.</span><span class="sxs-lookup"><span data-stu-id="d801c-111">Count of bytes in the entry identifier pointed to by **lpEntryID**.</span></span> 
    
 <span data-ttu-id="d801c-112">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="d801c-112">**lpEntryID**</span></span>
  
> <span data-ttu-id="d801c-113">Puntero al identificador de entrada del objeto que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="d801c-113">Pointer to the entry identifier of the object that causes the error.</span></span>
    
 <span data-ttu-id="d801c-114">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="d801c-114">**scode**</span></span>
  
> <span data-ttu-id="d801c-115">Valor de error para el error crítico.</span><span class="sxs-lookup"><span data-stu-id="d801c-115">Error value for the critical error.</span></span> 
    
 <span data-ttu-id="d801c-116">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d801c-116">**ulFlags**</span></span>
  
> <span data-ttu-id="d801c-117">Máscara de bits de indicadores que se utilizan para designar el formato del texto que señala el miembro **lpszError** en la estructura que señala **lpMAPIError**.</span><span class="sxs-lookup"><span data-stu-id="d801c-117">Bitmask of flags used to designate the format of the text pointed to by the **lpszError** member in the structure pointed to by **lpMAPIError**.</span></span> <span data-ttu-id="d801c-118">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="d801c-118">The following flag can be set:</span></span>
    
<span data-ttu-id="d801c-119">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d801c-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d801c-120">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d801c-120">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d801c-121">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d801c-121">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d801c-122">**lpMAPIError**</span><span class="sxs-lookup"><span data-stu-id="d801c-122">**lpMAPIError**</span></span>
  
> <span data-ttu-id="d801c-123">Puntero a una estructura [MAPIERROR](mapierror.md) que describe el error.</span><span class="sxs-lookup"><span data-stu-id="d801c-123">Pointer to a [MAPIERROR](mapierror.md) structure describing the error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d801c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d801c-124">Remarks</span></span>

<span data-ttu-id="d801c-125">La estructura **ERROR_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d801c-125">The **ERROR_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="d801c-126">Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **ERROR_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevCriticalError_.</span><span class="sxs-lookup"><span data-stu-id="d801c-126">When the **info** member of a **NOTIFICATION** structure contains an **ERROR_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevCriticalError_.</span></span>
  
<span data-ttu-id="d801c-127">El valor del miembro **cbEntryID** y el miembro **lpEntryID** puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d801c-127">The value of the **cbEntryID** member and the **lpEntryID** member can be NULL.</span></span> 
  
<span data-ttu-id="d801c-128">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d801c-128">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d801c-129">**Tema**</span><span class="sxs-lookup"><span data-stu-id="d801c-129">**Topic**</span></span>|<span data-ttu-id="d801c-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d801c-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d801c-131">Notificación de eventos de MAPI</span><span class="sxs-lookup"><span data-stu-id="d801c-131">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d801c-132">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="d801c-132">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d801c-133">Administrar las notificaciones</span><span class="sxs-lookup"><span data-stu-id="d801c-133">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d801c-134">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d801c-134">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d801c-135">Admitir notificaciones de eventos</span><span class="sxs-lookup"><span data-stu-id="d801c-135">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d801c-136">Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d801c-136">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d801c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d801c-137">See also</span></span>



[<span data-ttu-id="d801c-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d801c-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d801c-139">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="d801c-139">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="d801c-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d801c-140">MAPI Structures</span></span>](mapi-structures.md)

