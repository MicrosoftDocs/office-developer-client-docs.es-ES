---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816257"
---
# <a name="iolkenum"></a><span data-ttu-id="1aacd-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="1aacd-102">IOlkEnum</span></span>

<span data-ttu-id="1aacd-103">Admite enumerar cuentas como objetos de [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1aacd-103">Supports enumerating accounts as [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1aacd-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1aacd-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aacd-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="1aacd-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="1aacd-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="1aacd-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="1aacd-107">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1aacd-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="1aacd-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="1aacd-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="1aacd-109">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="1aacd-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="1aacd-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="1aacd-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="1aacd-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1aacd-111">Called by:</span></span>  <br/> |<span data-ttu-id="1aacd-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="1aacd-112">Client</span></span>  <br/> |
|<span data-ttu-id="1aacd-113">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="1aacd-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1aacd-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="1aacd-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1aacd-115">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="1aacd-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1aacd-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="1aacd-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="1aacd-117">Obtiene el número de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="1aacd-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="1aacd-118">Reset</span><span class="sxs-lookup"><span data-stu-id="1aacd-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="1aacd-119">Restablece el enumerador al principio.</span><span class="sxs-lookup"><span data-stu-id="1aacd-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="1aacd-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="1aacd-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="1aacd-121">Obtiene la cuenta siguiente en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="1aacd-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="1aacd-122">Omitir</span><span class="sxs-lookup"><span data-stu-id="1aacd-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="1aacd-123">Omite un número especificado de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="1aacd-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1aacd-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1aacd-124">Remarks</span></span>

<span data-ttu-id="1aacd-125">Esta interfaz es devuelto por **IOlkAccountManager::EnumerateAccounts** cuando se obtiene un enumerador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="1aacd-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1aacd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aacd-126">See also</span></span>

- [<span data-ttu-id="1aacd-127">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="1aacd-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="1aacd-128">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="1aacd-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

