---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345510"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="24c4c-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="24c4c-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="24c4c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24c4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24c4c-105">Copia o mueve las propiedades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="24c4c-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="24c4c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="24c4c-106">Parameters</span></span>

 <span data-ttu-id="24c4c-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="24c4c-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="24c4c-108">[in] Puntero a una matriz de etiquetas de propiedades que especifica las propiedades que se copian o se mueven.</span><span class="sxs-lookup"><span data-stu-id="24c4c-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="24c4c-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no se puede incluir en la matriz.</span><span class="sxs-lookup"><span data-stu-id="24c4c-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="24c4c-110">El  _parámetro lpIncludeProps_ no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="24c4c-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="24c4c-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="24c4c-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="24c4c-112">[in] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="24c4c-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="24c4c-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="24c4c-113">_lpProgress_</span></span>
  
> <span data-ttu-id="24c4c-114">[in] Puntero a una implementación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="24c4c-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="24c4c-115">Si se pasa **null** en el  _parámetro lpProgress,_ el indicador de progreso se muestra mediante la implementación MAPI.</span><span class="sxs-lookup"><span data-stu-id="24c4c-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="24c4c-116">El _parámetro lpProgress_ se omite a menos que MAPI_DIALOG marca se establezca en _el parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="24c4c-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="24c4c-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="24c4c-117">_lpInterface_</span></span>
  
> <span data-ttu-id="24c4c-118">[in] Puntero al identificador de interfaz (IID) que representa la interfaz que debe usarse para tener acceso al objeto al que apunta el _parámetro lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="24c4c-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="24c4c-119">El  _parámetro lpInterface_ no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="24c4c-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="24c4c-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="24c4c-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="24c4c-121">[in] Puntero al objeto para recibir las propiedades copiadas o movida.</span><span class="sxs-lookup"><span data-stu-id="24c4c-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="24c4c-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24c4c-122">_ulFlags_</span></span>
  
> <span data-ttu-id="24c4c-123">[in] Máscara de bits de marcas que controla la operación de copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="24c4c-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="24c4c-124">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="24c4c-124">The following flags can be set:</span></span>
    
<span data-ttu-id="24c4c-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="24c4c-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="24c4c-126">Si **CopyProps llama** al método [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) para controlar la operación de copia o movimiento, debería devolverse inmediatamente con el valor de error MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="24c4c-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="24c4c-127">MAPI MAPI_DECLINE_OK marca de inicio de sesión para limitar la recursividad.</span><span class="sxs-lookup"><span data-stu-id="24c4c-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="24c4c-128">Los clientes no establecen esta marca.</span><span class="sxs-lookup"><span data-stu-id="24c4c-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="24c4c-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="24c4c-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="24c4c-130">Muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="24c4c-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="24c4c-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="24c4c-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="24c4c-132">**CopyProps debe** realizar una operación de movimiento en lugar de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="24c4c-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="24c4c-133">Cuando no se establece esta marca, **CopyProps** realiza una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="24c4c-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="24c4c-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="24c4c-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="24c4c-135">Las propiedades existentes en el objeto de destino no deben sobrescribirse.</span><span class="sxs-lookup"><span data-stu-id="24c4c-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="24c4c-136">Cuando no se establece esta marca, **CopyProps** sobrescribe las propiedades existentes.</span><span class="sxs-lookup"><span data-stu-id="24c4c-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="24c4c-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="24c4c-137">_lppProblems_</span></span>
  
> <span data-ttu-id="24c4c-138">[in, out] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo **contrario, null**, que indica que no es necesario obtener información de error.</span><span class="sxs-lookup"><span data-stu-id="24c4c-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="24c4c-139">Si  _lppProblems_ es un puntero válido en la entrada, **CopyProps** devuelve información detallada acerca de los errores al copiar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="24c4c-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24c4c-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24c4c-140">Return value</span></span>

<span data-ttu-id="24c4c-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="24c4c-141">S_OK</span></span> 
  
> <span data-ttu-id="24c4c-142">Las propiedades se han copiado o movido correctamente.</span><span class="sxs-lookup"><span data-stu-id="24c4c-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="24c4c-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="24c4c-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="24c4c-144">Un subobjeto no se puede copiar porque un subobjeto con el mismo nombre para mostrar, definido por la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), ya existe en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="24c4c-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="24c4c-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="24c4c-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="24c4c-146">El proveedor de servicios no implementa la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="24c4c-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="24c4c-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="24c4c-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="24c4c-148">El objeto de origen que realiza la operación de copiar o mover directa o indirectamente contiene el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="24c4c-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="24c4c-149">Es posible que se haya realizado un trabajo significativo antes de que se detectara esta condición, por lo que los objetos de origen y de destino podrían modificarse parcialmente.</span><span class="sxs-lookup"><span data-stu-id="24c4c-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="24c4c-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="24c4c-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="24c4c-151">La interfaz identificada por el  _parámetro lpInterface_ no es compatible con el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="24c4c-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="24c4c-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="24c4c-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="24c4c-153">Se intentó obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="24c4c-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="24c4c-154">Este error se devuelve si el objeto de destino es el mismo que el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="24c4c-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="24c4c-155">Los siguientes valores se pueden devolver en la estructura **SPropProblemArray,** pero no como valores **devueltos para CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="24c4c-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="24c4c-156">Estos errores se aplican a una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="24c4c-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="24c4c-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="24c4c-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="24c4c-158">La marca MAPI_UNICODE se estableció y **CopyProps** no admite Unicode o MAPI_UNICODE no se estableció **y CopyProps** solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="24c4c-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="24c4c-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="24c4c-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="24c4c-160">El autor de la llamada no puede modificar la propiedad porque es una propiedad de solo lectura, calculada por el propietario del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="24c4c-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="24c4c-161">Este error no es grave; el autor de la llamada debe permitir que la operación de copia continúe.</span><span class="sxs-lookup"><span data-stu-id="24c4c-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="24c4c-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="24c4c-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="24c4c-163">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="24c4c-163">The property type is invalid.</span></span>
    
