---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica la dirección de correo electrónico para la cuenta.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816325"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="c731b-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="c731b-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="c731b-104">Especifica la dirección de correo electrónico para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c731b-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c731b-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c731b-105">Quick info</span></span>

<span data-ttu-id="c731b-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="c731b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c731b-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c731b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c731b-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="c731b-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="c731b-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="c731b-109">Property type:</span></span>  <br/> |<span data-ttu-id="c731b-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c731b-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c731b-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="c731b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c731b-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="c731b-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="c731b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="c731b-113">Access:</span></span>  <br/> |<span data-ttu-id="c731b-114">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c731b-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c731b-115">Notas</span><span class="sxs-lookup"><span data-stu-id="c731b-115">Remarks</span></span>

 <span data-ttu-id="c731b-116">**PROP_ACCT_USER_EMAIL_ADDR** no se espera que existen en cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="c731b-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="c731b-117">Por ejemplo, podría tener una cuenta de Exchange [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) pero no **PROP_ACCT_USER_EMAIL_ADDR**, mientras que para una cuenta POP3/SMTP, la situación se invierte.</span><span class="sxs-lookup"><span data-stu-id="c731b-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c731b-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="c731b-118">See also</span></span>

- [<span data-ttu-id="c731b-119">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="c731b-119">About the Account Management API</span></span>](about-the-account-management-api.md)

