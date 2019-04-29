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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439922"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="d73ef-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="d73ef-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="d73ef-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d73ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d73ef-105">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="d73ef-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="d73ef-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d73ef-106">Parameters</span></span>

 <span data-ttu-id="d73ef-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d73ef-107">_lpUID_</span></span>
  
> <span data-ttu-id="d73ef-108">a Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d73ef-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="d73ef-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d73ef-109">_lpInterface_</span></span>
  
> <span data-ttu-id="d73ef-110">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d73ef-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="d73ef-111">Pasar NULL hace que el parámetro _lppProfSect_ devuelva un puntero a la interfaz estándar de la sección del perfil, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="d73ef-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="d73ef-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d73ef-112">_ulFlags_</span></span>
  
> <span data-ttu-id="d73ef-113">a Una máscara de máscara de marcas que controla el acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d73ef-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="d73ef-114">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d73ef-114">The following flags can be set:</span></span>
    
<span data-ttu-id="d73ef-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d73ef-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d73ef-116">Permite que **OpenProfileSection** se devuelva correctamente, posiblemente antes de que la sección de perfil esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="d73ef-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="d73ef-117">Si la sección de perfil no está disponible, realizar una llamada subsiguiente al mismo puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="d73ef-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="d73ef-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d73ef-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="d73ef-119">Permite el acceso a una sección de perfil que no pertenece al proveedor.</span><span class="sxs-lookup"><span data-stu-id="d73ef-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="d73ef-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d73ef-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d73ef-121">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d73ef-121">Requests read/write permission.</span></span> <span data-ttu-id="d73ef-122">De forma predeterminada, las secciones de perfil se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d73ef-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="d73ef-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="d73ef-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="d73ef-124">contempla Un puntero a un puntero a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="d73ef-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d73ef-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d73ef-125">Return value</span></span>

<span data-ttu-id="d73ef-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="d73ef-126">S_OK</span></span> 
  
> <span data-ttu-id="d73ef-127">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d73ef-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="d73ef-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d73ef-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d73ef-129">Se intentó obtener acceso a una sección de perfil para la que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="d73ef-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="d73ef-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d73ef-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d73ef-131">La sección de perfil solicitada no existe.</span><span class="sxs-lookup"><span data-stu-id="d73ef-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d73ef-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d73ef-132">Remarks</span></span>

<span data-ttu-id="d73ef-133">El método **IMAPISession:: OpenProfileSection** abre una sección o un objeto de perfil que admite la interfaz **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="d73ef-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="d73ef-134">Las secciones de perfil se usan para leer información y escribir información en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="d73ef-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="d73ef-135">No puede usar **OpenProfileSection** para abrir secciones de perfil que sean propias de proveedores de servicios individuales a menos que especifique MAPI_FORCE_ACCESS en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d73ef-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d73ef-136">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d73ef-136">Notes to callers</span></span>

<span data-ttu-id="d73ef-137">Varios clientes pueden abrir una sección de perfil con permiso de solo lectura, pero solo un cliente puede abrir una sección de perfil con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d73ef-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="d73ef-138">Si otro cliente tiene una sección de perfil abierta que intenta abrir llamando a **OpenProfileSection** con el indicador MAPI_MODIFY, se producirá un error en la llamada y se devolverá MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="d73ef-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="d73ef-139">Se producirá un error en una operación de apertura de sólo lectura si la sección está abierta para la escritura.</span><span class="sxs-lookup"><span data-stu-id="d73ef-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="d73ef-140">Puede crear una sección de perfil llamando a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura **MAPIUID** no existente en el parámetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="d73ef-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="d73ef-141">Asegúrese de especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d73ef-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="d73ef-142">Si establece _lpUID_ para que apunte a una **MAPIUID** no existente y **OpenProfileSection** se establece para usar el modo de acceso predeterminado de solo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="d73ef-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d73ef-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="d73ef-143">See also</span></span>



[<span data-ttu-id="d73ef-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d73ef-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d73ef-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d73ef-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="d73ef-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d73ef-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d73ef-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d73ef-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

