---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317125"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="95eff-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="95eff-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="95eff-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95eff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95eff-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="95eff-105">Deprecated.</span></span> <span data-ttu-id="95eff-106">Cambia la contraseña de un perfil.</span><span class="sxs-lookup"><span data-stu-id="95eff-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="95eff-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="95eff-107">Parameters</span></span>

 <span data-ttu-id="95eff-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="95eff-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="95eff-109">a Un puntero al nombre del perfil asociado con la contraseña que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="95eff-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="95eff-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="95eff-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="95eff-111">a Un puntero a la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="95eff-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="95eff-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="95eff-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="95eff-113">a Un puntero a la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="95eff-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="95eff-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95eff-114">_ulFlags_</span></span>
  
> <span data-ttu-id="95eff-115">a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas.</span><span class="sxs-lookup"><span data-stu-id="95eff-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="95eff-116">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="95eff-116">The following flag can be set:</span></span>
    
<span data-ttu-id="95eff-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95eff-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="95eff-118">El nombre del perfil y las contraseñas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="95eff-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="95eff-119">Si no se establece la marca MAPI_UNICODE, estas cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="95eff-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95eff-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95eff-120">Return value</span></span>

<span data-ttu-id="95eff-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="95eff-121">S_OK</span></span> 
  
> <span data-ttu-id="95eff-122">Si se llama a este método, devolverá S_OK.</span><span class="sxs-lookup"><span data-stu-id="95eff-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="95eff-123">Sin embargo, no se llevará a cabo ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="95eff-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95eff-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95eff-124">Remarks</span></span>

<span data-ttu-id="95eff-125">No use este método.</span><span class="sxs-lookup"><span data-stu-id="95eff-125">Do not use this method.</span></span> <span data-ttu-id="95eff-126">MAPI no admite contraseñas para los perfiles.</span><span class="sxs-lookup"><span data-stu-id="95eff-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95eff-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="95eff-127">See also</span></span>



[<span data-ttu-id="95eff-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95eff-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

