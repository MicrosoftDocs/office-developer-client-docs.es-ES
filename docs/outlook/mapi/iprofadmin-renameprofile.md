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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317083"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="52ebd-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="52ebd-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="52ebd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52ebd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52ebd-105">Asigna un nombre nuevo a un perfil.</span><span class="sxs-lookup"><span data-stu-id="52ebd-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="52ebd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="52ebd-106">Parameters</span></span>

 <span data-ttu-id="52ebd-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="52ebd-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="52ebd-108">a Un puntero al nombre actual del perfil al que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="52ebd-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="52ebd-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="52ebd-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="52ebd-110">a Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="52ebd-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="52ebd-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="52ebd-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="52ebd-112">a Un puntero al nuevo nombre del perfil al que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="52ebd-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="52ebd-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="52ebd-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="52ebd-114">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="52ebd-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="52ebd-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52ebd-115">_ulFlags_</span></span>
  
> <span data-ttu-id="52ebd-116">a Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="52ebd-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52ebd-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52ebd-117">Return value</span></span>

<span data-ttu-id="52ebd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="52ebd-118">S_OK</span></span> 
  
> <span data-ttu-id="52ebd-119">Se cambió el nombre del perfil correctamente.</span><span class="sxs-lookup"><span data-stu-id="52ebd-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="52ebd-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="52ebd-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="52ebd-121">La contraseña del perfil es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="52ebd-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="52ebd-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="52ebd-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="52ebd-123">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="52ebd-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="52ebd-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52ebd-124">Remarks</span></span>

<span data-ttu-id="52ebd-125">El método **IProfAdmin:: RenameProfile** asigna un nuevo nombre a un perfil, si tiene uno.</span><span class="sxs-lookup"><span data-stu-id="52ebd-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="52ebd-126">Si el perfil al que se va a cambiar el nombre lo está usando un cliente cuando se llama a **RenameProfile** , **RenameProfile** marca el perfil y Devuelve S_OK en lugar de intentar la operación de cambio de nombre mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="52ebd-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="52ebd-127">Cuando el perfil ya no se usa, **RenameProfile** le asigna el nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="52ebd-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="52ebd-128">Los nombres antiguos y nuevos del perfil pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="52ebd-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="52ebd-129">Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="52ebd-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="52ebd-130">Espacios insertados, pero no espacios iniciales ni finales.</span><span class="sxs-lookup"><span data-stu-id="52ebd-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="52ebd-131">_LpszPassword_ siempre debe ser null o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="52ebd-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52ebd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="52ebd-132">See also</span></span>



[<span data-ttu-id="52ebd-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52ebd-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

