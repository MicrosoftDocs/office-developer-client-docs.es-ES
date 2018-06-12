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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: cf5060ba2113032fe1e13e5417590006808a53e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817891"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="b1340-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1340-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="b1340-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1340-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1340-105">Establece o borra el perfil predeterminado de un cliente.</span><span class="sxs-lookup"><span data-stu-id="b1340-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b1340-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1340-106">Parameters</span></span>

 <span data-ttu-id="b1340-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="b1340-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="b1340-108">[entrada] Un puntero al nombre del perfil que va a convertirse en el valor predeterminado o NULL.</span><span class="sxs-lookup"><span data-stu-id="b1340-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="b1340-109">Si el valor _lpszProfileName_ NULL indica que **SetDefaultProfile** debe quitar el perfil predeterminado existente, dejando al cliente sin un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b1340-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="b1340-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1340-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b1340-111">[entrada] Una máscara de bits de indicadores que controla el tipo de la cadena indicada por _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="b1340-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="b1340-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="b1340-112">The following flag can be set:</span></span>
    
<span data-ttu-id="b1340-113">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b1340-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1340-114">El nombre del perfil está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1340-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="b1340-115">Si no está establecido el indicador MAPI_UNICODE., el nombre del perfil está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1340-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1340-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1340-116">Return value</span></span>

<span data-ttu-id="b1340-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1340-117">S_OK</span></span> 
  
> <span data-ttu-id="b1340-118">Un perfil predeterminado se establece o se quitó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1340-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="b1340-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b1340-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b1340-120">No existe el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="b1340-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1340-121">Notas</span><span class="sxs-lookup"><span data-stu-id="b1340-121">Remarks</span></span>

<span data-ttu-id="b1340-122">El método **IProfAdmin::SetDefaultProfile** establece un perfil determinado como el perfil del cliente predeterminado o borra el perfil predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="b1340-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="b1340-123">El perfil predeterminado es el perfil que se usa automáticamente cada vez que el cliente inicia una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1340-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="b1340-124">**SetDefaultProfile** también establece la propiedad de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) del perfil predeterminado nuevo en TRUE.</span><span class="sxs-lookup"><span data-stu-id="b1340-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1340-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b1340-125">Notes to callers</span></span>

<span data-ttu-id="b1340-126">Para iniciar una sesión con el perfil predeterminado, pase el indicador MAPI_USE_DEFAULT a la función [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="b1340-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1340-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="b1340-127">See also</span></span>



[<span data-ttu-id="b1340-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="b1340-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="b1340-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="b1340-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="b1340-130">Propiedad canónico PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1340-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="b1340-131">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1340-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

