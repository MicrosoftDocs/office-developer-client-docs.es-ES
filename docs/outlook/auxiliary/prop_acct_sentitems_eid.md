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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431844"
---
# <a name="prop_acct_sentitems_eid"></a><span data-ttu-id="4caca-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="4caca-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="4caca-104">Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="4caca-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4caca-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4caca-105">Quick info</span></span>

<span data-ttu-id="4caca-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4caca-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4caca-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4caca-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4caca-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="4caca-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="4caca-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4caca-109">Property type:</span></span>  <br/> |<span data-ttu-id="4caca-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4caca-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4caca-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4caca-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4caca-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="4caca-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="4caca-113">Access:</span><span class="sxs-lookup"><span data-stu-id="4caca-113">Access:</span></span>  <br/> |<span data-ttu-id="4caca-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4caca-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4caca-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4caca-115">Remarks</span></span>

<span data-ttu-id="4caca-116">Obtener esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="4caca-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="4caca-117">La carpeta predeterminada para los elementos enviados es **Elementos enviados**.</span><span class="sxs-lookup"><span data-stu-id="4caca-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="4caca-118">Esta propiedad es de solo lectura para cuentas POP3 e IMAP.</span><span class="sxs-lookup"><span data-stu-id="4caca-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="4caca-119">Al intentar establecer esta propiedad para estos tipos de cuentas, **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="4caca-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

