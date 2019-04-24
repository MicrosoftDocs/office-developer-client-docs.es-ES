---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Devuelve el accountsendstamp.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327611"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="2fdc0-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="2fdc0-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="2fdc0-104">Devuelve la marca de "enviar" de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="2fdc0-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2fdc0-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2fdc0-105">Quick info</span></span>

<span data-ttu-id="2fdc0-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="2fdc0-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2fdc0-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2fdc0-107">Identifier:</span></span>  <br/> |<span data-ttu-id="2fdc0-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="2fdc0-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="2fdc0-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="2fdc0-109">Property type:</span></span>  <br/> |<span data-ttu-id="2fdc0-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2fdc0-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2fdc0-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="2fdc0-111">Property tag:</span></span>  <br/> |<span data-ttu-id="2fdc0-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="2fdc0-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="2fdc0-113">Al</span><span class="sxs-lookup"><span data-stu-id="2fdc0-113">Access:</span></span>  <br/> |<span data-ttu-id="2fdc0-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fdc0-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fdc0-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fdc0-115">Remarks</span></span>

<span data-ttu-id="2fdc0-116">Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="2fdc0-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="2fdc0-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="2fdc0-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2fdc0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fdc0-118">See also</span></span>

- [<span data-ttu-id="2fdc0-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="2fdc0-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="2fdc0-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="2fdc0-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

