---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Recupera o establece el identificador de entrada de la libreta de direcciones de la cuenta.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326435"
---
# <a name="prop_mapi_identity_entryid"></a><span data-ttu-id="00f81-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="00f81-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="00f81-104">Recupera o establece el identificador de entrada de la libreta de direcciones de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="00f81-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="00f81-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="00f81-105">Quick info</span></span>

<span data-ttu-id="00f81-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="00f81-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00f81-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="00f81-107">Identifier:</span></span>  <br/> |<span data-ttu-id="00f81-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="00f81-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="00f81-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="00f81-109">Property type:</span></span>  <br/> |<span data-ttu-id="00f81-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="00f81-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="00f81-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="00f81-111">Property tag:</span></span>  <br/> |<span data-ttu-id="00f81-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="00f81-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="00f81-113">Acceso:</span><span class="sxs-lookup"><span data-stu-id="00f81-113">Access:</span></span>  <br/> |<span data-ttu-id="00f81-114">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="00f81-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00f81-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00f81-115">Remarks</span></span>

 <span data-ttu-id="00f81-116">**PROP \_ No \_ se espera que MAPI IDENTITY \_ ENTRYID** exista en todas las cuentas.</span><span class="sxs-lookup"><span data-stu-id="00f81-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="00f81-117">Por ejemplo, una cuenta de Exchange podría tener establecido **PROP \_ MAPI IDENTITY \_ \_ ENTRYID** y no [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), mientras que para una cuenta SMTP/POP3 se invierte la situación.</span><span class="sxs-lookup"><span data-stu-id="00f81-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="00f81-118">**PROP \_ MAPI_IDENTITY_ENTRYID** devuelve un identificador de entrada similar al valor devuelto por  _lppEntryID_ en [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="00f81-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00f81-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00f81-119">See also</span></span>

- [<span data-ttu-id="00f81-120">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="00f81-120">About the Account Management API</span></span>](about-the-account-management-api.md)

