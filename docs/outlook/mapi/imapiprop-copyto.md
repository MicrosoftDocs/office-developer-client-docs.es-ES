---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356395"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="34d81-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="34d81-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="34d81-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34d81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34d81-105">Copia o mueve todas las propiedades, excepto las propiedades excluidas específicamente.</span><span class="sxs-lookup"><span data-stu-id="34d81-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="34d81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34d81-106">Parameters</span></span>

 <span data-ttu-id="34d81-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="34d81-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="34d81-108">[entrada] Recuento de interfaces que se excluirán cuando se copien o se mueven las propiedades.</span><span class="sxs-lookup"><span data-stu-id="34d81-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="34d81-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="34d81-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="34d81-110">[entrada] Matriz de identificadores de interfaz (IID) que especifican interfaces que no deben usarse cuando se copia o mueve información complementaria al objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="34d81-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="34d81-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="34d81-112">[entrada] Puntero a una matriz de etiquetas de propiedades que identifica las etiquetas de propiedad que deben excluirse de la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="34d81-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="34d81-113">Pasar **null** en  _el parámetro lpExcludeProps_ indica que todas las propiedades del objeto deben copiarse o moverse.</span><span class="sxs-lookup"><span data-stu-id="34d81-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="34d81-114">**CopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropProblemArray](spropproblemarray.md) a la que apunta  _lpExcludeProps_ está establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="34d81-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="34d81-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="34d81-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="34d81-116">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="34d81-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="34d81-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="34d81-117">_lpProgress_</span></span>
  
> <span data-ttu-id="34d81-118">[entrada] Puntero a una implementación de indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="34d81-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="34d81-119">Si **se** pasa null en el  _parámetro lpProgress,_ MAPI proporciona la implementación del progreso.</span><span class="sxs-lookup"><span data-stu-id="34d81-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="34d81-120">El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="34d81-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="34d81-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="34d81-121">_lpInterface_</span></span>
  
> <span data-ttu-id="34d81-122">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto al que apunta el parámetro _lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="34d81-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="34d81-123">El _parámetro lpInterface_ no debe ser **nulo.**</span><span class="sxs-lookup"><span data-stu-id="34d81-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="34d81-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="34d81-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="34d81-125">[entrada] Puntero al objeto para recibir las propiedades copiadas o movida.</span><span class="sxs-lookup"><span data-stu-id="34d81-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="34d81-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34d81-126">_ulFlags_</span></span>
  
> <span data-ttu-id="34d81-127">[entrada] Máscara de bits de marcas que controla la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="34d81-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="34d81-128">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="34d81-128">The following flags can be set:</span></span>
    
<span data-ttu-id="34d81-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="34d81-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="34d81-130">Si **CopyTo** llama al método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) para controlar la operación de copia o movimiento, debería devolverse inmediatamente con el valor de error MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="34d81-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="34d81-131">MAPI MAPI_DECLINE_OK marca para limitar la recursión.</span><span class="sxs-lookup"><span data-stu-id="34d81-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="34d81-132">Los clientes no establecen esta marca.</span><span class="sxs-lookup"><span data-stu-id="34d81-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="34d81-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="34d81-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="34d81-134">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="34d81-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="34d81-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="34d81-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="34d81-136">**CopyTo** debe realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="34d81-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="34d81-137">Cuando no se establece esta marca, **CopyTo** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="34d81-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="34d81-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="34d81-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="34d81-139">Las propiedades existentes en el objeto de destino no deben sobrescribirse.</span><span class="sxs-lookup"><span data-stu-id="34d81-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="34d81-140">Cuando no se establece esta marca, **CopyTo** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="34d81-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="34d81-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="34d81-141">_lppProblems_</span></span>
  
> <span data-ttu-id="34d81-142">[entrada, salida] En la entrada, un puntero a un puntero a una **estructura SPropProblemArray;** de lo **contrario, null**, que indica que no es necesario obtener información de error.</span><span class="sxs-lookup"><span data-stu-id="34d81-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="34d81-143">Si  _lppProblems_ es un puntero válido en la entrada, **CopyTo** devuelve información detallada acerca de los errores al copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="34d81-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="34d81-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34d81-144">Return value</span></span>

<span data-ttu-id="34d81-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="34d81-145">S_OK</span></span> 
  
