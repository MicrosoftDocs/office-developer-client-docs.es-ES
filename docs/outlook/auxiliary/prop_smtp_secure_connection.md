---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816333"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="2b102-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="2b102-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="2b102-104">Especifica el tipo de conexión cifrada que se usará para una cuenta SMTP.</span><span class="sxs-lookup"><span data-stu-id="2b102-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2b102-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2b102-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b102-106">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2b102-106">Identifier:</span></span>  <br/> |<span data-ttu-id="2b102-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="2b102-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="2b102-108">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="2b102-108">Property type:</span></span>  <br/> |<span data-ttu-id="2b102-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="2b102-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="2b102-110">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="2b102-110">Property tag:</span></span>  <br/> |<span data-ttu-id="2b102-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="2b102-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="2b102-112">Access:</span><span class="sxs-lookup"><span data-stu-id="2b102-112">Access:</span></span>  <br/> |<span data-ttu-id="2b102-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b102-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b102-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b102-114">Remarks</span></span>

<span data-ttu-id="2b102-115">El valor puede ser una de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="2b102-115">The value can be one of the following constants.</span></span> <span data-ttu-id="2b102-116">Vea [constantes (API de administración de cuenta)](constants-account-management-api.md) para sus valores.</span><span class="sxs-lookup"><span data-stu-id="2b102-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="2b102-117">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="2b102-117">**Constants**</span></span>|<span data-ttu-id="2b102-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b102-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b102-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="2b102-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="2b102-120">No use cualquier cifrado.</span><span class="sxs-lookup"><span data-stu-id="2b102-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="2b102-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="2b102-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="2b102-122">Usar el cifrado de capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="2b102-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="2b102-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="2b102-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="2b102-124">Usar el protocolo de autenticación y el cifrado de seguridad de capa de transporte (TLS).</span><span class="sxs-lookup"><span data-stu-id="2b102-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="2b102-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="2b102-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="2b102-126">Automáticamente detectar y usar el método de cifrado compatible con el servidor de correo.</span><span class="sxs-lookup"><span data-stu-id="2b102-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b102-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b102-127">See also</span></span>

- [<span data-ttu-id="2b102-128">Administrar la descarga de mensajes de las cuentas POP3</span><span class="sxs-lookup"><span data-stu-id="2b102-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="2b102-129">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="2b102-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

