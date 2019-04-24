---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270171"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="d5ce8-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ce8-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="d5ce8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5ce8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5ce8-105">Establece o borra el perfil predeterminado de un cliente.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d5ce8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5ce8-106">Parameters</span></span>

 <span data-ttu-id="d5ce8-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="d5ce8-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="d5ce8-108">a Un puntero al nombre del perfil que se convertirá en el valor predeterminado o NULL.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="d5ce8-109">Establecer _lpszProfileName_ en NULL indica que **setdefaultprofile a** debe quitar el perfil predeterminado existente, dejando el cliente sin un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="d5ce8-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5ce8-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d5ce8-111">a Máscara de máscara de marcadores que controla el tipo de la cadena a la que apunta _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="d5ce8-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="d5ce8-112">The following flag can be set:</span></span>
    
<span data-ttu-id="d5ce8-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5ce8-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d5ce8-114">El nombre del perfil está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="d5ce8-115">Si no se establece la marca MAPI_UNICODE, el nombre del perfil está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5ce8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5ce8-116">Return value</span></span>

<span data-ttu-id="d5ce8-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5ce8-117">S_OK</span></span> 
  
> <span data-ttu-id="d5ce8-118">Un perfil predeterminado se estableció o quitó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="d5ce8-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d5ce8-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d5ce8-120">El perfil especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5ce8-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5ce8-121">Remarks</span></span>

<span data-ttu-id="d5ce8-122">El método **IProfAdmin:: setdefaultprofile a** establece un perfil en particular como perfil predeterminado del cliente o borra el perfil predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="d5ce8-123">El perfil predeterminado es el que se usa automáticamente siempre que el cliente inicia una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="d5ce8-124">**Setdefaultprofile a** también establece la propiedad **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) del nuevo perfil predeterminado en true.</span><span class="sxs-lookup"><span data-stu-id="d5ce8-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5ce8-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d5ce8-125">Notes to callers</span></span>

<span data-ttu-id="d5ce8-126">Para iniciar una sesión con el perfil predeterminado, pase la marca MAPI_USE_DEFAULT a la función [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ce8-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5ce8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5ce8-127">See also</span></span>



[<span data-ttu-id="d5ce8-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="d5ce8-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="d5ce8-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="d5ce8-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="d5ce8-130">Propiedad canónica PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ce8-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="d5ce8-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5ce8-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

