---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica el método de autenticación que se usará para la cuenta de SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816337"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="4ffba-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="4ffba-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="4ffba-104">Especifica el método de autenticación que se usará para la cuenta de SMTP.</span><span class="sxs-lookup"><span data-stu-id="4ffba-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ffba-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4ffba-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ffba-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4ffba-106">Identifier:</span></span>  <br/> |<span data-ttu-id="4ffba-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="4ffba-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="4ffba-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="4ffba-108">Property type:</span></span>  <br/> |<span data-ttu-id="4ffba-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="4ffba-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="4ffba-110">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="4ffba-110">Property tag:</span></span>  <br/> |<span data-ttu-id="4ffba-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="4ffba-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="4ffba-112">Access:</span><span class="sxs-lookup"><span data-stu-id="4ffba-112">Access:</span></span>  <br/> |<span data-ttu-id="4ffba-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ffba-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ffba-114">Notas</span><span class="sxs-lookup"><span data-stu-id="4ffba-114">Remarks</span></span>

<span data-ttu-id="4ffba-115">El valor es una máscara de bits de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="4ffba-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="4ffba-116">Vea [constantes (API de administración de cuenta)](constants-account-management-api.md) para sus valores.</span><span class="sxs-lookup"><span data-stu-id="4ffba-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="4ffba-117">**SMTP_AUTH_SAME_AS_POP** significa que con las mismas credenciales que el servidor de correo entrante, tal y como proporcionado por [PROP_INET_USER](prop_inet_user.md) y [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="4ffba-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="4ffba-118">**SMTP_AUTH_USER_PASS** significa que con las credenciales como proporcionado por [PROP_SMTP_USER](prop_smtp_user.md) y [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="4ffba-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="4ffba-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** significa que solicita al usuario que inicie sesión en el servidor de correo entrante antes de enviar correo.</span><span class="sxs-lookup"><span data-stu-id="4ffba-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4ffba-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="4ffba-120">See also</span></span>

- [<span data-ttu-id="4ffba-121">Descargas de mensaje administración de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="4ffba-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="4ffba-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="4ffba-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

