---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtiene el nombre de Perfil de una cuenta.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322109"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="85764-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="85764-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="85764-104">Obtiene el nombre de Perfil de una cuenta.</span><span class="sxs-lookup"><span data-stu-id="85764-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="85764-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="85764-105">Quick info</span></span>

<span data-ttu-id="85764-106">Consulte [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="85764-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="85764-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="85764-107">Parameters</span></span>

<span data-ttu-id="85764-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="85764-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="85764-109">a contempla El nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="85764-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="85764-110">_PCCh_</span><span class="sxs-lookup"><span data-stu-id="85764-110">_pcch_</span></span>
  
> <span data-ttu-id="85764-111">a contempla Después de llamar a este método, contiene el tamaño (en número de caracteres) de _pwszIdentity_ que se ha asignado.</span><span class="sxs-lookup"><span data-stu-id="85764-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="85764-112">Cuando se devuelve, contiene la longitud real, incluido el carácter de terminación 0, del nombre del perfil devuelto.</span><span class="sxs-lookup"><span data-stu-id="85764-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="85764-113">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="85764-113">Return values</span></span>

|<span data-ttu-id="85764-114">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="85764-114">**HRESULT**</span></span>|<span data-ttu-id="85764-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="85764-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85764-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="85764-116">S_OK</span></span>  <br/> |<span data-ttu-id="85764-117">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="85764-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="85764-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="85764-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="85764-119">El nombre del perfil devuelto es más largo que el tamaño de _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="85764-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="85764-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="85764-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="85764-121">_PCCh_ es NULL.</span><span class="sxs-lookup"><span data-stu-id="85764-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85764-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85764-122">Remarks</span></span>

<span data-ttu-id="85764-123">Si _pwszIdentity_ es demasiado pequeño para contener el nombre del perfil, no se establecerá en la devolución y _PCCh_ apuntará al tamaño necesario para _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="85764-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85764-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="85764-124">See also</span></span>

- [<span data-ttu-id="85764-125">Acerca de la API de administración de cuenta</span><span class="sxs-lookup"><span data-stu-id="85764-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="85764-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="85764-126">PidTagProfileName</span></span>](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

