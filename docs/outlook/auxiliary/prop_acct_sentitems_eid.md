---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816313"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="12905-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="12905-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="12905-104">Representa el identificador de entrada de la carpeta predeterminada para los elementos enviados para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="12905-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="12905-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="12905-105">Quick info</span></span>

<span data-ttu-id="12905-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="12905-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12905-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="12905-107">Identifier:</span></span>  <br/> |<span data-ttu-id="12905-108">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="12905-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="12905-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="12905-109">Property type:</span></span>  <br/> |<span data-ttu-id="12905-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="12905-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="12905-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="12905-111">Property tag:</span></span>  <br/> |<span data-ttu-id="12905-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="12905-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="12905-113">Access:</span><span class="sxs-lookup"><span data-stu-id="12905-113">Access:</span></span>  <br/> |<span data-ttu-id="12905-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="12905-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12905-115">Notas</span><span class="sxs-lookup"><span data-stu-id="12905-115">Remarks</span></span>

<span data-ttu-id="12905-116">Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="12905-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="12905-117">La carpeta predeterminada para los elementos enviados es **Elementos enviados**.</span><span class="sxs-lookup"><span data-stu-id="12905-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="12905-118">Esta propiedad es de sólo lectura para las cuentas POP3 e IMAP.</span><span class="sxs-lookup"><span data-stu-id="12905-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="12905-119">Si se intenta establecer esta propiedad para estos tipos de cuentas, devuelve **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="12905-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

