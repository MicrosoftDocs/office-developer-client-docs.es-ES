---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421287"
---
# <a name="prop_smtp_secure_connection"></a><span data-ttu-id="c850f-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="c850f-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="c850f-104">Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.</span><span class="sxs-lookup"><span data-stu-id="c850f-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c850f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c850f-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c850f-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c850f-106">Identifier:</span></span>  <br/> |<span data-ttu-id="c850f-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="c850f-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="c850f-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="c850f-108">Property type:</span></span>  <br/> |<span data-ttu-id="c850f-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="c850f-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="c850f-110">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="c850f-110">Property tag:</span></span>  <br/> |<span data-ttu-id="c850f-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="c850f-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="c850f-112">Access:</span><span class="sxs-lookup"><span data-stu-id="c850f-112">Access:</span></span>  <br/> |<span data-ttu-id="c850f-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c850f-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c850f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c850f-114">Remarks</span></span>

<span data-ttu-id="c850f-115">El valor puede ser una de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="c850f-115">The value can be one of the following constants.</span></span> <span data-ttu-id="c850f-116">Consulta [Constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener sus valores.</span><span class="sxs-lookup"><span data-stu-id="c850f-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="c850f-117">**Constants**</span><span class="sxs-lookup"><span data-stu-id="c850f-117">**Constants**</span></span>|<span data-ttu-id="c850f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c850f-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c850f-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="c850f-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="c850f-120">No use ningún cifrado.</span><span class="sxs-lookup"><span data-stu-id="c850f-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="c850f-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="c850f-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="c850f-122">Use el cifrado de capa de socket seguro (SSL).</span><span class="sxs-lookup"><span data-stu-id="c850f-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="c850f-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="c850f-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="c850f-124">Use el protocolo de autenticación y cifrado de seguridad de la capa de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="c850f-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="c850f-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="c850f-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="c850f-126">Detecte y use automáticamente el método de cifrado admitido por el servidor de correo.</span><span class="sxs-lookup"><span data-stu-id="c850f-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c850f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c850f-127">See also</span></span>

- [<span data-ttu-id="c850f-128">Administrar la descarga de mensajes de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="c850f-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="c850f-129">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="c850f-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

