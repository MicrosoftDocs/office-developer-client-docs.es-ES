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
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429631"
---
# <a name="notifkey"></a><span data-ttu-id="1f728-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="1f728-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="1f728-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f728-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f728-105">Identifica de forma única una conexión entre un receptor de avisos, un origen de aviso y MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f728-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f728-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1f728-106">Header file:</span></span>  <br/> |<span data-ttu-id="1f728-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1f728-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="1f728-108">Members</span><span class="sxs-lookup"><span data-stu-id="1f728-108">Members</span></span>

 <span data-ttu-id="1f728-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="1f728-109">**cb**</span></span>
  
> <span data-ttu-id="1f728-110">Recuento de bytes en el **miembro ab.**</span><span class="sxs-lookup"><span data-stu-id="1f728-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="1f728-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="1f728-111">**ab**</span></span>
  
> <span data-ttu-id="1f728-112">Matriz de bytes que describen la clave de notificación.</span><span class="sxs-lookup"><span data-stu-id="1f728-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f728-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f728-113">Remarks</span></span>

<span data-ttu-id="1f728-114">Los [métodos Subscribe](imapisupport-subscribe.md) y [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usan la estructura **NOTIFKEY** para generar notificaciones al receptor de avisos adecuado sobre el origen de asesoramiento adecuado.</span><span class="sxs-lookup"><span data-stu-id="1f728-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="1f728-115">Los proveedores de servicios generan claves de notificación cuando se llama al método **Advise** y quieren llamar a **Subscribe** para controlar el registro de notificaciones y el envío posterior de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1f728-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="1f728-116">Una clave de notificación puede ser el identificador de entrada del origen del aviso o puede ser cualquier otro elemento de identificación, como una constante.</span><span class="sxs-lookup"><span data-stu-id="1f728-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="1f728-117">Por ejemplo, un proveedor de almacén de mensajes puede usar la ruta de acceso de una carpeta como clave de notificación.</span><span class="sxs-lookup"><span data-stu-id="1f728-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="1f728-118">La clave de notificación debe funcionar en varios procesos.</span><span class="sxs-lookup"><span data-stu-id="1f728-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="1f728-119">Los requisitos de ámbito de una clave de notificación son similares a los de un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="1f728-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="1f728-120">Sin embargo, a diferencia de un identificador de entrada, una clave de notificación debe ser comparable a binarios.</span><span class="sxs-lookup"><span data-stu-id="1f728-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="1f728-121">Normalmente, una clave de notificación incluye un **valor GUID** definido por el proveedor de servicios seguido de otra información específica del proveedor única del objeto.</span><span class="sxs-lookup"><span data-stu-id="1f728-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="1f728-122">Para obtener una explicación del uso de la estructura **NOTIFKEY** para administrar las conexiones entre los receptores de notificaciones y los objetos que generan las notificaciones, vea [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="1f728-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f728-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f728-123">See also</span></span>



[<span data-ttu-id="1f728-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="1f728-124">MAPI Structures</span></span>](mapi-structures.md)

