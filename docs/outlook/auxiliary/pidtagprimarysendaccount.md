---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Especifica el accountsendstamp principal para un mensaje.
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816308"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="76734-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="76734-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="76734-104">Especifica la marca de "Enviar" de la cuenta principal de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="76734-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76734-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="76734-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76734-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="76734-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76734-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="76734-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="76734-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="76734-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76734-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="76734-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="76734-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="76734-110">Data type:</span></span>  <br/> |<span data-ttu-id="76734-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="76734-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="76734-112">Área:</span><span class="sxs-lookup"><span data-stu-id="76734-112">Area:</span></span>  <br/> |<span data-ttu-id="76734-113">Cuenta</span><span class="sxs-lookup"><span data-stu-id="76734-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76734-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76734-114">Remarks</span></span>

<span data-ttu-id="76734-115">Esta propiedad se aplica a un objeto de mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="76734-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="76734-116">Para un mensaje recibido, la marca de "Enviar" de la cuenta principal indica qué cuenta se debe enviar una directa o bien una respuesta con.</span><span class="sxs-lookup"><span data-stu-id="76734-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="76734-117">Para un mensaje saliente, determina en qué cuenta para enviar el mensaje con.</span><span class="sxs-lookup"><span data-stu-id="76734-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="76734-118">Su valor es el valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) desde la interfaz de [IOlkAccount](iolkaccount.md) de la cuenta con la que se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="76734-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76734-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="76734-119">See also</span></span>

- [<span data-ttu-id="76734-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="76734-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="76734-121">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="76734-121">MAPI Properties</span></span>](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="76734-122">Propiedad canónica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="76734-122">PidTagPrimarySendAccount Canonical Property</span></span>](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

