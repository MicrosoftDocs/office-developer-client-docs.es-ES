---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327674"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="59aea-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="59aea-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="59aea-104">Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="59aea-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="59aea-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="59aea-105">Quick info</span></span>

<span data-ttu-id="59aea-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="59aea-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59aea-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="59aea-107">Identifier:</span></span>  <br/> |<span data-ttu-id="59aea-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="59aea-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="59aea-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="59aea-109">Property type:</span></span>  <br/> |<span data-ttu-id="59aea-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="59aea-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="59aea-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="59aea-111">Property tag:</span></span>  <br/> |<span data-ttu-id="59aea-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="59aea-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="59aea-113">Al</span><span class="sxs-lookup"><span data-stu-id="59aea-113">Access:</span></span>  <br/> |<span data-ttu-id="59aea-114">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="59aea-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59aea-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59aea-115">Remarks</span></span>

<span data-ttu-id="59aea-116">Obtenga o establezca esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md) o [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="59aea-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="59aea-117">Uno de los efectos secundarios de establecer un almacén como el almacén de entrega predeterminado para una cuenta es que al iniciar Outlook, Outlook crea carpetas de búsqueda para ese almacén si todavía no existen y muestra el almacén en la barra tareas pendientes.</span><span class="sxs-lookup"><span data-stu-id="59aea-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59aea-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="59aea-118">See also</span></span>

- [<span data-ttu-id="59aea-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="59aea-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="59aea-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="59aea-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

