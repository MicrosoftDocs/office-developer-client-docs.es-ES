---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817470"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="bbd77-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="bbd77-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="bbd77-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbd77-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbd77-105">Modifica la contraseña de un proveedor de servicios sin mostrar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bbd77-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="bbd77-106">Opcionalmente, este método se admite en los objetos de estado que implementan los proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="bbd77-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bbd77-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbd77-107">Parameters</span></span>

 <span data-ttu-id="bbd77-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="bbd77-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="bbd77-109">[entrada] Un puntero a la contraseña antigua.</span><span class="sxs-lookup"><span data-stu-id="bbd77-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="bbd77-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="bbd77-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="bbd77-111">[entrada] Un puntero a la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="bbd77-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="bbd77-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbd77-112">_ulFlags_</span></span>
  
> <span data-ttu-id="bbd77-113">[entrada] Una máscara de bits de indicadores que controla el formato de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="bbd77-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="bbd77-114">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="bbd77-114">The following flag can be set:</span></span>
    
<span data-ttu-id="bbd77-115">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bbd77-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bbd77-116">Las contraseñas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bbd77-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="bbd77-117">Si no está establecido el indicador MAPI_UNICODE., las contraseñas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bbd77-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbd77-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbd77-118">Return value</span></span>

<span data-ttu-id="bbd77-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbd77-119">S_OK</span></span> 
  
> <span data-ttu-id="bbd77-120">La modificación de la contraseña era correcta.</span><span class="sxs-lookup"><span data-stu-id="bbd77-120">The password modification was successful.</span></span>
    
<span data-ttu-id="bbd77-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bbd77-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="bbd77-122">La contraseña antigua que señala _lpOldPass_ no es válida.</span><span class="sxs-lookup"><span data-stu-id="bbd77-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="bbd77-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bbd77-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bbd77-124">El objeto de estado no es compatible con esta operación, tal como se indica por la ausencia de la marca STATUS_CHANGE_PASSWORD en propiedad de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="bbd77-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbd77-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbd77-125">Remarks</span></span>

<span data-ttu-id="bbd77-126">No todos los objetos de estado admiten el método **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="bbd77-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="bbd77-127">Se admite sólo por los proveedores de servicio que requieren los clientes que escribir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="bbd77-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="bbd77-128">Ninguno de los objetos de estado que implementa MAPI admite la operación de cambio de contraseña.</span><span class="sxs-lookup"><span data-stu-id="bbd77-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="bbd77-129">**ChangePassword** modifica una contraseña mediante programación, sin interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="bbd77-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bbd77-130">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="bbd77-130">Notes to implementers</span></span>

<span data-ttu-id="bbd77-131">Los proveedores de transporte remoto implementan **ChangePassword** tal como se especifica aquí.</span><span class="sxs-lookup"><span data-stu-id="bbd77-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="bbd77-132">No hay ninguna consideración especial.</span><span class="sxs-lookup"><span data-stu-id="bbd77-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbd77-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbd77-133">See also</span></span>



[<span data-ttu-id="bbd77-134">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="bbd77-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="bbd77-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bbd77-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

