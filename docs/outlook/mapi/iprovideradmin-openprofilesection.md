---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 276a2bd84156e9b396df71f51130e6704ad7c7fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817915"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="5355c-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5355c-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="5355c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5355c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5355c-105">Abre una sección de perfil desde el perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="5355c-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="5355c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5355c-106">Parameters</span></span>

 <span data-ttu-id="5355c-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5355c-107">_lpUID_</span></span>
  
> <span data-ttu-id="5355c-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para la sección de perfil que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="5355c-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="5355c-109">Los clientes no deben pasar NULL para el parámetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="5355c-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="5355c-110">Proveedores de servicios pueden pasar NULL para recuperar el **MAPIUID** al que llaman desde sus funciones de punto de entrada de servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5355c-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="5355c-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5355c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="5355c-112">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="5355c-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="5355c-113">Si se pasa NULL da como resultado en la interfaz de estándar de la sección perfil (**IProfSect**) que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="5355c-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="5355c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5355c-114">_ulFlags_</span></span>
  
> <span data-ttu-id="5355c-115">[entrada] Una máscara de bits de indicadores que controla cómo se abre la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="5355c-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="5355c-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5355c-116">The following flags can be set:</span></span>
    
<span data-ttu-id="5355c-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5355c-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5355c-118">Permite **OpenProfileSection** devolver de correctamente, posiblemente antes de la sección de perfil es completamente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5355c-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="5355c-119">Si la sección de perfil no está disponible, realizar una llamada posterior a él puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="5355c-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="5355c-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5355c-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5355c-121">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5355c-121">Requests read/write permission.</span></span> <span data-ttu-id="5355c-122">De forma predeterminada, los objetos se abren con permiso de sólo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5355c-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="5355c-123">Permiso de lectura y escritura a las secciones del proveedor del perfil no se permiten a los clientes.</span><span class="sxs-lookup"><span data-stu-id="5355c-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="5355c-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5355c-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="5355c-125">Permite el acceso a todas las secciones de perfil, incluso los que pertenecen a los proveedores de servicios individuales.</span><span class="sxs-lookup"><span data-stu-id="5355c-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="5355c-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="5355c-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="5355c-127">[out] Un puntero a un puntero a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="5355c-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5355c-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5355c-128">Return value</span></span>

<span data-ttu-id="5355c-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="5355c-129">S_OK</span></span> 
  
> <span data-ttu-id="5355c-130">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="5355c-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="5355c-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5355c-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5355c-132">Se ha intentado modificar una sección de perfil de sólo lectura o tener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="5355c-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="5355c-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5355c-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5355c-134">La sección de perfil solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="5355c-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5355c-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5355c-135">Remarks</span></span>

<span data-ttu-id="5355c-136">El método **IProviderAdmin::OpenProfileSection** abre una sección de perfil, que permita el autor de la llamada leer información desde y, posiblemente, escribir información en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="5355c-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="5355c-137">Los clientes no pueden abrir las secciones de perfil que pertenecen a los proveedores mediante el método **OpenProfileSection** .</span><span class="sxs-lookup"><span data-stu-id="5355c-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="5355c-138">Varios clientes o proveedores de servicios pueden abrir simultáneamente una sección de perfil con permiso de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5355c-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="5355c-139">Sin embargo, cuando una sección de perfil está abierta con permiso de lectura y escritura, no hay otras llamadas pueden estar para abrir la sección, independientemente del tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="5355c-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="5355c-140">Si una sección de perfil se abre con permiso de sólo lectura, se producirá un error en una llamada posterior a la solicitud de permiso de lectura y escritura con MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="5355c-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="5355c-141">Del mismo modo, si una sección está abierta con permiso de lectura y escritura, también producirá una llamada posterior a la solicitud de permiso de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5355c-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5355c-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5355c-142">Notes to callers</span></span>

<span data-ttu-id="5355c-143">Si solicita **OpenProfileSection** para abrir una sección de perfil que no existe, pasando MAPI_MODIFY _ulFlags_ y se creará un desconocido **MAPIUID** en _lpUID_, la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="5355c-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="5355c-144">Si solicita que **OpenProfileSection** abrir una sección que no existe con permiso de sólo lectura, devuelve MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="5355c-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5355c-145">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5355c-145">MFCMAPI reference</span></span>

<span data-ttu-id="5355c-146">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5355c-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5355c-147">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5355c-147">**File**</span></span>|<span data-ttu-id="5355c-148">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="5355c-148">**Function**</span></span>|<span data-ttu-id="5355c-149">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5355c-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5355c-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5355c-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5355c-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5355c-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="5355c-152">MFCMAPI utiliza el método **IProviderAdmin::OpenProfileSection** para abrir una sección de perfil desde el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="5355c-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5355c-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="5355c-153">See also</span></span>



[<span data-ttu-id="5355c-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5355c-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="5355c-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5355c-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="5355c-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5355c-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5355c-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5355c-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="5355c-158">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="5355c-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

