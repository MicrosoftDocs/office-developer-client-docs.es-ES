---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Especifica el método de autenticación que se va a usar para la cuenta SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434644"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="7d0de-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="7d0de-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="7d0de-104">Especifica el método de autenticación que se va a usar para la cuenta SMTP.</span><span class="sxs-lookup"><span data-stu-id="7d0de-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7d0de-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7d0de-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d0de-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d0de-106">Identifier:</span></span>  <br/> |<span data-ttu-id="7d0de-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="7d0de-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="7d0de-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="7d0de-108">Property type:</span></span>  <br/> |<span data-ttu-id="7d0de-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="7d0de-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="7d0de-110">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="7d0de-110">Property tag:</span></span>  <br/> |<span data-ttu-id="7d0de-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="7d0de-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="7d0de-112">Al</span><span class="sxs-lookup"><span data-stu-id="7d0de-112">Access:</span></span>  <br/> |<span data-ttu-id="7d0de-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d0de-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d0de-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d0de-114">Remarks</span></span>

<span data-ttu-id="7d0de-115">El valor es una máscara de máscara de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="7d0de-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="7d0de-116">Consulte [constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener sus valores.</span><span class="sxs-lookup"><span data-stu-id="7d0de-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="7d0de-117">**SMTP_AUTH_SAME_AS_POP** significa usar las mismas credenciales que mi servidor de correo entrante, tal y como lo proporciona [PROP_INET_USER](prop_inet_user.md) y [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="7d0de-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="7d0de-118">**SMTP_AUTH_USER_PASS** significa usar las credenciales proporcionadas por [PROP_SMTP_USER](prop_smtp_user.md) y [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="7d0de-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="7d0de-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** significa solicitar al usuario que inicie sesión en el servidor de correo entrante antes de enviar correo.</span><span class="sxs-lookup"><span data-stu-id="7d0de-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7d0de-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="7d0de-120">See also</span></span>

- [<span data-ttu-id="7d0de-121">Administrar la descarga de mensajes de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="7d0de-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="7d0de-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="7d0de-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

