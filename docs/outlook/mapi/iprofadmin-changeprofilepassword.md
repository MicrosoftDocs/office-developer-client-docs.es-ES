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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817892"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="4f09f-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="4f09f-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="4f09f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f09f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f09f-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="4f09f-105">Deprecated.</span></span> <span data-ttu-id="4f09f-106">Cambia la contraseña de un perfil.</span><span class="sxs-lookup"><span data-stu-id="4f09f-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4f09f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f09f-107">Parameters</span></span>

 <span data-ttu-id="4f09f-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="4f09f-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="4f09f-109">[entrada] Un puntero al nombre del perfil asociado con la contraseña que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="4f09f-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="4f09f-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="4f09f-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="4f09f-111">[entrada] Un puntero a la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="4f09f-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="4f09f-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="4f09f-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="4f09f-113">[entrada] Un puntero a la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="4f09f-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="4f09f-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f09f-114">_ulFlags_</span></span>
  
> <span data-ttu-id="4f09f-115">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas que se pasan en.</span><span class="sxs-lookup"><span data-stu-id="4f09f-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="4f09f-116">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f09f-116">The following flag can be set:</span></span>
    
<span data-ttu-id="4f09f-117">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4f09f-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4f09f-118">El nombre del perfil y las contraseñas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f09f-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="4f09f-119">Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4f09f-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f09f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f09f-120">Return value</span></span>

<span data-ttu-id="4f09f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f09f-121">S_OK</span></span> 
  
> <span data-ttu-id="4f09f-122">Si se llama a este método, devolverá S_OK.</span><span class="sxs-lookup"><span data-stu-id="4f09f-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="4f09f-123">Sin embargo, no se realizará ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="4f09f-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f09f-124">Notas</span><span class="sxs-lookup"><span data-stu-id="4f09f-124">Remarks</span></span>

<span data-ttu-id="4f09f-125">No use este método.</span><span class="sxs-lookup"><span data-stu-id="4f09f-125">Do not use this method.</span></span> <span data-ttu-id="4f09f-126">MAPI no admite las contraseñas para los perfiles.</span><span class="sxs-lookup"><span data-stu-id="4f09f-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f09f-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f09f-127">See also</span></span>



[<span data-ttu-id="4f09f-128">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f09f-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

