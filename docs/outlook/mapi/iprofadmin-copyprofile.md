---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437241"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="cf418-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="cf418-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="cf418-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf418-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf418-105">Copia un perfil.</span><span class="sxs-lookup"><span data-stu-id="cf418-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf418-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf418-106">Parameters</span></span>

 <span data-ttu-id="cf418-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="cf418-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="cf418-108">a Un puntero al nombre del perfil que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="cf418-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="cf418-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="cf418-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="cf418-110">a Un puntero a la contraseña del perfil que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="cf418-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="cf418-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="cf418-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="cf418-112">a Un puntero al nuevo nombre del perfil copiado.</span><span class="sxs-lookup"><span data-stu-id="cf418-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="cf418-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cf418-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="cf418-114">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="cf418-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="cf418-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf418-115">_ulFlags_</span></span>
  
> <span data-ttu-id="cf418-116">a Una máscara de máscara de marcadores que controla cómo se copia el perfil.</span><span class="sxs-lookup"><span data-stu-id="cf418-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="cf418-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="cf418-117">The following flags can be set:</span></span>
    
<span data-ttu-id="cf418-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="cf418-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="cf418-119">Muestra un cuadro de diálogo que solicita al usuario la contraseña correcta del perfil que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="cf418-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="cf418-120">Si no se establece esta marca, no se muestra ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cf418-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf418-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf418-121">Return value</span></span>

<span data-ttu-id="cf418-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf418-122">S_OK</span></span> 
  
> <span data-ttu-id="cf418-123">El perfil se copió correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf418-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="cf418-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="cf418-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="cf418-125">El nombre del nuevo perfil es el mismo que el de un perfil existente.</span><span class="sxs-lookup"><span data-stu-id="cf418-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="cf418-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="cf418-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="cf418-127">La contraseña del perfil para copiar no es correcta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta porque MAPI_DIALOG no se estableció en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="cf418-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="cf418-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cf418-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cf418-129">El perfil especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="cf418-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="cf418-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="cf418-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="cf418-131">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cf418-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf418-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf418-132">Remarks</span></span>

<span data-ttu-id="cf418-133">El método **IProfAdmin:: CopyProfile** hace una copia del perfil apuntado por _lpszOldProfileName_, dándole el nombre que apunta a _lpszNewProfileName_.</span><span class="sxs-lookup"><span data-stu-id="cf418-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="cf418-134">La copia de un perfil deja la copia con la misma contraseña que la original.</span><span class="sxs-lookup"><span data-stu-id="cf418-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="cf418-135">El nombre del perfil original, su contraseña y la copia pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="cf418-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="cf418-136">Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="cf418-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="cf418-137">Espacios insertados, pero no espacios iniciales ni finales.</span><span class="sxs-lookup"><span data-stu-id="cf418-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="cf418-138">Las contraseñas de perfil no son compatibles con todos los sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="cf418-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="cf418-139">En los sistemas operativos que no admiten contraseñas de perfil, _lpszOldPassword_ puede ser null o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="cf418-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="cf418-140">Si _lpszOldPassword_ se establece en null, el perfil que se va a copiar requiere una contraseña y se establece la marca MAPI_DIALOG; se muestra un cuadro de diálogo que solicita al usuario que especifique la contraseña.</span><span class="sxs-lookup"><span data-stu-id="cf418-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="cf418-141">Si se requiere una contraseña, pero _lpszOldPassword_ está establecida en NULL y la marca MAPI_DIALOG no está establecida, **CopyProfile** devuelve MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="cf418-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf418-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="cf418-142">See also</span></span>



[<span data-ttu-id="cf418-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf418-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

