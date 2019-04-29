---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True si la cuenta es una cuenta de Exchange.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418235"
---
# <a name="propacctisexch"></a><span data-ttu-id="4ec0c-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="4ec0c-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="4ec0c-104">True si la cuenta es una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4ec0c-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ec0c-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4ec0c-105">Quick info</span></span>

<span data-ttu-id="4ec0c-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4ec0c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ec0c-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4ec0c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4ec0c-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="4ec0c-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="4ec0c-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4ec0c-109">Property type:</span></span>  <br/> |<span data-ttu-id="4ec0c-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4ec0c-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4ec0c-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4ec0c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4ec0c-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="4ec0c-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="4ec0c-113">Al</span><span class="sxs-lookup"><span data-stu-id="4ec0c-113">Access:</span></span>  <br/> |<span data-ttu-id="4ec0c-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ec0c-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ec0c-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ec0c-115">Remarks</span></span>

<span data-ttu-id="4ec0c-116">Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="4ec0c-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="4ec0c-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="4ec0c-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ec0c-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="4ec0c-118">See also</span></span>

- [<span data-ttu-id="4ec0c-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="4ec0c-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="4ec0c-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="4ec0c-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

