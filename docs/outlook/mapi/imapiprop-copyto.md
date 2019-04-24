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
# <a name="imapipropcopyto"></a><span data-ttu-id="69d9c-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="69d9c-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="69d9c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69d9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69d9c-105">Copia o mueve todas las propiedades, excepto las propiedades excluidas específicamente.</span><span class="sxs-lookup"><span data-stu-id="69d9c-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="69d9c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="69d9c-106">Parameters</span></span>

 <span data-ttu-id="69d9c-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="69d9c-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="69d9c-108">a Número de interfaces que se van a excluir al copiar o mover las propiedades.</span><span class="sxs-lookup"><span data-stu-id="69d9c-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="69d9c-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="69d9c-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="69d9c-110">a Matriz de identificadores de interfaz (IID) que especifican interfaces que no se deben usar cuando se copia o se mueve información complementaria al objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="69d9c-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="69d9c-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="69d9c-112">a Un puntero a una matriz de etiquetas de propiedad que identifica las etiquetas de propiedad que se deben excluir de la operación de copia o movimiento.</span><span class="sxs-lookup"><span data-stu-id="69d9c-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="69d9c-113">Pasar **null** en el parámetro _lpExcludeProps_ indica que todas las propiedades del objeto se deben copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="69d9c-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="69d9c-114">**CopyTo** devuelve MAPI_E_INVALID_PARAMETER cuando el miembro **cValues** de la estructura [SPropProblemArray](spropproblemarray.md) a la que apunta _lpExcludeProps_ se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="69d9c-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="69d9c-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="69d9c-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="69d9c-116">a Identificador de la ventana primaria del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="69d9c-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="69d9c-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="69d9c-117">_lpProgress_</span></span>
  
> <span data-ttu-id="69d9c-118">a Un puntero a una implementación del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="69d9c-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="69d9c-119">Si se pasa **null** en el parámetro _lpProgress_ , MAPI proporciona la implementación del progreso.</span><span class="sxs-lookup"><span data-stu-id="69d9c-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="69d9c-120">El parámetro _lpProgress_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="69d9c-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="69d9c-121">_lpInterface_</span></span>
  
> <span data-ttu-id="69d9c-122">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al objeto al que apunta el parámetro _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="69d9c-123">El parámetro _lpInterface_ no debe ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="69d9c-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="69d9c-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="69d9c-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="69d9c-125">a Un puntero al objeto que va a recibir las propiedades que se han copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="69d9c-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="69d9c-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69d9c-126">_ulFlags_</span></span>
  
> <span data-ttu-id="69d9c-127">a Una máscara de máscara de marcadores que controla la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="69d9c-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="69d9c-128">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="69d9c-128">The following flags can be set:</span></span>
    
<span data-ttu-id="69d9c-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="69d9c-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="69d9c-130">Si **CopyTo** llama al método [IMAPISupport::D ocopyto](imapisupport-docopyto.md) para controlar la operación de copia o movimiento, en su lugar debe volver inmediatamente con el valor de error MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="69d9c-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="69d9c-131">MAPI establece la marca MAPI_DECLINE_OK para limitar la recursividad.</span><span class="sxs-lookup"><span data-stu-id="69d9c-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="69d9c-132">Los clientes no establecen esta marca.</span><span class="sxs-lookup"><span data-stu-id="69d9c-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="69d9c-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="69d9c-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="69d9c-134">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="69d9c-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="69d9c-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="69d9c-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="69d9c-136">**CopyTo** debe realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="69d9c-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="69d9c-137">Si no se establece esta marca, **CopyTo** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="69d9c-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="69d9c-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="69d9c-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="69d9c-139">Las propiedades existentes en el objeto de destino no se deben sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="69d9c-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="69d9c-140">Si no se establece este indicador, **CopyTo** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="69d9c-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="69d9c-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="69d9c-141">_lppProblems_</span></span>
  
> <span data-ttu-id="69d9c-142">[in, out] En la entrada, un puntero a un puntero a una estructura **SPropProblemArray** ; de lo contrario, **null**, que indica que no es necesaria información de error.</span><span class="sxs-lookup"><span data-stu-id="69d9c-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="69d9c-143">Si _lppProblems_ es un puntero válido en la entrada \*\*\*\* , CopyTo devuelve información detallada sobre los errores al copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="69d9c-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69d9c-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69d9c-144">Return value</span></span>

<span data-ttu-id="69d9c-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="69d9c-145">S_OK</span></span> 
  
