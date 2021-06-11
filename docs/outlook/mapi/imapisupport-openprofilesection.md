---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411389"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="6c615-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="6c615-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="6c615-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c615-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c615-105">Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="6c615-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="6c615-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6c615-106">Parameters</span></span>

 <span data-ttu-id="6c615-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="6c615-107">_lpUid_</span></span>
  
> <span data-ttu-id="6c615-108">[in] Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="6c615-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="6c615-109">Si se pasa NULL para  _el parámetro lpUid,_ se abre la sección de perfil del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6c615-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="6c615-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c615-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6c615-111">[in] Máscara de bits de marcas que controla cómo se abre la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="6c615-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="6c615-112">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="6c615-112">The following flags can be set:</span></span>
    
<span data-ttu-id="6c615-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6c615-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6c615-114">Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil sea totalmente accesible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6c615-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="6c615-115">Si la sección de perfil no es accesible, realizar una llamada de objeto posterior puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="6c615-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="6c615-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6c615-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6c615-117">Solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6c615-117">Requests read/write permission.</span></span> <span data-ttu-id="6c615-118">De forma predeterminada, los objetos se abren como de solo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6c615-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="6c615-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="6c615-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="6c615-120">[salida] Puntero a un puntero a la sección de perfil abierto.</span><span class="sxs-lookup"><span data-stu-id="6c615-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c615-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c615-121">Return value</span></span>

<span data-ttu-id="6c615-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c615-122">S_OK</span></span> 
  
> <span data-ttu-id="6c615-123">La sección de perfil se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c615-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="6c615-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6c615-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6c615-125">Se intentó modificar una sección de perfil de solo lectura o obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="6c615-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="6c615-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6c615-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6c615-127">No hay una sección de perfil asociada con el identificador de entrada pasado en  _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="6c615-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="6c615-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6c615-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="6c615-129">Se usaron marcas reservadas o no admitidas y, por lo tanto, la operación no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="6c615-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c615-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c615-130">Remarks</span></span>

<span data-ttu-id="6c615-131">El **método IMAPISupport::OpenProfileSection** se implementa para todos los objetos de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="6c615-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="6c615-132">Los proveedores de servicios y servicios de mensajes llaman a **OpenProfileSection** para abrir una sección de perfil y recuperar un puntero a su implementación de interfaz **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="6c615-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c615-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6c615-133">Notes to callers</span></span>

 <span data-ttu-id="6c615-134">**OpenProfileSection** abre secciones de perfil como de solo lectura, a menos que establezca la marca MAPI_MODIFY en el  _parámetro ulFlags_ y su permiso sea suficiente.</span><span class="sxs-lookup"><span data-stu-id="6c615-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="6c615-135">Establecer esta marca no garantiza el permiso de lectura y escritura; los permisos que se le concedan dependen del nivel de acceso y del objeto.</span><span class="sxs-lookup"><span data-stu-id="6c615-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="6c615-136">Si **OpenProfileSection intenta** abrir una sección de perfil inexistente como de solo lectura, devuelve MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="6c615-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="6c615-137">Si **OpenProfileSection intenta** abrir una sección de perfil inexistente como lectura y escritura, crea la sección de perfil y devuelve el puntero **IProfSect.**</span><span class="sxs-lookup"><span data-stu-id="6c615-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c615-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c615-138">See also</span></span>



[<span data-ttu-id="6c615-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c615-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="6c615-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6c615-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="6c615-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6c615-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6c615-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c615-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

