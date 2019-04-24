---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica el tipo de conexión cifrada que se va a usar para una cuenta SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328332"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="ec55e-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="ec55e-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="ec55e-104">Especifica el tipo de conexión cifrada que se va a usar para una cuenta SMTP.</span><span class="sxs-lookup"><span data-stu-id="ec55e-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ec55e-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ec55e-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec55e-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ec55e-106">Identifier:</span></span>  <br/> |<span data-ttu-id="ec55e-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="ec55e-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="ec55e-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ec55e-108">Property type:</span></span>  <br/> |<span data-ttu-id="ec55e-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="ec55e-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="ec55e-110">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ec55e-110">Property tag:</span></span>  <br/> |<span data-ttu-id="ec55e-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="ec55e-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="ec55e-112">Al</span><span class="sxs-lookup"><span data-stu-id="ec55e-112">Access:</span></span>  <br/> |<span data-ttu-id="ec55e-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec55e-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec55e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec55e-114">Remarks</span></span>

<span data-ttu-id="ec55e-115">El valor puede ser una de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="ec55e-115">The value can be one of the following constants.</span></span> <span data-ttu-id="ec55e-116">Consulte [constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener sus valores.</span><span class="sxs-lookup"><span data-stu-id="ec55e-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="ec55e-117">**Constants**</span><span class="sxs-lookup"><span data-stu-id="ec55e-117">**Constants**</span></span>|<span data-ttu-id="ec55e-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec55e-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec55e-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="ec55e-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="ec55e-120">No use ningún cifrado.</span><span class="sxs-lookup"><span data-stu-id="ec55e-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="ec55e-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="ec55e-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="ec55e-122">Usar el cifrado de capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="ec55e-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="ec55e-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="ec55e-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="ec55e-124">Usar el cifrado de seguridad de la capa de transporte (TLS) y el protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="ec55e-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="ec55e-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="ec55e-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="ec55e-126">Detectar y usar automáticamente el método de cifrado admitido por el servidor de correo.</span><span class="sxs-lookup"><span data-stu-id="ec55e-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec55e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec55e-127">See also</span></span>

- [<span data-ttu-id="ec55e-128">Administrar la descarga de mensajes de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="ec55e-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="ec55e-129">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ec55e-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

