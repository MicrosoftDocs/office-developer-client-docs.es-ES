---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Especifica la accountsendstamp secundaria para el mensaje.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396480"
---
# <a name="pidtagnextsendacct"></a><span data-ttu-id="419fe-103">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="419fe-103">PidTagNextSendAcct</span></span>

<span data-ttu-id="419fe-104">Especifica la marca "Enviar" de cuenta secundaria para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="419fe-104">Specifies the secondary account "send" stamp for the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="419fe-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="419fe-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="419fe-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="419fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="419fe-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="419fe-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="419fe-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="419fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="419fe-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="419fe-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="419fe-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="419fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="419fe-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="419fe-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="419fe-112">Área:</span><span class="sxs-lookup"><span data-stu-id="419fe-112">Area:</span></span>  <br/> |<span data-ttu-id="419fe-113">Aplicación de Outlook</span><span class="sxs-lookup"><span data-stu-id="419fe-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="419fe-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="419fe-114">Remarks</span></span>

<span data-ttu-id="419fe-115">Esta propiedad se aplica a un objeto de mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="419fe-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="419fe-116">Para un mensaje recibido, la marca "Enviar" de cuenta secundaria indica qué cuenta se debe enviar un directa o una respuesta con, si no se puede enviar la reenviar o responder con la cuenta principal.</span><span class="sxs-lookup"><span data-stu-id="419fe-116">For a received message, the secondary account "send" stamp indicates which account a forward or a reply should be sent with, if the forward or reply cannot be sent with the primary account.</span></span> <span data-ttu-id="419fe-117">Para un mensaje saliente, la cuenta secundaria "Enviar" marca determina con qué cuenta para enviar el mensaje, si no se puede enviar el mensaje con la cuenta principal.</span><span class="sxs-lookup"><span data-stu-id="419fe-117">For an outgoing message, the secondary account "send" stamp determines with which account to send the message, if the message cannot be sent with the primary account.</span></span> <span data-ttu-id="419fe-118">Su valor es el valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) desde la interfaz de [IOlkAccount](iolkaccount.md) de la cuenta con la que se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="419fe-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="419fe-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="419fe-119">See also</span></span>

- [<span data-ttu-id="419fe-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="419fe-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="419fe-121">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="419fe-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [<span data-ttu-id="419fe-122">Propiedad canónica PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="419fe-122">PidTagNextSendAcct Canonical Property</span></span>](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

