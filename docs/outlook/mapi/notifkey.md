---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 36b8381e2bf98f5ddcb88a54b56f2b5c91b3b668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572602"
---
# <a name="notifkey"></a><span data-ttu-id="ed607-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="ed607-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="ed607-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed607-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed607-105">Identifica exclusivamente una conexión entre un receptor con notificación, un origen de advise y MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed607-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed607-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ed607-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed607-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ed607-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="ed607-108">Members</span><span class="sxs-lookup"><span data-stu-id="ed607-108">Members</span></span>

 <span data-ttu-id="ed607-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="ed607-109">**cb**</span></span>
  
> <span data-ttu-id="ed607-110">Recuento de bytes en el miembro **ab** .</span><span class="sxs-lookup"><span data-stu-id="ed607-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="ed607-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="ed607-111">**ab**</span></span>
  
> <span data-ttu-id="ed607-112">Matriz de bytes que describe la clave de notificación.</span><span class="sxs-lookup"><span data-stu-id="ed607-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed607-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed607-113">Remarks</span></span>

<span data-ttu-id="ed607-114">Los métodos [suscribir](imapisupport-subscribe.md) y [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usan la estructura **NOTIFKEY** para generar las notificaciones para el receptor de notificaciones adecuados sobre el origen de advise adecuado.</span><span class="sxs-lookup"><span data-stu-id="ed607-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="ed607-115">Proveedores de servicios de generan claves de notificación cuando se llama a su método **Advise** y deseen llamar **suscribirse** para controlar el registro de la notificación y el envío subsiguientes de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ed607-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="ed607-116">Una clave de notificación puede ser el identificador de entrada del origen de advise o puede ser cualquier otro elemento de identificación, como una constante.</span><span class="sxs-lookup"><span data-stu-id="ed607-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="ed607-117">Por ejemplo, un proveedor de almacén de mensajes es posible que use la ruta de acceso de una carpeta como su clave de notificación.</span><span class="sxs-lookup"><span data-stu-id="ed607-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="ed607-118">La clave de notificación debe trabajar a través de varios procesos.</span><span class="sxs-lookup"><span data-stu-id="ed607-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="ed607-119">Los requisitos de ámbito para una clave de notificación son similares a las de un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="ed607-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="ed607-120">Sin embargo, a diferencia de un identificador de entrada, una clave de notificación debe ser binario comparable.</span><span class="sxs-lookup"><span data-stu-id="ed607-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="ed607-121">Normalmente, una clave de notificación incluye un valor **GUID** definido por el proveedor de servicios seguido de otra información específica del proveedor único para el objeto.</span><span class="sxs-lookup"><span data-stu-id="ed607-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="ed607-122">Para obtener una descripción del uso de la estructura **NOTIFKEY** para administrar las conexiones entre los receptores advise y los objetos que generan las notificaciones, vea [Compatibilidad con notificación de evento](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ed607-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed607-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed607-123">See also</span></span>



[<span data-ttu-id="ed607-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="ed607-124">MAPI Structures</span></span>](mapi-structures.md)

