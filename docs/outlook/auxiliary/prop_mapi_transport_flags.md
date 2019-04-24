---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y deshabilitar los elementos de la interfaz de usuario (UI) que no son compatibles con la cuenta.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326484"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="be834-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="be834-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="be834-104">Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y deshabilitar los elementos de la interfaz de usuario (UI) que no son compatibles con la cuenta.</span><span class="sxs-lookup"><span data-stu-id="be834-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="be834-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="be834-105">Quick info</span></span>

<span data-ttu-id="be834-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="be834-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be834-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be834-107">Identifier:</span></span>  <br/> |<span data-ttu-id="be834-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="be834-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="be834-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="be834-109">Property type:</span></span>  <br/> |<span data-ttu-id="be834-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="be834-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="be834-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="be834-111">Property tag:</span></span>  <br/> |<span data-ttu-id="be834-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="be834-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="be834-113">Al</span><span class="sxs-lookup"><span data-stu-id="be834-113">Access:</span></span>  <br/> |<span data-ttu-id="be834-114">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="be834-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be834-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be834-115">Remarks</span></span>

<span data-ttu-id="be834-116">Obtenga o establezca esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md) o [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="be834-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="be834-117">Devuelve **MAPIACCT_SEND_ONLY** si la cuenta solo puede enviar mensajes, pero no puede recibirlos.</span><span class="sxs-lookup"><span data-stu-id="be834-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="be834-118">En este caso, Outlook deshabilita la interfaz de usuario que no se aplica a este tipo de cuentas (por ejemplo, la interfaz de usuario para el **envío o recepción**).</span><span class="sxs-lookup"><span data-stu-id="be834-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be834-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="be834-119">See also</span></span>

- [<span data-ttu-id="be834-120">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="be834-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="be834-121">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="be834-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

