---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592692"
---
# <a name="iolkenum"></a><span data-ttu-id="c722f-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="c722f-102">IOlkEnum</span></span>

<span data-ttu-id="c722f-103">Admite enumerar cuentas como objetos de [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c722f-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c722f-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c722f-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c722f-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="c722f-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="c722f-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c722f-106">IUnknown</span></span>](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="c722f-107">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c722f-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="c722f-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="c722f-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="c722f-109">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="c722f-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="c722f-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="c722f-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="c722f-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c722f-111">Called by:</span></span>  <br/> |<span data-ttu-id="c722f-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="c722f-112">Client</span></span>  <br/> |
|<span data-ttu-id="c722f-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="c722f-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c722f-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="c722f-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c722f-115">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="c722f-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c722f-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="c722f-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="c722f-117">Obtiene el número de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="c722f-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="c722f-118">Reset</span><span class="sxs-lookup"><span data-stu-id="c722f-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="c722f-119">Restablece el enumerador al principio.</span><span class="sxs-lookup"><span data-stu-id="c722f-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="c722f-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="c722f-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="c722f-121">Obtiene la cuenta siguiente en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="c722f-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="c722f-122">Omitir</span><span class="sxs-lookup"><span data-stu-id="c722f-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="c722f-123">Omite un número especificado de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="c722f-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c722f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c722f-124">Remarks</span></span>

<span data-ttu-id="c722f-125">Esta interfaz es devuelto por **IOlkAccountManager::EnumerateAccounts** cuando se obtiene un enumerador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="c722f-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c722f-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c722f-126">See also</span></span>

- [<span data-ttu-id="c722f-127">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="c722f-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="c722f-128">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="c722f-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

