---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322158"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="e0f34-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="e0f34-102">IOlkAccountHelper</span></span>

<span data-ttu-id="e0f34-103">Proporciona funcionalidad auxiliar en la sesión MAPI actual para administrar cuentas.</span><span class="sxs-lookup"><span data-stu-id="e0f34-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e0f34-104">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e0f34-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0f34-105">Hereda de:</span><span class="sxs-lookup"><span data-stu-id="e0f34-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="e0f34-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0f34-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e0f34-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="e0f34-107">Provided by:</span></span>  <br/> |<span data-ttu-id="e0f34-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="e0f34-108">Client</span></span>  <br/> |
|<span data-ttu-id="e0f34-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e0f34-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e0f34-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="e0f34-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e0f34-111">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="e0f34-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e0f34-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="e0f34-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="e0f34-113">*Este miembro es un marcador de posición y no es compatible.*</span><span class="sxs-lookup"><span data-stu-id="e0f34-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="e0f34-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="e0f34-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="e0f34-115">Obtiene el nombre de perfil de una cuenta.</span><span class="sxs-lookup"><span data-stu-id="e0f34-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="e0f34-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="e0f34-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="e0f34-117">Abre una sesión MAPI y mantiene una referencia a la sesión para el administrador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e0f34-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="e0f34-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="e0f34-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="e0f34-119">Libera el objeto de sesión MAPI devuelto por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="e0f34-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0f34-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0f34-120">Remarks</span></span>

<span data-ttu-id="e0f34-121">Esta interfaz se pasa a [IOlkAccountManager::Init al](iolkaccountmanager-init.md) inicializar el administrador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e0f34-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0f34-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e0f34-122">See also</span></span>

- [<span data-ttu-id="e0f34-123">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="e0f34-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="e0f34-124">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="e0f34-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

