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
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437115"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="35ce0-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="35ce0-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="35ce0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35ce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35ce0-105">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="35ce0-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="35ce0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="35ce0-106">Parameters</span></span>

 <span data-ttu-id="35ce0-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="35ce0-107">_lpUID_</span></span>
  
> <span data-ttu-id="35ce0-108">Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="35ce0-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="35ce0-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="35ce0-109">_lpInterface_</span></span>
  
> <span data-ttu-id="35ce0-110">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="35ce0-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="35ce0-111">Si se pasa NULL, se devuelve un puntero a su interfaz estándar en el _parámetro lppProfSect._</span><span class="sxs-lookup"><span data-stu-id="35ce0-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="35ce0-112">La interfaz estándar para una sección de perfil es **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="35ce0-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="35ce0-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35ce0-113">_ulFlags_</span></span>
  
> <span data-ttu-id="35ce0-114">[in] Máscara de bits de marcas que controla el acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="35ce0-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="35ce0-115">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="35ce0-115">The following flags can be set:</span></span>
    
<span data-ttu-id="35ce0-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="35ce0-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="35ce0-117">Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil esté totalmente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="35ce0-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="35ce0-118">Si la sección de perfil no está disponible, realizar una llamada posterior a ella puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="35ce0-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="35ce0-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="35ce0-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="35ce0-120">Solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="35ce0-120">Requests read/write permission.</span></span> <span data-ttu-id="35ce0-121">De forma predeterminada, las secciones de perfil se abren con permiso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="35ce0-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="35ce0-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="35ce0-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="35ce0-123">Permite el acceso a todas las secciones de perfil, incluso las que pertenecen a proveedores de servicios individuales.</span><span class="sxs-lookup"><span data-stu-id="35ce0-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="35ce0-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="35ce0-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="35ce0-125">[salida] Puntero a un puntero a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="35ce0-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35ce0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35ce0-126">Return value</span></span>

<span data-ttu-id="35ce0-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="35ce0-127">S_OK</span></span> 
  
> <span data-ttu-id="35ce0-128">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="35ce0-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="35ce0-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="35ce0-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="35ce0-130">Se intentó obtener acceso a una sección de perfil para la que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="35ce0-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="35ce0-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="35ce0-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="35ce0-132">La sección de perfil solicitado no existe.</span><span class="sxs-lookup"><span data-stu-id="35ce0-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35ce0-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35ce0-133">Remarks</span></span>

<span data-ttu-id="35ce0-134">El **método IMsgServiceAdmin::OpenProfileSection** abre una sección de perfil, un objeto que admite la [interfaz IProfSect.](iprofsectimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="35ce0-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="35ce0-135">Las secciones de perfil se usan para leer información desde y escribir información en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="35ce0-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="35ce0-136">**OpenProfileSection** no se puede usar para abrir secciones de perfil propiedad de proveedores de servicios individuales a menos que MAPI_FORCE_ACCESS se use.</span><span class="sxs-lookup"><span data-stu-id="35ce0-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="35ce0-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="35ce0-137">Notes to callers</span></span>

<span data-ttu-id="35ce0-138">Varios clientes pueden abrir una sección de perfil con permiso de solo lectura, pero solo un cliente puede abrir una sección de perfil con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="35ce0-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="35ce0-139">Si otro cliente tiene abierta una sección de perfil que intenta abrir llamando a **OpenProfileSection** con la marca MAPI_MODIFY establecida, la llamada producirá un error, lo que devuelve MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="35ce0-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="35ce0-140">Si la sección está abierta para escritura, se produce un error en una operación abierta de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="35ce0-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="35ce0-141">Puede crear una sección de perfil llamando a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura [MAPIUID](mapiuid.md) inexistente en el _parámetro lpUID._</span><span class="sxs-lookup"><span data-stu-id="35ce0-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="35ce0-142">Asegúrese de especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="35ce0-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="35ce0-143">Si establece  _lpUID_ para que apunte a un **MAPIUID** inexistente y **OpenProfileSection** se establece para usar el modo de acceso predeterminado de solo lectura, la llamada producirá un error con MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="35ce0-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="35ce0-144">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="35ce0-144">MFCMAPI reference</span></span>

<span data-ttu-id="35ce0-145">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="35ce0-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="35ce0-146">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="35ce0-146">**File**</span></span>|<span data-ttu-id="35ce0-147">**Función**</span><span class="sxs-lookup"><span data-stu-id="35ce0-147">**Function**</span></span>|<span data-ttu-id="35ce0-148">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="35ce0-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35ce0-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="35ce0-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="35ce0-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="35ce0-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="35ce0-151">MFCMAPI usa el **método IMsgServiceAdmin::OpenProfileSection** para abrir una sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="35ce0-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35ce0-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ce0-152">See also</span></span>



[<span data-ttu-id="35ce0-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35ce0-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="35ce0-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="35ce0-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="35ce0-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="35ce0-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="35ce0-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="35ce0-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="35ce0-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35ce0-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="35ce0-158">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="35ce0-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

