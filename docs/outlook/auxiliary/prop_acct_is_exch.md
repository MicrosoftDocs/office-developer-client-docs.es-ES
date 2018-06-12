---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Es True si la cuenta es una cuenta de Exchange.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816307"
---
# <a name="propacctisexch"></a><span data-ttu-id="7deae-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="7deae-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="7deae-104">Es True si la cuenta es una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7deae-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7deae-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7deae-105">Quick info</span></span>

<span data-ttu-id="7deae-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="7deae-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7deae-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7deae-107">Identifier:</span></span>  <br/> |<span data-ttu-id="7deae-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="7deae-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="7deae-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="7deae-109">Property type:</span></span>  <br/> |<span data-ttu-id="7deae-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7deae-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7deae-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="7deae-111">Property tag:</span></span>  <br/> |<span data-ttu-id="7deae-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="7deae-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="7deae-113">Access:</span><span class="sxs-lookup"><span data-stu-id="7deae-113">Access:</span></span>  <br/> |<span data-ttu-id="7deae-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7deae-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7deae-115">Notas</span><span class="sxs-lookup"><span data-stu-id="7deae-115">Remarks</span></span>

<span data-ttu-id="7deae-116">Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="7deae-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="7deae-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="7deae-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7deae-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="7deae-118">See also</span></span>

- [<span data-ttu-id="7deae-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="7deae-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="7deae-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="7deae-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

