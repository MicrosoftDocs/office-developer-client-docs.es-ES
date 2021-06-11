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
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419523"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="6ba02-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="6ba02-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="6ba02-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ba02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ba02-105">Asigna un nuevo nombre a un perfil.</span><span class="sxs-lookup"><span data-stu-id="6ba02-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6ba02-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6ba02-106">Parameters</span></span>

 <span data-ttu-id="6ba02-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="6ba02-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="6ba02-108">[in] Puntero al nombre actual del perfil para cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="6ba02-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="6ba02-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="6ba02-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="6ba02-110">[in] Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="6ba02-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="6ba02-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="6ba02-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="6ba02-112">[in] Puntero al nuevo nombre del perfil al que se cambiará el nombre.</span><span class="sxs-lookup"><span data-stu-id="6ba02-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="6ba02-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6ba02-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6ba02-114">[in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="6ba02-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="6ba02-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ba02-115">_ulFlags_</span></span>
  
> <span data-ttu-id="6ba02-116">[in] Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="6ba02-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ba02-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba02-117">Return value</span></span>

<span data-ttu-id="6ba02-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ba02-118">S_OK</span></span> 
  
> <span data-ttu-id="6ba02-119">El nombre del perfil se cambió correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ba02-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="6ba02-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="6ba02-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="6ba02-121">La contraseña del perfil es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="6ba02-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="6ba02-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6ba02-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6ba02-123">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6ba02-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6ba02-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ba02-124">Remarks</span></span>

<span data-ttu-id="6ba02-125">El **método IProfAdmin::RenameProfile** asigna un nuevo nombre a un perfil, si tiene uno.</span><span class="sxs-lookup"><span data-stu-id="6ba02-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="6ba02-126">Si un cliente usa el perfil para cambiar el nombre cuando se llama a **RenameProfile,** **RenameProfile** marca el perfil y devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="6ba02-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="6ba02-127">Cuando el perfil ya no se usa, **RenameProfile** le asigna el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="6ba02-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="6ba02-128">Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres y pueden incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="6ba02-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="6ba02-129">Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="6ba02-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="6ba02-130">Espacios incrustados, pero no espacios iniciales o finales.</span><span class="sxs-lookup"><span data-stu-id="6ba02-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="6ba02-131">_LpszPassword_ siempre debe ser NULL o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="6ba02-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ba02-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba02-132">See also</span></span>



[<span data-ttu-id="6ba02-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ba02-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

