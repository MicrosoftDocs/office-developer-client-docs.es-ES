---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389739"
---
# <a name="iolkenum"></a><span data-ttu-id="d6505-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="d6505-102">IOlkEnum</span></span>

<span data-ttu-id="d6505-103">Admite enumerar cuentas como objetos de [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d6505-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d6505-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d6505-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6505-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="d6505-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="d6505-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6505-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="d6505-107">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d6505-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6505-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="d6505-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="d6505-109">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="d6505-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="d6505-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="d6505-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="d6505-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d6505-111">Called by:</span></span>  <br/> |<span data-ttu-id="d6505-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="d6505-112">Client</span></span>  <br/> |
|<span data-ttu-id="d6505-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="d6505-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d6505-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="d6505-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d6505-115">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="d6505-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d6505-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="d6505-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="d6505-117">Obtiene el número de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d6505-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d6505-118">Reset</span><span class="sxs-lookup"><span data-stu-id="d6505-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="d6505-119">Restablece el enumerador al principio.</span><span class="sxs-lookup"><span data-stu-id="d6505-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="d6505-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="d6505-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="d6505-121">Obtiene la cuenta siguiente en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d6505-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d6505-122">Omitir</span><span class="sxs-lookup"><span data-stu-id="d6505-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="d6505-123">Omite un número especificado de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d6505-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6505-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6505-124">Remarks</span></span>

<span data-ttu-id="d6505-125">Esta interfaz es devuelto por **IOlkAccountManager::EnumerateAccounts** cuando se obtiene un enumerador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="d6505-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6505-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6505-126">See also</span></span>

- [<span data-ttu-id="d6505-127">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="d6505-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d6505-128">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="d6505-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

