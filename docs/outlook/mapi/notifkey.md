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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280050"
---
# <a name="notifkey"></a><span data-ttu-id="9d18c-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="9d18c-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="9d18c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d18c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d18c-105">Identifica de forma única una conexión entre un receptor de notificaciones, un origen de notificaciones y MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d18c-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d18c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9d18c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d18c-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="9d18c-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="9d18c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9d18c-108">Members</span></span>

 <span data-ttu-id="9d18c-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="9d18c-109">**cb**</span></span>
  
> <span data-ttu-id="9d18c-110">Número de bytes en el miembro **AB** .</span><span class="sxs-lookup"><span data-stu-id="9d18c-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="9d18c-111">**listín**</span><span class="sxs-lookup"><span data-stu-id="9d18c-111">**ab**</span></span>
  
> <span data-ttu-id="9d18c-112">Matriz de bytes que describe la clave de notificación.</span><span class="sxs-lookup"><span data-stu-id="9d18c-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d18c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d18c-113">Remarks</span></span>

<span data-ttu-id="9d18c-114">Los métodos [subscribe](imapisupport-subscribe.md) y [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) usan la estructura **NOTIFKEY** para generar notificaciones al receptor de notificaciones adecuado sobre el origen de la notificación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9d18c-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="9d18c-115">Los proveedores de servicios generan claves de \*\*\*\* notificación cuando se llama a su método Advise y quieren llamar a **subscribe** para controlar el registro de notificaciones y el envío posterior de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9d18c-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="9d18c-116">Una clave de notificación puede ser el identificador de entrada del origen de Advise o puede ser cualquier otro elemento de identificación, como una constante.</span><span class="sxs-lookup"><span data-stu-id="9d18c-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="9d18c-117">Por ejemplo, un proveedor de almacenamiento de mensajes podría usar la ruta de acceso de una carpeta como su clave de notificación.</span><span class="sxs-lookup"><span data-stu-id="9d18c-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="9d18c-118">La clave de notificación debe funcionar en varios procesos.</span><span class="sxs-lookup"><span data-stu-id="9d18c-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="9d18c-119">Los requisitos de ámbito de una clave de notificación son similares a los de un identificador de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="9d18c-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="9d18c-120">Sin embargo, a diferencia de un identificador de entrada, una clave de notificación debe ser de comparación binaria.</span><span class="sxs-lookup"><span data-stu-id="9d18c-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="9d18c-121">Normalmente, una clave de notificación incluye un valor **GUID** definido por el proveedor de servicios seguido de otra información específica del proveedor que es única para el objeto.</span><span class="sxs-lookup"><span data-stu-id="9d18c-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="9d18c-122">Para obtener una descripción del uso de la estructura **NOTIFKEY** para administrar las conexiones entre los receptores de notificaciones y los objetos que generan las notificaciones, consulte [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="9d18c-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d18c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d18c-123">See also</span></span>



[<span data-ttu-id="9d18c-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="9d18c-124">MAPI Structures</span></span>](mapi-structures.md)

