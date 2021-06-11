---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Devuelve un identificador que identifica de forma única una cuenta dentro del perfil en el que se crea la cuenta.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407168"
---
# <a name="prop_acct_id"></a><span data-ttu-id="ec25b-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="ec25b-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="ec25b-104">Devuelve un identificador que identifica de forma única una cuenta dentro del perfil en el que se crea la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ec25b-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ec25b-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ec25b-105">Quick info</span></span>

<span data-ttu-id="ec25b-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ec25b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec25b-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ec25b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ec25b-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="ec25b-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="ec25b-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ec25b-109">Property type:</span></span>  <br/> |<span data-ttu-id="ec25b-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ec25b-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ec25b-111">Etiqueta de propiedad:</span><span class="sxs-lookup"><span data-stu-id="ec25b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ec25b-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="ec25b-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="ec25b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="ec25b-113">Access:</span></span>  <br/> |<span data-ttu-id="ec25b-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec25b-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec25b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec25b-115">Remarks</span></span>

<span data-ttu-id="ec25b-116">Obtener esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="ec25b-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="ec25b-117">Si el cliente intenta establecer esta propiedad, esta propiedad devuelve **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="ec25b-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="ec25b-118">Esta propiedad es diferente [de PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) ya que su valor es único solo entre todas las cuentas dentro del perfil en el que se creó la cuenta, mientras que **PROP \_ ACCT_MINI_UID** identifica de forma única la cuenta dentro y fuera del perfil en el que se creó la cuenta.</span><span class="sxs-lookup"><span data-stu-id="ec25b-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="ec25b-119">Cuando un mensaje con estas propiedades se desvía a un segundo equipo con un perfil de Outlook diferente y un conjunto de cuentas diferente, **PROP_ACCT_ID** puede entrar en conflicto con una cuenta en el perfil del segundo equipo y **PROP_ACCT_MINI_UID** puede identificar de forma única la cuenta original en el perfil original.</span><span class="sxs-lookup"><span data-stu-id="ec25b-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec25b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec25b-120">See also</span></span>

- [<span data-ttu-id="ec25b-121">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="ec25b-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="ec25b-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="ec25b-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