> <span data-ttu-id="69d9c-146">Las propiedades se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="69d9c-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="69d9c-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="69d9c-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="69d9c-148">No se puede copiar un subobjeto porque ya existe un subobjeto con el mismo nombre para mostrar, especificado por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="69d9c-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="69d9c-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="69d9c-150">El proveedor de servicios no implementa la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="69d9c-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="69d9c-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="69d9c-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="69d9c-152">El objeto de origen que realiza la operación de copia o movimiento contiene directa o indirectamente el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="69d9c-153">Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="69d9c-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="69d9c-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="69d9c-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="69d9c-155">La interfaz identificada por el parámetro _lpInterface_ no es compatible con el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="69d9c-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="69d9c-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="69d9c-157">Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="69d9c-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="69d9c-158">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="69d9c-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="69d9c-159">Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="69d9c-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="69d9c-160">Los errores siguientes se aplican a una sola propiedad:</span><span class="sxs-lookup"><span data-stu-id="69d9c-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="69d9c-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="69d9c-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="69d9c-162">Se ha establecido la marca MAPI_UNICODE y **CopyTo** no admite Unicode, o bien no se ha establecido MAPI_UNICODE \*\*\*\* y CopyTo solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="69d9c-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="69d9c-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="69d9c-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="69d9c-164">La propiedad no la puede modificar el autor de la llamada porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="69d9c-165">Este error no es grave; el autor de la llamada debe permitir que continúe la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="69d9c-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="69d9c-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="69d9c-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="69d9c-167">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="69d9c-167">The property type is invalid.</span></span>
    
<span data-ttu-id="69d9c-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="69d9c-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="69d9c-169">El tipo de propiedad no es el tipo que espera el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="69d9c-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69d9c-170">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69d9c-170">Remarks</span></span>

<span data-ttu-id="69d9c-171">De forma predeterminada, el método **IMAPIProp:: CopyTo** copia o mueve todas las propiedades del objeto actual a un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="69d9c-172">**CopyTo** se usa cuando un objeto se debe copiar o mover exactamente, con todas o casi todas sus propiedades intactas.</span><span class="sxs-lookup"><span data-stu-id="69d9c-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="69d9c-173">Todos los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o se mueven en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="69d9c-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="69d9c-174">De forma predeterminada \*\*\*\* , CopyTo sobrescribe las propiedades del objeto de destino que coinciden con las propiedades del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="69d9c-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="69d9c-175">Si alguna de las propiedades que se han copiado o movido ya existe en el objeto de destino, las propiedades existentes se sobrescriben con las nuevas propiedades, a menos que la marca MAPI_NOREPLACE se establezca en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="69d9c-176">La información existente en el objeto de destino que no se sobrescribe permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="69d9c-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="69d9c-177">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="69d9c-177">Notes to implementers</span></span>

<span data-ttu-id="69d9c-178">Puede proporcionar una implementación completa de **CopyTo** o confiar en la implementación que proporciona MAPI en su objeto de soporte.</span><span class="sxs-lookup"><span data-stu-id="69d9c-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="69d9c-179">Si desea usar la implementación de MAPI, llame a **IMAPISupport::D ocopyto**.</span><span class="sxs-lookup"><span data-stu-id="69d9c-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="69d9c-180">Sin embargo, si realiza el procesamiento delegado \*\*\*\* en encopyto y se le pasa la marca MAPI_DECLINE_OK, evite la llamada al soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar.</span><span class="sxs-lookup"><span data-stu-id="69d9c-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="69d9c-181">MAPI llamará con esta marca para evitar la posible recursividad que puede ocurrir cuando se copian carpetas.</span><span class="sxs-lookup"><span data-stu-id="69d9c-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="69d9c-182">Como la operación de copia puede ser prolongada, debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="69d9c-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="69d9c-183">Use la implementación de [método imapiprogress](imapiprogressiunknown.md) que se ha pasado en el parámetro _lpProgress_ , si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="69d9c-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="69d9c-184">Si _lpProgress_ es **null**, llame al método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para usar la implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="69d9c-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="69d9c-185">No intente establecer ninguna de las propiedades de solo lectura conocidas en el objeto de destino; Devuelve MAPI_E_NO_ACCESS en su lugar.</span><span class="sxs-lookup"><span data-stu-id="69d9c-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="69d9c-186">Los objetos de origen y de destino deben usar las mismas interfaces.</span><span class="sxs-lookup"><span data-stu-id="69d9c-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="69d9c-187">Devuelve MAPI_E_INVALID_PARAMETER si no se establece _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="69d9c-188">Devuelve MAPI_E_INTERFACE_NOT_SUPPORTED si se excluyen todas las interfaces conocidas.</span><span class="sxs-lookup"><span data-stu-id="69d9c-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="69d9c-189">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="69d9c-189">Notes to callers</span></span>

