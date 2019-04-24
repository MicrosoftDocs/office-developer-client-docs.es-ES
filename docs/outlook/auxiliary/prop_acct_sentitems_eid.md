---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327590"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="e1ac7-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="e1ac7-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="e1ac7-104">Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e1ac7-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e1ac7-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e1ac7-105">Quick info</span></span>

<span data-ttu-id="e1ac7-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="e1ac7-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1ac7-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e1ac7-107">Identifier:</span></span>  <br/> |<span data-ttu-id="e1ac7-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="e1ac7-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="e1ac7-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="e1ac7-109">Property type:</span></span>  <br/> |<span data-ttu-id="e1ac7-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e1ac7-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e1ac7-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="e1ac7-111">Property tag:</span></span>  <br/> |<span data-ttu-id="e1ac7-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="e1ac7-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="e1ac7-113">Al</span><span class="sxs-lookup"><span data-stu-id="e1ac7-113">Access:</span></span>  <br/> |<span data-ttu-id="e1ac7-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1ac7-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1ac7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1ac7-115">Remarks</span></span>

<span data-ttu-id="e1ac7-116">Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="e1ac7-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="e1ac7-117">La carpeta predeterminada para los elementos enviados es **elementos enviados**.</span><span class="sxs-lookup"><span data-stu-id="e1ac7-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="e1ac7-118">Esta propiedad es de sólo lectura para cuentas POP3 e IMAP.</span><span class="sxs-lookup"><span data-stu-id="e1ac7-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="e1ac7-119">Si se intenta establecer esta propiedad para estos tipos de cuentas, devuelve **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="e1ac7-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

