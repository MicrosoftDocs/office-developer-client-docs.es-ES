---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Representa una estructura ACCT_BIN que contiene el identificador exclusivo de una cuenta de Exchange.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816342"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="9b18a-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="9b18a-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="9b18a-104">Representa una estructura [ACCT_BIN](acct_bin.md) que contiene el identificador exclusivo de una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9b18a-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9b18a-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9b18a-105">Quick info</span></span>

<span data-ttu-id="9b18a-106">Vea [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="9b18a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b18a-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9b18a-107">Identifier:</span></span>  <br/> |<span data-ttu-id="9b18a-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="9b18a-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="9b18a-109">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="9b18a-109">Property type:</span></span>  <br/> |<span data-ttu-id="9b18a-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9b18a-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9b18a-111">Etiqueta de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="9b18a-111">Property tag:</span></span>  <br/> |<span data-ttu-id="9b18a-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="9b18a-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="9b18a-113">Access:</span><span class="sxs-lookup"><span data-stu-id="9b18a-113">Access:</span></span>  <br/> |<span data-ttu-id="9b18a-114">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b18a-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b18a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b18a-115">Remarks</span></span>

<span data-ttu-id="9b18a-116">Obtener esta propiedad mediante el uso de [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="9b18a-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="9b18a-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) para comprobar si la cuenta es una cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9b18a-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="9b18a-118">Si es así, **propiedades\_MAPI_EMSMDB_UID** es un **ACCT_BIN** que contiene **emsmdbUID**, que es el identificador único para la cuenta de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9b18a-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="9b18a-119">Si la cuenta no es una cuenta de Exchange, esta propiedad no está definida.</span><span class="sxs-lookup"><span data-stu-id="9b18a-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b18a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b18a-120">See also</span></span>

- [<span data-ttu-id="9b18a-121">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="9b18a-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="9b18a-122">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="9b18a-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="9b18a-123">Usar varias cuentas de Exchange</span><span class="sxs-lookup"><span data-stu-id="9b18a-123">Using Multiple Exchange Accounts</span></span>](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="9b18a-124">Propiedad can�nico de PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="9b18a-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

