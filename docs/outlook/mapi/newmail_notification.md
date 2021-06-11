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
ms.openlocfilehash: 25af1c1b05618d4f36a43721e71be6ff5c7c597f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439859"
---
# <a name="newmail_notification"></a><span data-ttu-id="9e409-103">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9e409-103">NEWMAIL_NOTIFICATION</span></span>

  
  
<span data-ttu-id="9e409-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e409-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e409-105">Describe la información relacionada con la llegada de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e409-105">Describes information that relate to the arrival of a new message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e409-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9e409-106">Header file:</span></span>  <br/> |<span data-ttu-id="9e409-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e409-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="9e409-108">Members</span><span class="sxs-lookup"><span data-stu-id="9e409-108">Members</span></span>

 <span data-ttu-id="9e409-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="9e409-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="9e409-110">Recuento de bytes en el identificador de entrada al que apunta el **miembro lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="9e409-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="9e409-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="9e409-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="9e409-112">Puntero al identificador de entrada del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="9e409-112">Pointer to the entry identifier of the newly arrived message.</span></span>
    
 <span data-ttu-id="9e409-113">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="9e409-113">**cbParentID**</span></span>
  
> <span data-ttu-id="9e409-114">Recuento de bytes en el identificador de entrada al que apunta el **miembro lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="9e409-114">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="9e409-115">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="9e409-115">**lpParentID**</span></span>
  
> <span data-ttu-id="9e409-116">Puntero al identificador de entrada de la carpeta de recepción del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="9e409-116">Pointer to the entry identifier of the receive folder for the newly arrived message.</span></span>
    
 <span data-ttu-id="9e409-117">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9e409-117">**ulFlags**</span></span>
  
> <span data-ttu-id="9e409-118">Máscara de bits de marcas usadas para describir el formato de las propiedades de cadena incluidas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e409-118">Bitmask of flags used to describe the format of the string properties included with the message.</span></span> <span data-ttu-id="9e409-119">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="9e409-119">The following flag can be set:</span></span>
    
<span data-ttu-id="9e409-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e409-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e409-121">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e409-121">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9e409-122">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e409-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9e409-123">**lpszMessageClass**</span><span class="sxs-lookup"><span data-stu-id="9e409-123">**lpszMessageClass**</span></span>
  
> <span data-ttu-id="9e409-124">Puntero a la clase de mensaje del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="9e409-124">Pointer to the message class of the newly arrived message.</span></span> 
    
 <span data-ttu-id="9e409-125">**ulMessageFlags**</span><span class="sxs-lookup"><span data-stu-id="9e409-125">**ulMessageFlags**</span></span>
  
> <span data-ttu-id="9e409-126">Máscara de bits de marcas que describe el estado actual del mensaje recién llegado.</span><span class="sxs-lookup"><span data-stu-id="9e409-126">Bitmask of flags that describes the current state of the newly arrived message.</span></span> <span data-ttu-id="9e409-127">El **miembro ulMessageFlags** es una copia de la propiedad PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e409-127">The **ulMessageFlags** member is a copy of the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e409-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e409-128">Remarks</span></span>

<span data-ttu-id="9e409-129">La **NEWMAIL_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el **miembro de información** de la estructura [notification.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="9e409-129">The **NEWMAIL_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="9e409-130">Cuando el **miembro de** información de una estructura **NOTIFICATION** contiene una estructura **NEWMAIL_NOTIFICATION,** el **miembro ulEventType** de la estructura **NOTIFICATION** se establece en  _fnevNewMail._</span><span class="sxs-lookup"><span data-stu-id="9e409-130">When the **info** member of a **NOTIFICATION** structure contains a **NEWMAIL_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevNewMail._</span></span>
  
<span data-ttu-id="9e409-131">MAPI usa la **NEWMAIL_NOTIFICATION** solo como miembro de la estructura **NOTIFICATION,** que contiene información sobre un evento de notificación para el receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9e409-131">MAPI uses the **NEWMAIL_NOTIFICATION** structure only as a member of the **NOTIFICATION** structure, which holds information about a notification event for the advise sink.</span></span> 
  
<span data-ttu-id="9e409-132">Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e409-132">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="9e409-133">**Tema**</span><span class="sxs-lookup"><span data-stu-id="9e409-133">**Topic**</span></span>|<span data-ttu-id="9e409-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e409-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e409-135">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="9e409-135">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="9e409-136">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="9e409-136">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="9e409-137">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="9e409-137">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="9e409-138">Discusión sobre cómo los clientes deben administrar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9e409-138">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="9e409-139">Notificación de eventos de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="9e409-139">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="9e409-140">Discusión sobre cómo los proveedores de servicios pueden usar [el método IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9e409-140">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e409-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e409-141">See also</span></span>



[<span data-ttu-id="9e409-142">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="9e409-142">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="9e409-143">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="9e409-143">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)


[<span data-ttu-id="9e409-144">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="9e409-144">MAPI Structures</span></span>](mapi-structures.md)

