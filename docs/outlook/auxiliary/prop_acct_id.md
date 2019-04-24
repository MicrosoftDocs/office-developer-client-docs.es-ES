---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Devuelve un identificador que identifica de forma única una cuenta en el perfil en el que se crea la cuenta.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327660"
---
# <a name="propacctid"></a><span data-ttu-id="e6d6f-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="e6d6f-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="e6d6f-104">Devuelve un identificador que identifica de forma única una cuenta en el perfil en el que se crea la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e6d6f-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e6d6f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e6d6f-105">Quick info</span></span>

<span data-ttu-id="e6d6f-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="e6d6f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6d6f-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e6d6f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="e6d6f-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="e6d6f-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="e6d6f-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="e6d6f-109">Property type:</span></span>  <br/> |<span data-ttu-id="e6d6f-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e6d6f-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e6d6f-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="e6d6f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="e6d6f-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="e6d6f-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="e6d6f-113">Al</span><span class="sxs-lookup"><span data-stu-id="e6d6f-113">Access:</span></span>  <br/> |<span data-ttu-id="e6d6f-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6d6f-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6d6f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6d6f-115">Remarks</span></span>

<span data-ttu-id="e6d6f-116">Obtenga esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="e6d6f-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="e6d6f-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="e6d6f-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="e6d6f-118">Esta propiedad es diferente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en el que su valor solo es único entre todas las cuentas de ese perfil en el que se creó la cuenta, mientras que **prop\_ACCT_MINI_UID** identifica de forma única la cuenta dentro y fuera del perfil en el que se creó la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e6d6f-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="e6d6f-119">Cuando un mensaje con estas propiedades se mueve a un segundo equipo con un perfil de Outlook diferente y un conjunto diferente de cuentas, **PROP_ACCT_ID** puede entrar en conflicto con una cuenta en el perfil del segundo equipo y **PROP_ACCT_MINI_UID** puede identificar de forma única la cuenta original en el perfil original.</span><span class="sxs-lookup"><span data-stu-id="e6d6f-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6d6f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6d6f-120">See also</span></span>

- [<span data-ttu-id="e6d6f-121">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="e6d6f-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="e6d6f-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="e6d6f-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

