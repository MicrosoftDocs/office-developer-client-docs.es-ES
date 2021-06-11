---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322102"
---
# <a name="iolkenum"></a><span data-ttu-id="e457e-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="e457e-102">IOlkEnum</span></span>

<span data-ttu-id="e457e-103">Admite enumerar cuentas como [objetos IUnknown.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="e457e-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e457e-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e457e-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e457e-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="e457e-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="e457e-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e457e-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="e457e-107">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e457e-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="e457e-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="e457e-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="e457e-109">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="e457e-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="e457e-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="e457e-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="e457e-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e457e-111">Called by:</span></span>  <br/> |<span data-ttu-id="e457e-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="e457e-112">Client</span></span>  <br/> |
|<span data-ttu-id="e457e-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e457e-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e457e-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="e457e-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e457e-115">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="e457e-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e457e-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="e457e-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="e457e-117">Obtiene el número de cuentas del enumerador.</span><span class="sxs-lookup"><span data-stu-id="e457e-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="e457e-118">Reset</span><span class="sxs-lookup"><span data-stu-id="e457e-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="e457e-119">Restablece el enumerador al principio.</span><span class="sxs-lookup"><span data-stu-id="e457e-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="e457e-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="e457e-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="e457e-121">Obtiene la siguiente cuenta en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="e457e-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="e457e-122">Skip</span><span class="sxs-lookup"><span data-stu-id="e457e-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="e457e-123">Omite un número especificado de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="e457e-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e457e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e457e-124">Remarks</span></span>

<span data-ttu-id="e457e-125">**IOlkAccountManager::EnumerateAccounts** devuelve esta interfaz al obtener un enumerador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e457e-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e457e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e457e-126">See also</span></span>

- [<span data-ttu-id="e457e-127">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="e457e-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="e457e-128">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="e457e-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

