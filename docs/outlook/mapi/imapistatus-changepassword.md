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
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410360"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="cccc9-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="cccc9-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="cccc9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cccc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cccc9-105">Modifica la contraseña de un proveedor de servicios sin mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cccc9-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="cccc9-106">Este método es compatible opcionalmente con los objetos de estado que implementan los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="cccc9-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cccc9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cccc9-107">Parameters</span></span>

 <span data-ttu-id="cccc9-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="cccc9-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="cccc9-109">a Un puntero a la contraseña antigua.</span><span class="sxs-lookup"><span data-stu-id="cccc9-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="cccc9-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="cccc9-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="cccc9-111">a Un puntero a la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="cccc9-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="cccc9-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cccc9-112">_ulFlags_</span></span>
  
> <span data-ttu-id="cccc9-113">a Una máscara de máscara de marcadores que controla el formato de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="cccc9-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="cccc9-114">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="cccc9-114">The following flag can be set:</span></span>
    
<span data-ttu-id="cccc9-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cccc9-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cccc9-116">Las contraseñas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cccc9-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="cccc9-117">Si no se establece la marca MAPI_UNICODE, las contraseñas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="cccc9-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cccc9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cccc9-118">Return value</span></span>

<span data-ttu-id="cccc9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cccc9-119">S_OK</span></span> 
  
> <span data-ttu-id="cccc9-120">La modificación de la contraseña se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cccc9-120">The password modification was successful.</span></span>
    
<span data-ttu-id="cccc9-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cccc9-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="cccc9-122">La contraseña anterior a la que apunta _lpOldPass_ no es válida.</span><span class="sxs-lookup"><span data-stu-id="cccc9-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="cccc9-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cccc9-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cccc9-124">El objeto status no admite esta operación, como indica la ausencia de la marca STATUS_CHANGE_PASSWORD en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="cccc9-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cccc9-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cccc9-125">Remarks</span></span>

<span data-ttu-id="cccc9-126">No todos los objetos status admiten el método **IMAPIStatus:: ChangePassword** .</span><span class="sxs-lookup"><span data-stu-id="cccc9-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="cccc9-127">Solo la admiten los proveedores de servicios que requieren que los clientes escriban una contraseña.</span><span class="sxs-lookup"><span data-stu-id="cccc9-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="cccc9-128">Ninguno de los objetos de estado que implementa MAPI admiten la operación de cambio de contraseña.</span><span class="sxs-lookup"><span data-stu-id="cccc9-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="cccc9-129">**ChangePassword** modifica una contraseña mediante programación, sin interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="cccc9-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cccc9-130">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="cccc9-130">Notes to implementers</span></span>

<span data-ttu-id="cccc9-131">Los proveedores de transporte remoto implementan **ChangePassword** tal y como se especifica aquí.</span><span class="sxs-lookup"><span data-stu-id="cccc9-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="cccc9-132">No hay ninguna consideración especial.</span><span class="sxs-lookup"><span data-stu-id="cccc9-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cccc9-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="cccc9-133">See also</span></span>



[<span data-ttu-id="cccc9-134">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="cccc9-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="cccc9-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cccc9-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

