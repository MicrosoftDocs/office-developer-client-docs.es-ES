---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817081"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="ffe2c-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="ffe2c-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="ffe2c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffe2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ffe2c-105">Copia las entradas de uno o más, los usuarios normalmente mensajería o listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ffe2c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffe2c-106">Parameters</span></span>

 <span data-ttu-id="ffe2c-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="ffe2c-107">_lpEntries_</span></span>
  
> <span data-ttu-id="ffe2c-108">[entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que contiene los identificadores de entrada de las entradas para copiar.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="ffe2c-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ffe2c-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="ffe2c-110">[entrada] El identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="ffe2c-111">El parámetro _ulUIParam_ debe ser cero si se establece la marca AB_NO_DIALOG en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="ffe2c-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ffe2c-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="ffe2c-112">_lpProgress_</span></span>
  
> <span data-ttu-id="ffe2c-113">[entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso o NULL.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="ffe2c-114">Si _lpProgress_ es NULL, se debe mostrar un indicador de progreso con el objeto de progreso proporcionado por MAPI a través del método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="ffe2c-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="ffe2c-115">El parámetro _lpProgress_ se omite si se establece la marca AB_NO_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="ffe2c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ffe2c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ffe2c-117">[entrada] Una máscara de bits de indicadores que controla cómo se realiza la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="ffe2c-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="ffe2c-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ffe2c-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ffe2c-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="ffe2c-120">Suprime la visualización de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="ffe2c-121">Si no se establece este marcador, se muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="ffe2c-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="ffe2c-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="ffe2c-123">Indica que se debe realizar un nivel separado de comprobación de la entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="ffe2c-124">La implementación de comprobación de la entrada duplicada suelto es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="ffe2c-125">Por ejemplo, un proveedor puede definir a una coincidencia separada como las dos entradas que tienen el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="ffe2c-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="ffe2c-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="ffe2c-127">Indica que se debe realizar un nivel estricto de comprobación de la entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="ffe2c-128">La implementación de comprobación estricta entrada duplicada es específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="ffe2c-129">Por ejemplo, un proveedor puede definir a una coincidencia estricta como las dos entradas que tienen ambos el mismo nombre para mostrar y la dirección de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="ffe2c-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="ffe2c-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="ffe2c-131">Indica que una nueva entrada debe reemplazar uno existente si se determina que las dos son duplicados.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ffe2c-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffe2c-132">Return value</span></span>

<span data-ttu-id="ffe2c-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="ffe2c-133">S_OK</span></span> 
  
> <span data-ttu-id="ffe2c-134">Se ha realizado correctamente la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="ffe2c-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="ffe2c-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="ffe2c-136">La operación de copia satisfactoria, pero no se podrían copiar uno o más de las entradas.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="ffe2c-137">Cuando se devuelve este valor, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="ffe2c-138">Para probar este valor, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="ffe2c-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="ffe2c-139">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ffe2c-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ffe2c-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffe2c-140">Remarks</span></span>

<span data-ttu-id="ffe2c-141">El método **IABContainer::CopyEntries** copia entradas desde el mismo contenedor o un contenedor diferente.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="ffe2c-142">Una llamada a **CopyEntries** es funcionalmente equivalente a hacer que las llamadas siguientes para cada entrada que se va a copiar:</span><span class="sxs-lookup"><span data-stu-id="ffe2c-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="ffe2c-143">El método [IABContainer::CreateEntry](iabcontainer-createentry.md) para crear la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="ffe2c-144">El método [IMAPIProp::GetProps](imapiprop-getprops.md) para leer las propiedades de la entrada que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="ffe2c-145">El método [IMAPIProp::SetProps](imapiprop-setprops.md) para escribir las propiedades para la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="ffe2c-146">[IMAPIProp::SaveChanges](imapiprop-savechanges.md) (método) de la nueva entrada para llevar a cabo un proceso de guardar.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="ffe2c-147">[IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) (método) de la nueva entrada para liberar la referencia del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-147">The new entry's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ffe2c-148">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="ffe2c-148">Notes to implementers</span></span>

<span data-ttu-id="ffe2c-149">Todos los contenedores que admiten el método **IABContainer::CopyEntries** deben ser modificables.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="ffe2c-150">Establecer marca AB_MODIFIABLE de su contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="ffe2c-151">Debe admitir todas las marcas; Sin embargo, la interpretación y el uso de estos indicadores es específico de la implementación, es decir, puede determinar el significado de la semántica de los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de su implementación.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="ffe2c-152">Si no puede o no determinar si una entrada es un duplicado, permitir siempre la entrada que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="ffe2c-153">Si se establece la marca CREATE_REPLACE, copie siempre la entrada, independientemente de si se ha establecido CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT y si la entrada es un duplicado.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="ffe2c-154">Si no se ha establecido CREATE_REPLACE y CREATE_CHECK_DUP_STRICT se establece, compruebe si existen duplicados.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="ffe2c-155">Si una entrada se determina como un duplicado, no copie la entrada.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="ffe2c-156">No es necesario admitir CREATE_REPLACE; no se admite la CREATE_REPLACE significa que puede omitir de forma segura y siempre realizar una copia.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="ffe2c-157">Devolver la advertencia MAPI_W_PARTIAL_COMPLETION sólo si no se puede copiar una entrada no duplicada.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ffe2c-158">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ffe2c-158">Notes to callers</span></span>

<span data-ttu-id="ffe2c-159">Utilice los indicadores CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT para indicar al proveedor de cómo desea que el contenedor para realizar la comprobación de entrada de duplicado.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="ffe2c-160">Si necesita tener una entrada agregada independientemente de que sea un duplicado, no configure cualquiera de estos marcadores o establecer la marca CREATE_REPLACE.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="ffe2c-161">CREATE_REPLACE indica que no importa si una entrada es un duplicado; siempre que desea reemplazar la entrada original.</span><span class="sxs-lookup"><span data-stu-id="ffe2c-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ffe2c-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffe2c-162">See also</span></span>



[<span data-ttu-id="ffe2c-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ffe2c-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="ffe2c-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="ffe2c-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="ffe2c-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ffe2c-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="ffe2c-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ffe2c-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="ffe2c-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ffe2c-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

