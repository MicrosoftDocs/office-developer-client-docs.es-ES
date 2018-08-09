---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816310"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="dfb9e-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="dfb9e-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="dfb9e-104">Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="dfb9e-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dfb9e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="dfb9e-105">Quick info</span></span>

<span data-ttu-id="dfb9e-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="dfb9e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfb9e-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dfb9e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="dfb9e-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="dfb9e-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="dfb9e-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="dfb9e-109">Property type:</span></span>  <br/> |<span data-ttu-id="dfb9e-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dfb9e-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dfb9e-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="dfb9e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="dfb9e-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="dfb9e-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="dfb9e-113">Access:</span><span class="sxs-lookup"><span data-stu-id="dfb9e-113">Access:</span></span>  <br/> |<span data-ttu-id="dfb9e-114">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dfb9e-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfb9e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfb9e-115">Remarks</span></span>

<span data-ttu-id="dfb9e-116">Obtener o establecer esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md) o [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dfb9e-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="dfb9e-117">Uno de los efectos secundarios de la configuración de un almacén como el almacén de entrega predeterminado para una cuenta es que, al iniciar Outlook, Outlook crea las carpetas de búsqueda de ese almacén si no está ya no existe y el almacenamiento en la barra Tareas pendientes de lista.</span><span class="sxs-lookup"><span data-stu-id="dfb9e-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dfb9e-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfb9e-118">See also</span></span>

- [<span data-ttu-id="dfb9e-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="dfb9e-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="dfb9e-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="dfb9e-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

