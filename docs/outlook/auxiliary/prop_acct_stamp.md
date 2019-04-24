---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Devuelve el sello de cuenta.
ms.openlocfilehash: fe3c6e65e12ab62bd1c2ec0245e4a22502f610eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327597"
---
# <a name="propacctstamp"></a><span data-ttu-id="d0756-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="d0756-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="d0756-104">Devuelve el sello de cuenta.</span><span class="sxs-lookup"><span data-stu-id="d0756-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d0756-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d0756-105">Quick info</span></span>

<span data-ttu-id="d0756-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d0756-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0756-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0756-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d0756-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="d0756-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="d0756-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="d0756-109">Property type:</span></span>  <br/> |<span data-ttu-id="d0756-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0756-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d0756-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="d0756-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d0756-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="d0756-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="d0756-113">Al</span><span class="sxs-lookup"><span data-stu-id="d0756-113">Access:</span></span>  <br/> |<span data-ttu-id="d0756-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0756-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0756-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0756-115">Remarks</span></span>

<span data-ttu-id="d0756-116">Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="d0756-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d0756-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="d0756-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0756-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0756-118">See also</span></span>

- [<span data-ttu-id="d0756-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="d0756-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="d0756-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="d0756-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