<span data-ttu-id="24c4c-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="24c4c-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="24c4c-165">El tipo de propiedad no es el tipo esperado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="24c4c-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24c4c-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24c4c-166">Remarks</span></span>

<span data-ttu-id="24c4c-167">El **método IMAPIProp::CopyProps** copia o mueve las propiedades seleccionadas del objeto actual a un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="24c4c-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="24c4c-168">**CopyProps** se usa principalmente para responder y reenviar mensajes, donde solo algunas de las propiedades del mensaje original viajan con la respuesta o la copia reenviada.</span><span class="sxs-lookup"><span data-stu-id="24c4c-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="24c4c-169">Los subobjetos del objeto de origen se incluyen automáticamente en la operación y se copian o se mueven en su totalidad, independientemente del uso de las propiedades indicadas por la estructura [SPropTagArray.](sproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="24c4c-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="24c4c-170">De forma predeterminada, **CopyProps sobrescribe** las propiedades del objeto de destino que coincidan con las propiedades del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="24c4c-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="24c4c-171">Si alguna de las propiedades copiadas o movida ya existen en el objeto de destino, las propiedades existentes se sobrescriben mediante las nuevas propiedades, a menos que la marca MAPI_NOREPLACE esté establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="24c4c-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="24c4c-172">La información existente en el objeto de destino que no se sobrescribe se deja intacta.</span><span class="sxs-lookup"><span data-stu-id="24c4c-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="24c4c-173">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="24c4c-173">Notes to implementers</span></span>

<span data-ttu-id="24c4c-174">Puede proporcionar una implementación completa de **CopyProps** o confiar en la implementación que MAPI proporciona en su objeto de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="24c4c-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="24c4c-175">Si desea usar la implementación MAPI, llame al método **IMAPISupport::D oCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="24c4c-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="24c4c-176">Sin embargo, si delega el procesamiento en **DoCopyProps** y se le pasa la marca MAPI_DECLINE_OK, evite la llamada de soporte técnico y devuelva MAPI_E_DECLINE_COPY en su lugar.</span><span class="sxs-lookup"><span data-stu-id="24c4c-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="24c4c-177">MAPI le llamará con esta marca para evitar la posible recursión que puede producirse al copiar carpetas.</span><span class="sxs-lookup"><span data-stu-id="24c4c-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="24c4c-178">Dado que la operación de copia puede ser larga, debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="24c4c-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="24c4c-179">Use la [implementación IMAPIProgress](imapiprogressiunknown.md) que se pasa en el parámetro  _lpProgress,_ si la hay.</span><span class="sxs-lookup"><span data-stu-id="24c4c-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="24c4c-180">Si  _lpProgress_ es **null,** llame al método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar la implementación MAPI.</span><span class="sxs-lookup"><span data-stu-id="24c4c-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="24c4c-181">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="24c4c-181">Notes to callers</span></span>

<span data-ttu-id="24c4c-182">No establezca la marca MAPI_DECLINE_OK; MAPI lo usa en sus llamadas a implementaciones **copyProps** del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="24c4c-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="24c4c-183">Dado que las operaciones de copiar y mover pueden tardar tiempo, es aconsejable solicitar la presentación de un indicador de progreso estableciendo la marca MAPI_DIALOG movimiento.</span><span class="sxs-lookup"><span data-stu-id="24c4c-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="24c4c-184">Puede establecer el parámetro  _lpProgress_ en la implementación de **IMAPIProgress**, si tiene uno, o en **null**.</span><span class="sxs-lookup"><span data-stu-id="24c4c-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="24c4c-185">Si  _lpProgress_ es **null,** **CopyProps** usará el indicador de progreso predeterminado proporcionado por MAPI.</span><span class="sxs-lookup"><span data-stu-id="24c4c-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="24c4c-186">Puede suprimir la presentación de un indicador de progreso no estableciendo la MAPI_DIALOG indicador.</span><span class="sxs-lookup"><span data-stu-id="24c4c-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="24c4c-187">**CopyProps omitirá** los parámetros  _ulUIParam_ y  _lpProgress_ y evitará mostrar el indicador.</span><span class="sxs-lookup"><span data-stu-id="24c4c-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="24c4c-188">**CopyProps puede** notificar errores globales e individuales, o errores que se producen con una o varias de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="24c4c-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="24c4c-189">Estos errores individuales se ponen en una **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="24c4c-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="24c4c-190">Puede suprimir los informes de errores en el nivel de propiedad pasando **null**, en lugar de un puntero válido, para el parámetro de estructura de matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="24c4c-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="24c4c-191">Si desea recibir información sobre errores, pase un puntero de estructura **SPropProblemArray** válido en el parámetro _lppProblems._</span><span class="sxs-lookup"><span data-stu-id="24c4c-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="24c4c-192">Cuando **CopyProps** devuelve S_OK, compruebe si hay errores posibles con propiedades individuales en la estructura.</span><span class="sxs-lookup"><span data-stu-id="24c4c-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="24c4c-193">Cuando **CopyProps** devuelve un error, no se devuelve información en la estructura **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="24c4c-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="24c4c-194">En su lugar, llama [al método IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar información de error detallada.</span><span class="sxs-lookup"><span data-stu-id="24c4c-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="24c4c-195">Si **CopyProps** devuelve S_OK, libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="24c4c-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="24c4c-196">Si va a copiar propiedades que son exclusivas del tipo de objeto de origen, debe asegurarse de que el objeto de destino es del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="24c4c-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="24c4c-197">**CopyProps** no impide asociar propiedades que normalmente pertenecen a un tipo de objeto con otro tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="24c4c-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="24c4c-198">Es su función copiar las propiedades que tienen sentido para el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="24c4c-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="24c4c-199">Por ejemplo, no debe copiar las propiedades del mensaje en un contenedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="24c4c-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="24c4c-200">Para asegurarse de que está copiando entre objetos del mismo tipo, compruebe que el objeto de origen y de destino sean del mismo tipo, ya sea comparando punteros de objeto o llamando al método [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24c4c-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="24c4c-201">Establezca el identificador de interfaz señalado por  _lpInterface_ en la interfaz estándar del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="24c4c-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="24c4c-202">Además, asegúrese de que el tipo de **objeto o PR_OBJECT_TYPE** propiedad ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) sea la misma para los dos objetos.</span><span class="sxs-lookup"><span data-stu-id="24c4c-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="24c4c-203">Por ejemplo, si va a copiar desde un mensaje, establezca  _lpInterface_ en IID_IMessage y la PR_OBJECT_TYPE para ambos objetos en MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="24c4c-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="24c4c-204">Si se pasa un puntero no válido en el  _parámetro lpDestObj,_ los resultados son impredecibles.</span><span class="sxs-lookup"><span data-stu-id="24c4c-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="24c4c-205">Para copiar la lista de destinatarios de un mensaje, llame al método **CopyProps** del mensaje e incluya la propiedad **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en la matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="24c4c-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="24c4c-206">Para copiar los datos adjuntos del mensaje, incluya **la propiedad PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="24c4c-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="24c4c-207">Para copiar la jerarquía o la tabla de contenido de un contenedor de carpeta o libreta de direcciones, incluya las propiedades **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) o **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) en la matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="24c4c-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="24c4c-208">Para incluir la tabla de contenido asociada de una carpeta, incluya la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en la matriz.</span><span class="sxs-lookup"><span data-stu-id="24c4c-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24c4c-209">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="24c4c-209">MFCMAPI reference</span></span>

<span data-ttu-id="24c4c-210">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="24c4c-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24c4c-211">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="24c4c-211">**File**</span></span>|<span data-ttu-id="24c4c-212">**Función**</span><span class="sxs-lookup"><span data-stu-id="24c4c-212">**Function**</span></span>|<span data-ttu-id="24c4c-213">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="24c4c-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24c4c-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="24c4c-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="24c4c-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="24c4c-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="24c4c-216">MFCMAPI usa el **método IMAPIProp::CopyProps** para copiar propiedades con nombre de un mensaje a otro.</span><span class="sxs-lookup"><span data-stu-id="24c4c-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="24c4c-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="24c4c-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="24c4c-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="24c4c-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="24c4c-219">MFCMAPI usa el **método IMAPIProp::CopyProps** para pegar una propiedad que se ha copiado de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="24c4c-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24c4c-220">Vea también</span><span class="sxs-lookup"><span data-stu-id="24c4c-220">See also</span></span>



[<span data-ttu-id="24c4c-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="24c4c-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="24c4c-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24c4c-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="24c4c-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="24c4c-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="24c4c-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="24c4c-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="24c4c-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="24c4c-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="24c4c-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="24c4c-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="24c4c-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="24c4c-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="24c4c-228">Propiedad canónica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="24c4c-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="24c4c-229">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="24c4c-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="24c4c-230">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="24c4c-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="24c4c-231">Propiedad canónica PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="24c4c-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="24c4c-232">Propiedad canónica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="24c4c-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="24c4c-233">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="24c4c-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="24c4c-234">Propiedad canónica PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="24c4c-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="24c4c-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="24c4c-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="24c4c-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="24c4c-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="24c4c-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24c4c-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="24c4c-238">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="24c4c-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