> <span data-ttu-id="34d81-146">Las propiedades se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="34d81-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="34d81-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="34d81-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="34d81-148">No se puede copiar un subobjeto porque ya existe un subobjeto con el mismo nombre para mostrar ( especificado por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="34d81-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="34d81-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="34d81-150">El proveedor de servicios no implementa la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="34d81-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="34d81-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="34d81-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="34d81-152">El objeto de origen que realiza la operación de copia o movimiento directa o indirectamente contiene el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="34d81-153">Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="34d81-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="34d81-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="34d81-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="34d81-155">La interfaz identificada por el  _parámetro lpInterface_ no es compatible con el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="34d81-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="34d81-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="34d81-157">Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="34d81-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="34d81-158">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="34d81-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="34d81-159">Los siguientes valores se pueden devolver en la **estructura SPropProblemArray,** pero no como valores devueltos **para CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="34d81-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="34d81-160">Los siguientes errores se aplican a una sola propiedad:</span><span class="sxs-lookup"><span data-stu-id="34d81-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="34d81-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="34d81-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="34d81-162">Se estableció MAPI_UNICODE marca y **CopyTo** no admite Unicode, o MAPI_UNICODE no se estableció y **CopyTo** solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="34d81-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="34d81-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="34d81-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="34d81-164">El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="34d81-165">Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="34d81-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="34d81-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="34d81-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="34d81-167">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="34d81-167">The property type is invalid.</span></span>
    
<span data-ttu-id="34d81-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="34d81-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="34d81-169">El tipo de propiedad no es el tipo esperado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="34d81-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34d81-170">Comentarios</span><span class="sxs-lookup"><span data-stu-id="34d81-170">Remarks</span></span>

<span data-ttu-id="34d81-171">De forma predeterminada, el **método IMAPIProp::CopyTo** copia o mueve todas las propiedades del objeto actual a un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="34d81-172">**CopyTo** se usa cuando un objeto debe copiarse o moverse exactamente, con todas o la mayoría de sus propiedades intactas.</span><span class="sxs-lookup"><span data-stu-id="34d81-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="34d81-173">Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o mueven en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="34d81-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="34d81-174">De forma predeterminada, **CopyTo** sobrescribe las propiedades del objeto de destino que coinciden con las propiedades del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="34d81-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="34d81-175">Si alguna de las propiedades copiadas o movida ya existe en el objeto de destino, las propiedades existentes se sobrescriben mediante las nuevas propiedades, a menos que la marca MAPI_NOREPLACE esté establecida en el parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="34d81-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="34d81-176">La información existente en el objeto de destino que no se sobrescribe se deja sin tocar.</span><span class="sxs-lookup"><span data-stu-id="34d81-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="34d81-177">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="34d81-177">Notes to implementers</span></span>

<span data-ttu-id="34d81-178">Puede proporcionar una implementación completa de **CopyTo** o confiar en la implementación que MAPI proporciona en su objeto de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="34d81-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="34d81-179">Si desea usar la implementación MAPI, llame a **IMAPISupport::D oCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="34d81-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="34d81-180">Sin embargo, si delega el procesamiento en **DoCopyTo** y se le pasa la marca MAPI_DECLINE_OK, evite la llamada de soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar.</span><span class="sxs-lookup"><span data-stu-id="34d81-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="34d81-181">MAPI llamará con esta marca para evitar la posible recursión que puede ocurrir cuando se copian carpetas.</span><span class="sxs-lookup"><span data-stu-id="34d81-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="34d81-182">Dado que la operación de copia puede ser larga, debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="34d81-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="34d81-183">Use la [implementación IMAPIProgress](imapiprogressiunknown.md) pasada en el parámetro  _lpProgress,_ si la hay.</span><span class="sxs-lookup"><span data-stu-id="34d81-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="34d81-184">Si  _lpProgress_ es **null,** llame al método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar la implementación mapi.</span><span class="sxs-lookup"><span data-stu-id="34d81-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="34d81-185">No intente establecer ninguna propiedad de solo lectura conocida en el objeto de destino; devolver MAPI_E_NO_ACCESS en su lugar.</span><span class="sxs-lookup"><span data-stu-id="34d81-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="34d81-186">Los objetos de origen y destino deben usar las mismas interfaces.</span><span class="sxs-lookup"><span data-stu-id="34d81-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="34d81-187">Devuelve MAPI_E_INVALID_PARAMETER si  _lpInterface_ no está establecido.</span><span class="sxs-lookup"><span data-stu-id="34d81-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="34d81-188">Devuelve MAPI_E_INTERFACE_NOT_SUPPORTED si se excluyen todas las interfaces conocidas.</span><span class="sxs-lookup"><span data-stu-id="34d81-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="34d81-189">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="34d81-189">Notes to callers</span></span>

