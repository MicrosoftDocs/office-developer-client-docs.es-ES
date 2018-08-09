---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 3c28b1e8ab7e2d72d27cc6545b6ef57834ef5b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816211"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="102da-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="102da-102">IOlkAccountHelper</span></span>

<span data-ttu-id="102da-103">Proporciona funcionalidad auxiliar en la sesión MAPI actual para administrar las cuentas.</span><span class="sxs-lookup"><span data-stu-id="102da-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="102da-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="102da-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="102da-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="102da-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="102da-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="102da-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="102da-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="102da-107">Provided by:</span></span>  <br/> |<span data-ttu-id="102da-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="102da-108">Client</span></span>  <br/> |
|<span data-ttu-id="102da-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="102da-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="102da-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="102da-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="102da-111">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="102da-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="102da-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="102da-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="102da-113">*Este miembro es un marcador de posición y no se admite.*</span><span class="sxs-lookup"><span data-stu-id="102da-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="102da-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="102da-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="102da-115">Obtiene el nombre del perfil de una cuenta.</span><span class="sxs-lookup"><span data-stu-id="102da-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="102da-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="102da-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="102da-117">Se abre una sesión MAPI y mantiene una referencia a la sesión para el Administrador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="102da-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="102da-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="102da-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="102da-119">Libera el objeto de sesión MAPI que se ha devuelto por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="102da-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="102da-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="102da-120">Remarks</span></span>

<span data-ttu-id="102da-121">Esta interfaz se pasa al [IOlkAccountManager::Init](iolkaccountmanager-init.md) al inicializar el Administrador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="102da-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="102da-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="102da-122">See also</span></span>

- [<span data-ttu-id="102da-123">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="102da-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="102da-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="102da-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

