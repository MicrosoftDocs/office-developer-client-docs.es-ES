---
title: NEWMAIL_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NEWMAIL_NOTIFICATION
api_type:
- COM
ms.assetid: 49913050-900a-4b05-84c4-c596a93ce68b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 779585f73a7032ae0259b30ebfc16868c733c7fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569515"
---
# <a name="newmailnotification"></a><span data-ttu-id="50bcc-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="50bcc-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="50bcc-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50bcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50bcc-105">Describe la información que se relacionan con la llegada de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="50bcc-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50bcc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="50bcc-106">Header file:</span></span>  <br/> |<span data-ttu-id="50bcc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50bcc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _NEWMAIL_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG ulFlags;
  LPSTR lpszMessageClass;
  ULONG ulMessageFlags;
} NEWMAIL_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="50bcc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="50bcc-108">Members</span></span>

 <span data-ttu-id="50bcc-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="50bcc-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="50bcc-110">Recuento de bytes en el identificador de entrada que señala el miembro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="50bcc-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="50bcc-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="50bcc-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="50bcc-112">Puntero al identificador de entrada del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="50bcc-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="50bcc-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="50bcc-113">**cbParentID**</span></span>
  
> <span data-ttu-id="50bcc-114">Recuento de bytes en el identificador de entrada que señala el miembro **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="50bcc-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="50bcc-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="50bcc-115">**lpParentID**</span></span>
  
> <span data-ttu-id="50bcc-116">Puntero al identificador de entrada de la carpeta de recepción para el mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="50bcc-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="50bcc-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="50bcc-117">**ulFlags**</span></span>
  
> <span data-ttu-id="50bcc-118">Máscara de bits de indicadores que se utilizan para describir el formato de las propiedades de cadena incluido con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="50bcc-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="50bcc-119">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="50bcc-119">The following flag can be set:</span></span>
    
<span data-ttu-id="50bcc-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50bcc-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="50bcc-121">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="50bcc-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="50bcc-122">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="50bcc-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="50bcc-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="50bcc-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="50bcc-124">Puntero a la clase de mensaje del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="50bcc-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="50bcc-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="50bcc-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="50bcc-126">Máscara de bits de indicadores que describe el estado actual del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="50bcc-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="50bcc-127">El miembro **ulMessageFlags** es una copia de la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="50bcc-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50bcc-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50bcc-128">Remarks</span></span>

<span data-ttu-id="50bcc-129">La estructura **NEWMAIL_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="50bcc-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="50bcc-130">Cuando el miembro de la **información** de una estructura de **notificación** contiene una estructura **NEWMAIL_NOTIFICATION** , se establece el miembro **ulEventType** de la estructura de **notificación** en _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="50bcc-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="50bcc-131">MAPI utiliza la estructura **NEWMAIL_NOTIFICATION** sólo como un miembro de la estructura de **notificación** , que contiene información acerca de un evento de notificación para el receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="50bcc-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="50bcc-132">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="50bcc-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="50bcc-133">**Tema**</span><span class="sxs-lookup"><span data-stu-id="50bcc-133">**Topic**</span></span>|<span data-ttu-id="50bcc-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50bcc-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50bcc-135">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="50bcc-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="50bcc-136">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="50bcc-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="50bcc-137">Administrar notificaciones</span><span class="sxs-lookup"><span data-stu-id="50bcc-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="50bcc-138">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="50bcc-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="50bcc-139">Compatibilidad con la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="50bcc-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="50bcc-140">Explicación de cómo los proveedores de servicios pueden usar el método [IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="50bcc-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50bcc-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="50bcc-141">See also</span></span>



[<span data-ttu-id="50bcc-142">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="50bcc-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="50bcc-143">Propiedad canónico PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="50bcc-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="50bcc-144">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="50bcc-144">MAPI Structures</span></span>](mapi-structures.md)

