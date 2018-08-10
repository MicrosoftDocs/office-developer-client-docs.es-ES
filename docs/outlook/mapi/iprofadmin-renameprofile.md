---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817887"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="d062e-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="d062e-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="d062e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d062e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d062e-105">Asigna un nombre nuevo a un perfil.</span><span class="sxs-lookup"><span data-stu-id="d062e-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d062e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d062e-106">Parameters</span></span>

 <span data-ttu-id="d062e-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="d062e-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="d062e-108">[entrada] Un puntero al nombre del perfil para cambiar el nombre actual.</span><span class="sxs-lookup"><span data-stu-id="d062e-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="d062e-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="d062e-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="d062e-110">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="d062e-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="d062e-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="d062e-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="d062e-112">[entrada] Un puntero al nuevo nombre del perfil para cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="d062e-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="d062e-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d062e-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="d062e-114">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="d062e-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="d062e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d062e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="d062e-116">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="d062e-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d062e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d062e-117">Return value</span></span>

<span data-ttu-id="d062e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d062e-118">S_OK</span></span> 
  
> <span data-ttu-id="d062e-119">Se cambió correctamente el perfil.</span><span class="sxs-lookup"><span data-stu-id="d062e-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="d062e-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="d062e-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="d062e-121">La contraseña de perfil es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="d062e-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="d062e-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d062e-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d062e-123">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d062e-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d062e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d062e-124">Remarks</span></span>

<span data-ttu-id="d062e-125">El método **IProfAdmin::RenameProfile** asigna un nuevo nombre a un perfil, si tiene uno.</span><span class="sxs-lookup"><span data-stu-id="d062e-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="d062e-126">Si el perfil para cambiar el nombre está en uso por un cliente cuando se llama a **RenameProfile** , **RenameProfile** marca el perfil y devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="d062e-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="d062e-127">Cuando ya no se usa el perfil, **RenameProfile** se asigna el nombre nuevo.</span><span class="sxs-lookup"><span data-stu-id="d062e-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="d062e-128">Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="d062e-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="d062e-129">Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="d062e-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="d062e-130">Espacios incrustados, pero no espacios al principio o al final.</span><span class="sxs-lookup"><span data-stu-id="d062e-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="d062e-131">El _lpszPassword_ siempre debe ser NULL o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="d062e-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d062e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d062e-132">See also</span></span>



[<span data-ttu-id="d062e-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d062e-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
