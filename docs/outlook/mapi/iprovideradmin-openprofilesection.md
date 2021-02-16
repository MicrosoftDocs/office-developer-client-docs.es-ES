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
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405663"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="ff057-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ff057-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="ff057-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff057-105">Abre una sección de perfil del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="ff057-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="ff057-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff057-106">Parameters</span></span>

 <span data-ttu-id="ff057-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="ff057-107">_lpUID_</span></span>
  
> <span data-ttu-id="ff057-108">[entrada] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único de la sección de perfil que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="ff057-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="ff057-109">Los clientes no deben pasar NULL para el _parámetro lpUID._</span><span class="sxs-lookup"><span data-stu-id="ff057-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="ff057-110">Los proveedores de servicios pueden pasar NULL para recuperar **MAPIUID** cuando llaman desde sus funciones de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff057-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="ff057-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ff057-111">_lpInterface_</span></span>
  
> <span data-ttu-id="ff057-112">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="ff057-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="ff057-113">Si se pasa NULL, se devuelve la interfaz estándar de la sección de perfil (**IProfSect**).</span><span class="sxs-lookup"><span data-stu-id="ff057-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="ff057-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff057-114">_ulFlags_</span></span>
  
> <span data-ttu-id="ff057-115">[entrada] Máscara de bits de marcas que controla cómo se abre la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="ff057-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="ff057-116">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="ff057-116">The following flags can be set:</span></span>
    
<span data-ttu-id="ff057-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ff057-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ff057-118">Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil esté totalmente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ff057-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="ff057-119">Si la sección de perfil no está disponible, realizar una llamada posterior a ella puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="ff057-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="ff057-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ff057-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ff057-121">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ff057-121">Requests read/write permission.</span></span> <span data-ttu-id="ff057-122">De forma predeterminada, los objetos se abren con permiso de solo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ff057-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="ff057-123">No se permite a los clientes permiso de lectura y escritura para las secciones del proveedor del perfil.</span><span class="sxs-lookup"><span data-stu-id="ff057-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="ff057-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff057-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="ff057-125">Permite el acceso a todas las secciones de perfil, incluso a las que pertenecen a proveedores de servicios individuales.</span><span class="sxs-lookup"><span data-stu-id="ff057-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="ff057-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="ff057-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="ff057-127">[salida] Puntero a un puntero a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="ff057-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff057-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff057-128">Return value</span></span>

<span data-ttu-id="ff057-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff057-129">S_OK</span></span> 
  
> <span data-ttu-id="ff057-130">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff057-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="ff057-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ff057-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ff057-132">Se intentó modificar una sección de perfil de solo lectura o obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="ff057-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="ff057-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ff057-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ff057-134">La sección de perfil solicitada no existe.</span><span class="sxs-lookup"><span data-stu-id="ff057-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff057-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff057-135">Remarks</span></span>

<span data-ttu-id="ff057-136">El **método IProviderAdmin::OpenProfileSection** abre una sección de perfil, lo que permite al autor de la llamada leer información y, posiblemente, escribir información en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="ff057-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="ff057-137">Los clientes no pueden abrir secciones de perfil que pertenezcan a proveedores mediante el **método OpenProfileSection.**</span><span class="sxs-lookup"><span data-stu-id="ff057-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="ff057-138">Varios clientes o proveedores de servicios pueden abrir simultáneamente una sección de perfil con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff057-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="ff057-139">Sin embargo, cuando se abre una sección de perfil con permiso de lectura y escritura, no se pueden realizar otras llamadas para abrir la sección, independientemente del tipo de acceso.</span><span class="sxs-lookup"><span data-stu-id="ff057-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="ff057-140">Si se abre una sección de perfil con permiso de solo lectura, se producirá un error en una llamada posterior para solicitar permiso de lectura y escritura con MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="ff057-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="ff057-141">Del mismo modo, si una sección está abierta con permiso de lectura y escritura, también se producirá un error en una llamada posterior para solicitar el permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff057-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff057-142">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ff057-142">Notes to callers</span></span>

<span data-ttu-id="ff057-143">Si solicita que **OpenProfileSection** abra una sección de perfil que no existe pasando MAPI_MODIFY  _en ulFlags_ y un **MAPIUID** desconocido en  _lpUID,_ se creará la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="ff057-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="ff057-144">Si solicita que **OpenProfileSection** abra una sección que no existe con permiso de solo lectura, devolverá MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="ff057-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff057-145">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff057-145">MFCMAPI reference</span></span>

<span data-ttu-id="ff057-146">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ff057-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff057-147">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ff057-147">**File**</span></span>|<span data-ttu-id="ff057-148">**Función**</span><span class="sxs-lookup"><span data-stu-id="ff057-148">**Function**</span></span>|<span data-ttu-id="ff057-149">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ff057-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff057-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ff057-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ff057-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ff057-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="ff057-152">MFCMAPI usa el **método IProviderAdmin::OpenProfileSection** para abrir una sección de perfil desde el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="ff057-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff057-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ff057-153">See also</span></span>



[<span data-ttu-id="ff057-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff057-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ff057-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff057-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="ff057-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ff057-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ff057-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff057-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="ff057-158">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ff057-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

