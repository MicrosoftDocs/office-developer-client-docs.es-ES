---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e5f329ef0d3483683d5c94ed38c6631d86e77b93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817460"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="d8d6d-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d8d6d-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="d8d6d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8d6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8d6d-105">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="d8d6d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8d6d-106">Parameters</span></span>

 <span data-ttu-id="d8d6d-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d8d6d-107">_lpUID_</span></span>
  
> <span data-ttu-id="d8d6d-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="d8d6d-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d8d6d-109">_lpInterface_</span></span>
  
> <span data-ttu-id="d8d6d-110">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="d8d6d-111">Pasando NULL hace que el parámetro _lppProfSect_ devolver un puntero a la interfaz estándar de la sección de perfil, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="d8d6d-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8d6d-112">_ulFlags_</span></span>
  
> <span data-ttu-id="d8d6d-113">[entrada] Una máscara de bits de indicadores que controla el acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="d8d6d-114">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d8d6d-114">The following flags can be set:</span></span>
    
<span data-ttu-id="d8d6d-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d8d6d-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d8d6d-116">Permite **OpenProfileSection** devolver correctamente, posiblemente antes el perfil de sección es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="d8d6d-117">Si la sección de perfil no está disponible, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="d8d6d-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d8d6d-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="d8d6d-119">Permite el acceso a una sección de perfil que no pertenecen al proveedor.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="d8d6d-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d8d6d-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d8d6d-121">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-121">Requests read/write permission.</span></span> <span data-ttu-id="d8d6d-122">De forma predeterminada, las secciones del perfil se abren con permiso de sólo lectura, y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="d8d6d-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="d8d6d-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="d8d6d-124">[out] Un puntero a un puntero a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8d6d-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8d6d-125">Return value</span></span>

<span data-ttu-id="d8d6d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8d6d-126">S_OK</span></span> 
  
> <span data-ttu-id="d8d6d-127">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="d8d6d-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d8d6d-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d8d6d-129">Se ha intentado tener acceso a una sección de perfil para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="d8d6d-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d8d6d-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d8d6d-131">La sección de perfil solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8d6d-132">Notas</span><span class="sxs-lookup"><span data-stu-id="d8d6d-132">Remarks</span></span>

<span data-ttu-id="d8d6d-133">El método **IMAPISession::OpenProfileSection** abre una sección de perfil o un objeto que admite la interfaz **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="d8d6d-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="d8d6d-134">Las secciones de perfil se usan para lectura y escritura de información en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="d8d6d-135">No se puede usar **OpenProfileSection** para abrir las secciones del perfil que proveedores de servicio individuales propio a menos que especifique el parámetro _ulFlags_ MAPI_FORCE_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d8d6d-136">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d8d6d-136">Notes to callers</span></span>

<span data-ttu-id="d8d6d-137">Varios clientes pueden abrir una sección de perfil con permiso de sólo lectura, pero sólo un cliente puede abrir una sección de perfil con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="d8d6d-138">Si otro cliente tiene una sección de perfil abierto que intenta abrir llamando a **OpenProfileSection** con el conjunto de marca MAPI_MODIFY, la llamada se producirá un error, devolver MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="d8d6d-139">Se produce un error en una operación de apertura de sólo lectura si la sección está abierta para escribir en él.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="d8d6d-140">Puede crear una sección de perfil mediante una llamada a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura **MAPIUID** que no existe en el parámetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="d8d6d-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="d8d6d-141">Asegúrese de que especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="d8d6d-142">Si se establece _lpUID_ para que apunte a una que no existe **MAPIUID** y **OpenProfileSection** está configurado para usar el modo de acceso predeterminada de sólo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="d8d6d-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8d6d-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="d8d6d-143">See also</span></span>



[<span data-ttu-id="d8d6d-144">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8d6d-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d8d6d-145">IProfSect: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d8d6d-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="d8d6d-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d8d6d-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d8d6d-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8d6d-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