<span data-ttu-id="34d81-190">No establezca la marca MAPI_DECLINE_OK; MAPI lo usa en sus llamadas a implementaciones **CopyTo** del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="34d81-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="34d81-191">Dado que las operaciones de copiar y mover pueden tardar tiempo, debe solicitar la visualización de un indicador de progreso estableciendo la MAPI_DIALOG de movimiento.</span><span class="sxs-lookup"><span data-stu-id="34d81-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="34d81-192">Puede establecer el parámetro  _lpProgress_ en la implementación de **IMAPIProgress**, si tiene uno, o en **null**.</span><span class="sxs-lookup"><span data-stu-id="34d81-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="34d81-193">Si  _lpProgress es_ **nulo,** **CopyTo** usará el indicador de progreso predeterminado que proporciona MAPI.</span><span class="sxs-lookup"><span data-stu-id="34d81-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="34d81-194">Puedes suprimir la presentación de un indicador de progreso si no estableces la MAPI_DIALOG indicador.</span><span class="sxs-lookup"><span data-stu-id="34d81-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="34d81-195">**CopyTo** omitirá  _los parámetros ulUIParam_ y  _lpProgress_ y no mostrará el indicador.</span><span class="sxs-lookup"><span data-stu-id="34d81-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="34d81-196">**CopyTo puede** notificar errores globales e individuales, o errores que se producen con una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="34d81-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="34d81-197">Estos errores individuales se colocan en una **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="34d81-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="34d81-198">Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de la matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="34d81-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="34d81-199">Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="34d81-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="34d81-200">Cuando **CopyTo** devuelve S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura.</span><span class="sxs-lookup"><span data-stu-id="34d81-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="34d81-201">Cuando **CopyTo** devuelve un error, no se devuelve información en la **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="34d81-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="34d81-202">En su lugar, [llame a IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error.</span><span class="sxs-lookup"><span data-stu-id="34d81-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="34d81-203">Si **CopyTo** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="34d81-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="34d81-204">Si copia las propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino sea del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="34d81-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="34d81-205">**CopyTo** no impide asociar propiedades que normalmente pertenecen a un tipo de objeto con otro tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="34d81-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="34d81-206">Es usted el que debe copiar las propiedades que tienen sentido para el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="34d81-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="34d81-207">Por ejemplo, no debe copiar las propiedades del mensaje en un contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="34d81-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="34d81-208">Para asegurarse de copiar entre objetos del mismo tipo, compruebe que el objeto de origen y de destino sean del mismo tipo, ya sea comparando punteros de objeto o llamando a [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="34d81-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="34d81-209">Establece el identificador de interfaz al que  _apunta lpInterface_ en la interfaz estándar para el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="34d81-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="34d81-210">Además, asegúrese de que el tipo de **objeto PR_OBJECT_TYPE** propiedad ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) sea la misma para los dos objetos.</span><span class="sxs-lookup"><span data-stu-id="34d81-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="34d81-211">Por ejemplo, si copia desde un mensaje, establezca _lpInterface_ en IID_IMessage y el PR_OBJECT_TYPE para ambos objetos en MAPI_MESSAGE. </span><span class="sxs-lookup"><span data-stu-id="34d81-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="34d81-212">Si se pasa un puntero no válido en el  _parámetro lpDestObj,_ los resultados son impredecibles.</span><span class="sxs-lookup"><span data-stu-id="34d81-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="34d81-213">Excluir las propiedades de **una llamada CopyTo** puede ser útil.</span><span class="sxs-lookup"><span data-stu-id="34d81-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="34d81-214">Por ejemplo, algunos objetos tienen propiedades específicas de una sola instancia del objeto, como la fecha y la hora de entrega del mensaje.</span><span class="sxs-lookup"><span data-stu-id="34d81-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="34d81-215">Para evitar copiar la hora de entrega de un mensaje al copiar el mensaje en otra carpeta, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la matriz de exclusión de etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="34d81-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="34d81-216">Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión.</span><span class="sxs-lookup"><span data-stu-id="34d81-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="34d81-217">Para excluir los datos adjuntos de un mensaje, agregue **la PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.</span><span class="sxs-lookup"><span data-stu-id="34d81-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="34d81-218">De forma similar, evita copiar o mover la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones incluyendo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="34d81-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="34d81-219">Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="34d81-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="34d81-220">Si pasa los resultados de la macro PROP_TAG para crear una etiqueta de propiedad **a** partir de un identificador específico en la matriz de etiquetas de propiedad, se excluirán todas las propiedades con ese identificador.</span><span class="sxs-lookup"><span data-stu-id="34d81-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="34d81-221">Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedades hace que todas las propiedades con un identificador de 0x8002 se excluyan, independientemente del tipo:</span><span class="sxs-lookup"><span data-stu-id="34d81-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="34d81-222">La **PR_NULL** de propiedad ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="34d81-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="34d81-223">La utilidad de la característica **CopyTo** para excluir interfaces quizás no sea tan obvia como la utilidad de excluir propiedades.</span><span class="sxs-lookup"><span data-stu-id="34d81-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="34d81-224">Puede excluir una interfaz al copiar a un objeto que no tiene conocimiento de un grupo de propiedades.</span><span class="sxs-lookup"><span data-stu-id="34d81-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="34d81-225">Por ejemplo, si copia propiedades de una carpeta a datos adjuntos, las únicas propiedades con las que pueden trabajar los datos adjuntos son las propiedades genéricas disponibles con cualquier [implementación imapiprop.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="34d81-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="34d81-226">Al excluir [IMAPIFolder de](imapifolderimapicontainer.md) la operación de copia, los datos adjuntos no recibirán ninguna de las propiedades de carpeta más específicas.</span><span class="sxs-lookup"><span data-stu-id="34d81-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="34d81-227">Cuando se usa el  _parámetro rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="34d81-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="34d81-228">Por ejemplo, la exclusión de [IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan carpetas o contenedores de libreta de direcciones, según el tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="34d81-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="34d81-229">No excluya **IMAPIProp** o [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) porque muchas interfaces derivan de ellas.</span><span class="sxs-lookup"><span data-stu-id="34d81-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="34d81-230">Omitir MAPI_E_COMPUTED errores devueltos en la **estructura SPropProblemArray** en el parámetro _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="34d81-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="34d81-231">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="34d81-231">MFCMAPI reference</span></span>

<span data-ttu-id="34d81-232">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="34d81-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="34d81-233">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="34d81-233">**File**</span></span>|<span data-ttu-id="34d81-234">**Función**</span><span class="sxs-lookup"><span data-stu-id="34d81-234">**Function**</span></span>|<span data-ttu-id="34d81-235">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="34d81-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34d81-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="34d81-236">File.cpp</span></span>  <br/> |<span data-ttu-id="34d81-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="34d81-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="34d81-238">MFCMAPI usa el **método IMAPIProp::CopyTo** para copiar propiedades de un archivo .msg a un [objeto IMAPIMessageSite.](imapimessagesiteiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="34d81-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="34d81-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="34d81-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="34d81-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="34d81-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="34d81-241">MFCMAPI usa el **método IMAPIProp::CopyTo** para copiar propiedades de un mensaje de origen a un mensaje de destino durante una operación de pegado.</span><span class="sxs-lookup"><span data-stu-id="34d81-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34d81-242">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34d81-242">See also</span></span>



[<span data-ttu-id="34d81-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="34d81-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="34d81-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="34d81-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="34d81-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34d81-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="34d81-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34d81-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="34d81-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="34d81-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="34d81-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="34d81-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="34d81-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="34d81-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="34d81-250">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="34d81-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="34d81-251">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="34d81-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="34d81-252">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="34d81-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="34d81-253">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="34d81-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="34d81-254">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="34d81-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="34d81-255">Propiedad canónica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="34d81-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="34d81-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="34d81-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="34d81-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="34d81-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="34d81-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34d81-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="34d81-259">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="34d81-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

