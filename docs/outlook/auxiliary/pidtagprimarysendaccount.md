---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Especifica el accountsendstamp principal de un mensaje.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327709"
---
# <a name="pidtagprimarysendaccount"></a><span data-ttu-id="126f6-103">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="126f6-103">PidTagPrimarySendAccount</span></span>

<span data-ttu-id="126f6-104">Especifica la marca de la cuenta principal "enviar" para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="126f6-104">Specifies the primary account "send" stamp for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="126f6-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="126f6-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="126f6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="126f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="126f6-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="126f6-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="126f6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="126f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="126f6-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="126f6-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="126f6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="126f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="126f6-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="126f6-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="126f6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="126f6-112">Area:</span></span>  <br/> |<span data-ttu-id="126f6-113">Cuenta</span><span class="sxs-lookup"><span data-stu-id="126f6-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="126f6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="126f6-114">Remarks</span></span>

<span data-ttu-id="126f6-115">Esta propiedad se aplica a un objeto de mensaje MAPI.</span><span class="sxs-lookup"><span data-stu-id="126f6-115">This property applies to a MAPI message object.</span></span> <span data-ttu-id="126f6-116">Para un mensaje recibido, la marca de la cuenta principal "enviar" indica a qué cuenta se debe enviar un reenvío o una respuesta.</span><span class="sxs-lookup"><span data-stu-id="126f6-116">For a received message, the primary account "send" stamp indicates which account a forward or a reply should be sent with.</span></span> <span data-ttu-id="126f6-117">Para un mensaje saliente, determina con qué cuenta debe enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="126f6-117">For an outgoing message, it determines which account to send the message with.</span></span> <span data-ttu-id="126f6-118">Su valor es el valor [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) de la interfaz [IOlkAccount](iolkaccount.md) de la cuenta con la que se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="126f6-118">Its value is the [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) value from the [IOlkAccount](iolkaccount.md) interface of the account with which the message is being sent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="126f6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="126f6-119">See also</span></span>

- [<span data-ttu-id="126f6-120">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="126f6-120">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="126f6-121">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="126f6-121">MAPI Properties</span></span>](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [<span data-ttu-id="126f6-122">Propiedad canónica PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="126f6-122">PidTagPrimarySendAccount Canonical Property</span></span>](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

