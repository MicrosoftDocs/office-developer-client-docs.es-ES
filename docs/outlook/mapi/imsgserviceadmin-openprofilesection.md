---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817732"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="12eaa-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="12eaa-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="12eaa-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12eaa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12eaa-105">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="12eaa-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="12eaa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12eaa-106">Parameters</span></span>

 <span data-ttu-id="12eaa-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="12eaa-107">_lpUID_</span></span>
  
> <span data-ttu-id="12eaa-108">Un puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="12eaa-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="12eaa-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="12eaa-109">_lpInterface_</span></span>
  
> <span data-ttu-id="12eaa-110">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="12eaa-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="12eaa-111">Si se pasa NULL da como resultado un puntero a su interfaz estándar que se devuelven en el parámetro _lppProfSect_ .</span><span class="sxs-lookup"><span data-stu-id="12eaa-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="12eaa-112">La interfaz estándar para una sección de perfil es **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="12eaa-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="12eaa-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="12eaa-113">_ulFlags_</span></span>
  
> <span data-ttu-id="12eaa-114">[entrada] Una máscara de bits de indicadores que controla el acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="12eaa-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="12eaa-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="12eaa-115">The following flags can be set:</span></span>
    
<span data-ttu-id="12eaa-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="12eaa-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="12eaa-117">Permite **OpenProfileSection** devolver correctamente, posiblemente antes el perfil de sección es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="12eaa-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="12eaa-118">Si la sección de perfil no está disponible, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="12eaa-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="12eaa-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="12eaa-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="12eaa-120">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="12eaa-120">Requests read/write permission.</span></span> <span data-ttu-id="12eaa-121">De forma predeterminada, las secciones del perfil se abren con permiso de sólo lectura, y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="12eaa-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="12eaa-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="12eaa-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="12eaa-123">Permite el acceso a todas las secciones de perfil, incluso los que pertenecen a los proveedores de servicios individuales.</span><span class="sxs-lookup"><span data-stu-id="12eaa-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="12eaa-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="12eaa-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="12eaa-125">[out] Un puntero a un puntero a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="12eaa-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12eaa-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12eaa-126">Return value</span></span>

<span data-ttu-id="12eaa-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="12eaa-127">S_OK</span></span> 
  
> <span data-ttu-id="12eaa-128">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="12eaa-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="12eaa-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="12eaa-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="12eaa-130">Se ha intentado tener acceso a una sección de perfil para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="12eaa-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="12eaa-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="12eaa-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="12eaa-132">La sección de perfil solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="12eaa-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12eaa-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12eaa-133">Remarks</span></span>

<span data-ttu-id="12eaa-134">El método **IMsgServiceAdmin::OpenProfileSection** abre una sección de perfil, un objeto que admite la interfaz [IProfSect](iprofsectimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="12eaa-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="12eaa-135">Las secciones de perfil se usan para lectura y escritura de información en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="12eaa-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="12eaa-136">**OpenProfileSection** no se puede usar para abrir secciones de perfil que son propiedad de los proveedores de servicios individuales, a menos que se usa MAPI_FORCE_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="12eaa-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="12eaa-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="12eaa-137">Notes to callers</span></span>

<span data-ttu-id="12eaa-138">Varios clientes pueden abrir una sección de perfil con permiso de sólo lectura, pero sólo un cliente puede abrir una sección de perfil con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="12eaa-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="12eaa-139">Si otro cliente tiene una sección de perfil abierto que intenta abrir llamando a **OpenProfileSection** con el conjunto de marca MAPI_MODIFY, la llamada se producirá un error, devolver MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="12eaa-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="12eaa-140">Se produce un error en una operación de apertura de sólo lectura si la sección está abierta para escribir en él.</span><span class="sxs-lookup"><span data-stu-id="12eaa-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="12eaa-141">Puede crear una sección de perfil mediante una llamada a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura [MAPIUID](mapiuid.md) que no existe en el parámetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="12eaa-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="12eaa-142">No olvide que especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="12eaa-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="12eaa-143">Si se establece _lpUID_ para que apunte a una que no existe **MAPIUID** y **OpenProfileSection** está configurado para usar el modo de acceso predeterminada de sólo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="12eaa-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="12eaa-144">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="12eaa-144">MFCMAPI reference</span></span>

<span data-ttu-id="12eaa-145">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="12eaa-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="12eaa-146">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="12eaa-146">**File**</span></span>|<span data-ttu-id="12eaa-147">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="12eaa-147">**Function**</span></span>|<span data-ttu-id="12eaa-148">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="12eaa-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12eaa-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="12eaa-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="12eaa-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="12eaa-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="12eaa-151">MFCMAPI utiliza el método **IMsgServiceAdmin::OpenProfileSection** para abrir una sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="12eaa-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12eaa-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="12eaa-152">See also</span></span>



[<span data-ttu-id="12eaa-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12eaa-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="12eaa-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="12eaa-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="12eaa-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="12eaa-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="12eaa-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="12eaa-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="12eaa-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12eaa-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="12eaa-158">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="12eaa-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

