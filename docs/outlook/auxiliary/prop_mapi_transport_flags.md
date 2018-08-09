---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de interfaz (IU) de usuario que no es compatible con la cuenta.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816323"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="f9471-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f9471-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="f9471-104">Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de interfaz (IU) de usuario que no es compatible con la cuenta.</span><span class="sxs-lookup"><span data-stu-id="f9471-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f9471-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f9471-105">Quick info</span></span>

<span data-ttu-id="f9471-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f9471-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9471-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f9471-107">Identifier:</span></span>  <br/> |<span data-ttu-id="f9471-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="f9471-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="f9471-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="f9471-109">Property type:</span></span>  <br/> |<span data-ttu-id="f9471-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f9471-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f9471-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="f9471-111">Property tag:</span></span>  <br/> |<span data-ttu-id="f9471-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="f9471-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="f9471-113">Access:</span><span class="sxs-lookup"><span data-stu-id="f9471-113">Access:</span></span>  <br/> |<span data-ttu-id="f9471-114">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f9471-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9471-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9471-115">Remarks</span></span>

<span data-ttu-id="f9471-116">Obtener o establecer esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md) o [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f9471-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="f9471-117">Devuelve **MAPIACCT_SEND_ONLY** si la cuenta sólo puede enviar mensajes pero no puede recibir los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f9471-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="f9471-118">En este caso, Outlook deshabilita la interfaz de usuario que no se aplica a este tipo de cuentas (por ejemplo, en la interfaz de usuario para el **Envío o recepción**).</span><span class="sxs-lookup"><span data-stu-id="f9471-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9471-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9471-119">See also</span></span>

- [<span data-ttu-id="f9471-120">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="f9471-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="f9471-121">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="f9471-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

