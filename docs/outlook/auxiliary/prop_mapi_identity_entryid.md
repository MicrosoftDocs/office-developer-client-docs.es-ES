---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Recupera o establece el identificador de entrada de la libreta de direcciones para la cuenta.
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816322"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="b7f05-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b7f05-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="b7f05-104">Recupera o establece el identificador de entrada de la libreta de direcciones para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="b7f05-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b7f05-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b7f05-105">Quick info</span></span>

<span data-ttu-id="b7f05-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="b7f05-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7f05-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b7f05-107">Identifier:</span></span>  <br/> |<span data-ttu-id="b7f05-108">0 x 2002</span><span class="sxs-lookup"><span data-stu-id="b7f05-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="b7f05-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="b7f05-109">Property type:</span></span>  <br/> |<span data-ttu-id="b7f05-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b7f05-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b7f05-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="b7f05-111">Property tag:</span></span>  <br/> |<span data-ttu-id="b7f05-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="b7f05-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="b7f05-113">Access:</span><span class="sxs-lookup"><span data-stu-id="b7f05-113">Access:</span></span>  <br/> |<span data-ttu-id="b7f05-114">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b7f05-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7f05-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7f05-115">Remarks</span></span>

 <span data-ttu-id="b7f05-116">**Propiedades\_MAPI\_identidad\_ENTRYID** no se espera que existen en cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="b7f05-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="b7f05-117">Por ejemplo, podría tener una cuenta de Exchange **propiedades\_MAPI\_identidad\_ENTRYID** establecer y no [propiedades\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), mientras que para una cuenta POP3/SMTP se invierte la situación.</span><span class="sxs-lookup"><span data-stu-id="b7f05-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="b7f05-118">**PROPIEDADES\_MAPI_IDENTITY_ENTRYID** devuelve un identificador de entrada que es similar al valor devuelto por _lppEntryID_ en [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7f05-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7f05-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f05-119">See also</span></span>

- [<span data-ttu-id="b7f05-120">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="b7f05-120">About the Account Management API</span></span>](about-the-account-management-api.md)

