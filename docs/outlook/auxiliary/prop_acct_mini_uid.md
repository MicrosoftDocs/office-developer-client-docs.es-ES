---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Devuelve un identificador de cuenta único en todos los perfiles de Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409436"
---
# <a name="prop_acct_mini_uid"></a><span data-ttu-id="fd1cc-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="fd1cc-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="fd1cc-104">Devuelve un identificador de cuenta único en todos los perfiles de Outlook.</span><span class="sxs-lookup"><span data-stu-id="fd1cc-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fd1cc-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="fd1cc-105">Quick info</span></span>

<span data-ttu-id="fd1cc-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="fd1cc-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd1cc-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fd1cc-107">Identifier:</span></span>  <br/> |<span data-ttu-id="fd1cc-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="fd1cc-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="fd1cc-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="fd1cc-109">Property type:</span></span>  <br/> |<span data-ttu-id="fd1cc-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fd1cc-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fd1cc-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="fd1cc-111">Property tag:</span></span>  <br/> |<span data-ttu-id="fd1cc-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="fd1cc-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="fd1cc-113">Acceso:</span><span class="sxs-lookup"><span data-stu-id="fd1cc-113">Access:</span></span>  <br/> |<span data-ttu-id="fd1cc-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd1cc-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd1cc-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd1cc-115">Remarks</span></span>

<span data-ttu-id="fd1cc-116">Obtenga esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="fd1cc-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="fd1cc-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="fd1cc-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="fd1cc-118">Esta propiedad es diferente de [PROP_ACCT_ID](prop_acct_id.md) en que su valor identifica de forma única la cuenta dentro y fuera del perfil en el que se creó la cuenta, mientras que **PROP_ACCT_ID** es único solo entre todas las cuentas dentro de ese perfil en el que se creó la cuenta.</span><span class="sxs-lookup"><span data-stu-id="fd1cc-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="fd1cc-119">Cuando un mensaje con estas propiedades se desvía a un segundo equipo con un perfil de Outlook diferente y un conjunto de cuentas diferente, **PROP_ACCT_MINI_UID** puede identificar de forma única la cuenta original en el perfil original.</span><span class="sxs-lookup"><span data-stu-id="fd1cc-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="fd1cc-120">Sin embargo, **PROP_ACCT_ID** posiblemente entre en conflicto con una cuenta en el perfil del segundo equipo.</span><span class="sxs-lookup"><span data-stu-id="fd1cc-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd1cc-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd1cc-121">See also</span></span>

- [<span data-ttu-id="fd1cc-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="fd1cc-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="fd1cc-123">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="fd1cc-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="fd1cc-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="fd1cc-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

