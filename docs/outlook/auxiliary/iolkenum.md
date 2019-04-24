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
# <a name="iolkenum"></a><span data-ttu-id="d1544-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="d1544-102">IOlkEnum</span></span>

<span data-ttu-id="d1544-103">Admite la enumeración de cuentas como objetos [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d1544-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d1544-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d1544-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1544-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="d1544-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="d1544-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1544-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="d1544-107">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d1544-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="d1544-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="d1544-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="d1544-109">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="d1544-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="d1544-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="d1544-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="d1544-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d1544-111">Called by:</span></span>  <br/> |<span data-ttu-id="d1544-112">Client</span><span class="sxs-lookup"><span data-stu-id="d1544-112">Client</span></span>  <br/> |
|<span data-ttu-id="d1544-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="d1544-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d1544-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="d1544-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d1544-115">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="d1544-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d1544-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="d1544-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="d1544-117">Obtiene el número de cuentas del enumerador.</span><span class="sxs-lookup"><span data-stu-id="d1544-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d1544-118">Reset</span><span class="sxs-lookup"><span data-stu-id="d1544-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="d1544-119">Restablece el enumerador al principio.</span><span class="sxs-lookup"><span data-stu-id="d1544-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="d1544-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="d1544-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="d1544-121">Obtiene la siguiente cuenta del enumerador.</span><span class="sxs-lookup"><span data-stu-id="d1544-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="d1544-122">Skip</span><span class="sxs-lookup"><span data-stu-id="d1544-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="d1544-123">Omite un número de cuentas especificado en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d1544-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1544-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1544-124">Remarks</span></span>

<span data-ttu-id="d1544-125">Esta interfaz se devuelve mediante **IOlkAccountManager:: EnumerateAccounts** al obtener un enumerador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="d1544-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1544-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1544-126">See also</span></span>

- [<span data-ttu-id="d1544-127">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="d1544-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d1544-128">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="d1544-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

