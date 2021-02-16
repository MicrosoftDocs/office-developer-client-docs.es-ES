---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430171"
---
# <a name="object_notification"></a><span data-ttu-id="2b999-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2b999-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="2b999-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b999-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b999-105">Contiene información sobre un objeto que se ha sometido a un cambio, como copiarse o modificarse.</span><span class="sxs-lookup"><span data-stu-id="2b999-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b999-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2b999-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b999-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b999-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="2b999-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b999-108">Members</span></span>

 <span data-ttu-id="2b999-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="2b999-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="2b999-110">Número de bytes en el identificador de entrada al que apunta el **miembro lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="2b999-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="2b999-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="2b999-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="2b999-112">Puntero al identificador de entrada del objeto afectado.</span><span class="sxs-lookup"><span data-stu-id="2b999-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="2b999-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="2b999-113">**ulObjType**</span></span>
  
> <span data-ttu-id="2b999-114">Tipo de objeto afectado.</span><span class="sxs-lookup"><span data-stu-id="2b999-114">Type of object affected.</span></span> <span data-ttu-id="2b999-115">Los tipos posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2b999-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="2b999-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="2b999-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="2b999-117">Almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2b999-117">Message store.</span></span> 
    
<span data-ttu-id="2b999-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="2b999-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="2b999-119">Libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2b999-119">Address book.</span></span> 
    
<span data-ttu-id="2b999-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="2b999-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="2b999-121">Carpeta.</span><span class="sxs-lookup"><span data-stu-id="2b999-121">Folder.</span></span>
    
<span data-ttu-id="2b999-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="2b999-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="2b999-123">Contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2b999-123">Address book container.</span></span>
    
<span data-ttu-id="2b999-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="2b999-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="2b999-125">Mensaje.</span><span class="sxs-lookup"><span data-stu-id="2b999-125">Message.</span></span>
    
<span data-ttu-id="2b999-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="2b999-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="2b999-127">Usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2b999-127">Messaging user.</span></span>
    
<span data-ttu-id="2b999-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="2b999-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="2b999-129">Datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2b999-129">Attachment.</span></span>
    
<span data-ttu-id="2b999-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="2b999-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="2b999-131">Lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="2b999-131">Distribution list.</span></span>
    
<span data-ttu-id="2b999-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="2b999-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="2b999-133">Sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="2b999-133">Profile section.</span></span>
    
<span data-ttu-id="2b999-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="2b999-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="2b999-135">Objeto Status.</span><span class="sxs-lookup"><span data-stu-id="2b999-135">Status object.</span></span>
    
<span data-ttu-id="2b999-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="2b999-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="2b999-137">Objeto Session.</span><span class="sxs-lookup"><span data-stu-id="2b999-137">Session object.</span></span>
    
 <span data-ttu-id="2b999-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="2b999-138">**cbParentID**</span></span>
  
> <span data-ttu-id="2b999-139">Recuento de bytes en el identificador de entrada al que apunta el **miembro lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="2b999-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="2b999-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="2b999-140">**lpParentID**</span></span>
  
> <span data-ttu-id="2b999-141">Puntero al identificador de entrada del objeto primario del objeto afectado.</span><span class="sxs-lookup"><span data-stu-id="2b999-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="2b999-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="2b999-142">**cbOldID**</span></span>
  
> <span data-ttu-id="2b999-143">Recuento de bytes en el identificador de entrada al que apunta el **miembro lpOldID.**</span><span class="sxs-lookup"><span data-stu-id="2b999-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="2b999-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="2b999-144">**lpOldID**</span></span>
  
> <span data-ttu-id="2b999-145">Puntero al identificador de entrada del objeto original.</span><span class="sxs-lookup"><span data-stu-id="2b999-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="2b999-146">Este puntero puede ser NULL si el evento no requiere un objeto original.</span><span class="sxs-lookup"><span data-stu-id="2b999-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="2b999-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="2b999-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="2b999-148">Recuento de bytes en el identificador de entrada al que apunta el **miembro lpOldParentID.**</span><span class="sxs-lookup"><span data-stu-id="2b999-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="2b999-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="2b999-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="2b999-150">Puntero al identificador de entrada del objeto primario del objeto original.</span><span class="sxs-lookup"><span data-stu-id="2b999-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="2b999-151">Este puntero puede ser NULL si el evento no requiere un objeto original.</span><span class="sxs-lookup"><span data-stu-id="2b999-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="2b999-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="2b999-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="2b999-153">Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene las etiquetas de propiedad que identifican las propiedades afectadas por el evento.</span><span class="sxs-lookup"><span data-stu-id="2b999-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2b999-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b999-154">Remarks</span></span>

<span data-ttu-id="2b999-155">La **OBJECT_NOTIFICATION** es uno de los miembros de la unión de estructuras incluidas en el miembro **de** información de la [estructura notification.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="2b999-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="2b999-156">Cuando el miembro  **de** información de una estructura notification contiene una estructura **OBJECT_NOTIFICATION,** el miembro **ulEventType** de la estructura **NOTIFICATION** se establece en uno de los siguientes tipos de eventos:</span><span class="sxs-lookup"><span data-stu-id="2b999-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="2b999-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="2b999-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="2b999-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="2b999-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="2b999-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="2b999-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="2b999-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="2b999-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="2b999-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="2b999-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="2b999-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="2b999-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="2b999-163">El evento de búsqueda completa, representado por el tipo de evento fnevSearchComplete, indica que se ha completado la búsqueda inicial del dominio para una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2b999-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="2b999-164">Los siguientes miembros que contienen información sobre el objeto original solo se usan en eventos de movimiento y copia.</span><span class="sxs-lookup"><span data-stu-id="2b999-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="2b999-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="2b999-165">**cbOldID**</span></span>
    
- <span data-ttu-id="2b999-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="2b999-166">**lpOldID**</span></span>
    
- <span data-ttu-id="2b999-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="2b999-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="2b999-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="2b999-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="2b999-169">Estos miembros no se aplican a los otros tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b999-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="2b999-170">Para obtener más información acerca de la notificación, consulte los temas descritos en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2b999-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="2b999-171">**Tema**</span><span class="sxs-lookup"><span data-stu-id="2b999-171">**Topic**</span></span>|<span data-ttu-id="2b999-172">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b999-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b999-173">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="2b999-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="2b999-174">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="2b999-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="2b999-175">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="2b999-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="2b999-176">Discusión sobre cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2b999-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="2b999-177">Notificación de eventos de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="2b999-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="2b999-178">Discusión sobre cómo los proveedores de servicios pueden usar [el método IMAPISupport](imapisupportiunknown.md) para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="2b999-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b999-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2b999-179">See also</span></span>



[<span data-ttu-id="2b999-180">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="2b999-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="2b999-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="2b999-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="2b999-182">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="2b999-182">MAPI Structures</span></span>](mapi-structures.md)