<span data-ttu-id="69d9c-190">No establezca la marca MAPI_DECLINE_OK; MAPI la usa en sus llamadas a implementaciones **CopyTo** del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="69d9c-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="69d9c-191">Como las operaciones de copiar y mover pueden tardar algún tiempo, debe solicitar la presentación de un indicador de progreso estableciendo la marca MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="69d9c-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="69d9c-192">Puede establecer el parámetro _lpProgress_ en su implementación de **método imapiprogress**, si tiene uno, o en **null**.</span><span class="sxs-lookup"><span data-stu-id="69d9c-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="69d9c-193">Si _lpProgress_ es **null**, **CopyTo** usará el indicador de progreso predeterminado que proporciona MAPI.</span><span class="sxs-lookup"><span data-stu-id="69d9c-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="69d9c-194">Puede suprimir la presentación de un indicador de progreso si no se configura la marca MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="69d9c-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="69d9c-195">**CopyTo** omitirá los parámetros _ulUIParam_ y _lpProgress_ , y no mostrará el indicador.</span><span class="sxs-lookup"><span data-stu-id="69d9c-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="69d9c-196">**CopyTo** puede informar de errores globales y individuales, o errores que se producen con una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="69d9c-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="69d9c-197">Estos errores individuales se colocan en una estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="69d9c-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="69d9c-198">Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de matriz con problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="69d9c-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="69d9c-199">Si desea recibir información sobre los errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="69d9c-200">Cuando **CopyTo** Devuelve S_OK, compruebe si hay posibles errores con propiedades individuales en la estructura.</span><span class="sxs-lookup"><span data-stu-id="69d9c-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="69d9c-201">Cuando **CopyTo** devuelve un error, no se devuelve información en la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="69d9c-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="69d9c-202">En su lugar, llame a [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) para recuperar información detallada del error.</span><span class="sxs-lookup"><span data-stu-id="69d9c-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="69d9c-203">Si **CopyTo** Devuelve S_OK, libere la estructura **SPropProblemArray** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="69d9c-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="69d9c-204">Si copia propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="69d9c-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="69d9c-205">**CopyTo** no impide que se asocien propiedades que, por lo general, pertenecen a un tipo de objeto con otro tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="69d9c-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="69d9c-206">El usuario debe copiar las propiedades que tengan sentido para el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="69d9c-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="69d9c-207">Por ejemplo, no debe copiar las propiedades de los mensajes en un contenedor de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="69d9c-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="69d9c-208">Para asegurarse de que copia entre objetos del mismo tipo, compruebe que el objeto de origen y el de destino son el mismo tipo, ya sea comparando los punteros de objeto o llamando a [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="69d9c-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="69d9c-209">Establezca el identificador de interfaz al que apunta _lpInterface_ en la interfaz estándar del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="69d9c-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="69d9c-210">Además, asegúrese de que la propiedad tipo de objeto o **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) es la misma para los dos objetos.</span><span class="sxs-lookup"><span data-stu-id="69d9c-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="69d9c-211">Por ejemplo, si copia de un mensaje, establezca _lpInterface_ en IID_IMessage y el **PR_OBJECT_TYPE** para ambos objetos en MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="69d9c-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="69d9c-212">Si se pasa un puntero no válido en el parámetro _lpDestObj_ , los resultados son imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="69d9c-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="69d9c-213">La exclusión de propiedades \*\*\*\* en una llamada a CopyTo puede ser útil.</span><span class="sxs-lookup"><span data-stu-id="69d9c-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="69d9c-214">Por ejemplo, algunos objetos tienen propiedades que son específicas de una única instancia del objeto, como la fecha y la hora de la entrega del mensaje.</span><span class="sxs-lookup"><span data-stu-id="69d9c-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="69d9c-215">Para evitar copiar el tiempo de entrega de un mensaje cuando copia el mensaje en una carpeta diferente, especifique **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) en la etiqueta de exclusión de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="69d9c-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="69d9c-216">Para excluir la lista de destinatarios de un mensaje, agregue la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) a la matriz de exclusión.</span><span class="sxs-lookup"><span data-stu-id="69d9c-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="69d9c-217">Para excluir los datos adjuntos de un mensaje, agregue la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) a la matriz.</span><span class="sxs-lookup"><span data-stu-id="69d9c-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="69d9c-218">De forma similar, evite copiar o mover una carpeta o una jerarquía de contenedor de libreta de direcciones o de contenido incluyendo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de exclusión de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="69d9c-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="69d9c-219">Para excluir propiedades de la operación de copiar o mover, incluya sus etiquetas de propiedad en el parámetro _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="69d9c-220">Si pasa los resultados de la macro **PROP_TAG** para crear una etiqueta de propiedad a partir de un identificador específico de la matriz de etiquetas de propiedades, se excluirán todas las propiedades con ese identificador.</span><span class="sxs-lookup"><span data-stu-id="69d9c-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="69d9c-221">Por ejemplo, la siguiente entrada en la matriz de etiquetas de propiedad hace que se excluyan todas las propiedades con un identificador de 0x8002, independientemente del tipo:</span><span class="sxs-lookup"><span data-stu-id="69d9c-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="69d9c-222">La etiqueta de propiedad **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz de _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="69d9c-223">La utilidad de la característica **CopyTo** para excluir interfaces quizá no es tan evidente como la utilidad de excluir las propiedades.</span><span class="sxs-lookup"><span data-stu-id="69d9c-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="69d9c-224">Puede excluir una interfaz al copiar a un objeto que no tenga ningún conocimiento de un grupo de propiedades.</span><span class="sxs-lookup"><span data-stu-id="69d9c-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="69d9c-225">Por ejemplo, si se copian propiedades de una carpeta a datos adjuntos, las únicas propiedades con las que se pueden trabajar los datos adjuntos son las propiedades genéricas disponibles con cualquier implementación de [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="69d9c-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="69d9c-226">Si se excluye [IMAPIFolder](imapifolderimapicontainer.md) de la operación de copia, los datos adjuntos no recibirán ninguna de las propiedades de carpeta más específicas.</span><span class="sxs-lookup"><span data-stu-id="69d9c-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="69d9c-227">Cuando se usa el parámetro _rgiidExclude_ para excluir una interfaz, también se excluyen todas las interfaces derivadas de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="69d9c-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="69d9c-228">Por ejemplo, excluir [IMAPIContainer](imapicontainerimapiprop.md) hace que se excluyan las carpetas o los contenedores de la libreta de direcciones, según el tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="69d9c-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="69d9c-229">No excluya **IMAPIProp** o [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) porque hay tantas interfaces que se derivan de ellos.</span><span class="sxs-lookup"><span data-stu-id="69d9c-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="69d9c-230">Omite los errores de MAPI_E_COMPUTED devueltos en la estructura **SPropProblemArray** en el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="69d9c-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="69d9c-231">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69d9c-231">MFCMAPI reference</span></span>

<span data-ttu-id="69d9c-232">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="69d9c-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69d9c-233">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="69d9c-233">**File**</span></span>|<span data-ttu-id="69d9c-234">**Función**</span><span class="sxs-lookup"><span data-stu-id="69d9c-234">**Function**</span></span>|<span data-ttu-id="69d9c-235">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="69d9c-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69d9c-236">Archivo. cpp</span><span class="sxs-lookup"><span data-stu-id="69d9c-236">File.cpp</span></span>  <br/> |<span data-ttu-id="69d9c-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="69d9c-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="69d9c-238">MFCMAPI usa el método **IMAPIProp:: CopyTo** para copiar las propiedades de un archivo. msg a un objeto [IMAPIMessageSite](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="69d9c-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="69d9c-239">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="69d9c-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="69d9c-240">CFolderDlg:: HandlePaste</span><span class="sxs-lookup"><span data-stu-id="69d9c-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="69d9c-241">MFCMAPI usa el método **IMAPIProp:: CopyTo** para copiar las propiedades de un mensaje de origen en un mensaje de destino durante una operación de pegado.</span><span class="sxs-lookup"><span data-stu-id="69d9c-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69d9c-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="69d9c-242">See also</span></span>



[<span data-ttu-id="69d9c-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="69d9c-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="69d9c-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="69d9c-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="69d9c-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69d9c-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="69d9c-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69d9c-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="69d9c-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="69d9c-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="69d9c-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="69d9c-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="69d9c-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="69d9c-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="69d9c-250">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="69d9c-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="69d9c-251">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="69d9c-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="69d9c-252">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="69d9c-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="69d9c-253">Propiedad canónica PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="69d9c-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="69d9c-254">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="69d9c-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="69d9c-255">Propiedad canónica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="69d9c-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="69d9c-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="69d9c-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="69d9c-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="69d9c-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="69d9c-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69d9c-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="69d9c-259">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="69d9c-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

