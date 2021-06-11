---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica la dirección de correo electrónico de la cuenta.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436779"
---
# <a name="prop_acct_user_email_addr"></a><span data-ttu-id="be286-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="be286-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="be286-104">Especifica la dirección de correo electrónico de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="be286-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="be286-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="be286-105">Quick info</span></span>

<span data-ttu-id="be286-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="be286-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be286-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="be286-107">Identifier:</span></span>  <br/> |<span data-ttu-id="be286-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="be286-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="be286-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="be286-109">Property type:</span></span>  <br/> |<span data-ttu-id="be286-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be286-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="be286-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="be286-111">Property tag:</span></span>  <br/> |<span data-ttu-id="be286-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="be286-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="be286-113">Access:</span><span class="sxs-lookup"><span data-stu-id="be286-113">Access:</span></span>  <br/> |<span data-ttu-id="be286-114">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="be286-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be286-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be286-115">Remarks</span></span>

 <span data-ttu-id="be286-116">**PROP_ACCT_USER_EMAIL_ADDR** no se espera que exista en todas las cuentas.</span><span class="sxs-lookup"><span data-stu-id="be286-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="be286-117">Por ejemplo, una cuenta Exchange [](prop_mapi_identity_entryid.md) puede tener PROP_MAPI_IDENTITY_ENTRYID pero no PROP_ACCT_USER_EMAIL_ADDR **,** mientras que para una cuenta SMTP/POP3, la situación se invierte.</span><span class="sxs-lookup"><span data-stu-id="be286-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be286-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="be286-118">See also</span></span>

- [<span data-ttu-id="be286-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="be286-119">About the Account Management API</span></span>](about-the-account-management-api.md)

