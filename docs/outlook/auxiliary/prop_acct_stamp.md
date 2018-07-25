---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Devuelve la marca de cuenta.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: c55eec212ae794592c83bbf06b01eab5ca6bff6d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/25/2018
ms.locfileid: "19816330"
---
# <a name="propacctstamp"></a><span data-ttu-id="ed3ae-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="ed3ae-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="ed3ae-104">Devuelve la marca de cuenta.</span><span class="sxs-lookup"><span data-stu-id="ed3ae-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ed3ae-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ed3ae-105">Quick info</span></span>

<span data-ttu-id="ed3ae-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ed3ae-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed3ae-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ed3ae-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ed3ae-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="ed3ae-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="ed3ae-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ed3ae-109">Property type:</span></span>  <br/> |<span data-ttu-id="ed3ae-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ed3ae-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ed3ae-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="ed3ae-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ed3ae-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="ed3ae-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="ed3ae-113">Access:</span><span class="sxs-lookup"><span data-stu-id="ed3ae-113">Access:</span></span>  <br/> |<span data-ttu-id="ed3ae-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed3ae-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed3ae-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed3ae-115">Remarks</span></span>

<span data-ttu-id="ed3ae-116">Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="ed3ae-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="ed3ae-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="ed3ae-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed3ae-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed3ae-118">See also</span></span>

- [<span data-ttu-id="ed3ae-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="ed3ae-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="ed3ae-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ed3ae-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

