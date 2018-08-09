---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Devuelve un identificador de cuenta que es exclusivo a través de los perfiles de Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816321"
---
# <a name="propacctminiuid"></a><span data-ttu-id="ed0d9-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="ed0d9-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="ed0d9-104">Devuelve un identificador de cuenta que es exclusivo a través de los perfiles de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ed0d9-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ed0d9-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ed0d9-105">Quick info</span></span>

<span data-ttu-id="ed0d9-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ed0d9-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed0d9-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ed0d9-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ed0d9-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="ed0d9-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="ed0d9-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ed0d9-109">Property type:</span></span>  <br/> |<span data-ttu-id="ed0d9-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ed0d9-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ed0d9-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="ed0d9-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ed0d9-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="ed0d9-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="ed0d9-113">Access:</span><span class="sxs-lookup"><span data-stu-id="ed0d9-113">Access:</span></span>  <br/> |<span data-ttu-id="ed0d9-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed0d9-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed0d9-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed0d9-115">Remarks</span></span>

<span data-ttu-id="ed0d9-116">Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="ed0d9-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="ed0d9-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="ed0d9-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="ed0d9-118">Esta propiedad es diferente de [PROP_ACCT_ID](prop_acct_id.md) en que su valor identifica la cuenta dentro y fuera del perfil en el que se creó la cuenta, mientras que **PROP_ACCT_ID** es único sólo entre todas las cuentas dentro de ese uno perfil en el que se creó la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ed0d9-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="ed0d9-119">Cuando un mensaje con estas propiedades se desplaza hasta un segundo equipo con un perfil de Outlook diferente y un conjunto diferente de las cuentas de, **PROP_ACCT_MINI_UID** puede identificar de forma exclusiva la cuenta original en el perfil original.</span><span class="sxs-lookup"><span data-stu-id="ed0d9-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="ed0d9-120">Sin embargo, **PROP_ACCT_ID** , posiblemente, pueden entrar en conflicto con una cuenta en el perfil del segundo equipo.</span><span class="sxs-lookup"><span data-stu-id="ed0d9-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed0d9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed0d9-121">See also</span></span>

- [<span data-ttu-id="ed0d9-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="ed0d9-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="ed0d9-123">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="ed0d9-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="ed0d9-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ed0d9-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

