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
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346399"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="7d4a6-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="7d4a6-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="7d4a6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d4a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d4a6-105">Copia una o más entradas, normalmente usuarios de mensajería o listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7d4a6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7d4a6-106">Parameters</span></span>

 <span data-ttu-id="7d4a6-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="7d4a6-107">_lpEntries_</span></span>
  
> <span data-ttu-id="7d4a6-108">[in] Puntero a una matriz de [estructuras ENTRYLIST](entrylist.md) que contiene los identificadores de entrada de las entradas que se copian.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="7d4a6-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7d4a6-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="7d4a6-110">[in] El identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="7d4a6-111">El _parámetro ulUIParam_ debe ser cero si la marca AB_NO_DIALOG se establece en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="7d4a6-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7d4a6-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="7d4a6-112">_lpProgress_</span></span>
  
> <span data-ttu-id="7d4a6-113">[in] Puntero a un objeto de progreso que muestra un indicador de progreso o NULL.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="7d4a6-114">Si _lpProgress_ es NULL, se debe mostrar un indicador de progreso mediante el objeto de progreso proporcionado por MAPI a través del método [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md)</span><span class="sxs-lookup"><span data-stu-id="7d4a6-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="7d4a6-115">El  _parámetro lpProgress_ se omite si la marca AB_NO_DIALOG se establece en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7d4a6-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d4a6-116">_ulFlags_</span></span>
  
> <span data-ttu-id="7d4a6-117">[in] Máscara de bits de marcas que controla cómo se realiza la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="7d4a6-118">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="7d4a6-118">The following flags can be set:</span></span>
    
<span data-ttu-id="7d4a6-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7d4a6-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="7d4a6-120">Suprime la presentación de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="7d4a6-121">Si no se establece esta marca, se muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="7d4a6-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="7d4a6-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="7d4a6-123">Indica que debe realizarse un nivel suelto de comprobación de entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="7d4a6-124">La implementación de la comprobación de entrada duplicada suelta es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="7d4a6-125">Por ejemplo, un proveedor puede definir una coincidencia suelta como cualquier dos entradas que tengan el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="7d4a6-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="7d4a6-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="7d4a6-127">Indica que se debe realizar un nivel estricto de comprobación de entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="7d4a6-128">La implementación de la comprobación estricta de entradas duplicadas es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="7d4a6-129">Por ejemplo, un proveedor puede definir una coincidencia estricta como cualquiera de las dos entradas que tienen el mismo nombre para mostrar y la misma dirección de mensajería.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="7d4a6-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="7d4a6-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="7d4a6-131">Indica que una nueva entrada debe reemplazar una existente si se determina que los dos son duplicados.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d4a6-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d4a6-132">Return value</span></span>

<span data-ttu-id="7d4a6-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d4a6-133">S_OK</span></span> 
  
> <span data-ttu-id="7d4a6-134">La operación de copia se ha correcto.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="7d4a6-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7d4a6-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7d4a6-136">La operación de copia se ha hecho correctamente en general, pero no se pudo copiar una o varias de las entradas.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="7d4a6-137">Cuando se devuelve este valor, la llamada debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7d4a6-138">Para probar este valor, use la **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7d4a6-139">Para obtener más información, vea [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7d4a6-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d4a6-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d4a6-140">Remarks</span></span>

<span data-ttu-id="7d4a6-141">El **método IABContainer::CopyEntries** copia entradas del mismo contenedor o de un contenedor diferente.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="7d4a6-142">Una llamada a **CopyEntries** es funcionalmente equivalente a realizar las siguientes llamadas para cada entrada que se va a copiar:</span><span class="sxs-lookup"><span data-stu-id="7d4a6-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="7d4a6-143">El [método IABContainer::CreateEntry](iabcontainer-createentry.md) para crear la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="7d4a6-144">El [método IMAPIProp::GetProps](imapiprop-getprops.md) para leer las propiedades de la entrada que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="7d4a6-145">El [método IMAPIProp::SetProps](imapiprop-setprops.md) para escribir propiedades en la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="7d4a6-146">Método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nueva entrada para realizar un guardado.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="7d4a6-147">El método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) de la nueva entrada para liberar la referencia del contenedor.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="7d4a6-148">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="7d4a6-148">Notes to implementers</span></span>

<span data-ttu-id="7d4a6-149">Todos los contenedores que admiten **el método IABContainer::CopyEntries** deben ser modificables.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="7d4a6-150">Establezca la marca de AB_MODIFIABLE contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="7d4a6-151">Debe admitir todas las marcas; sin embargo, la interpretación y el uso de estas marcas es específico de la implementación, es decir, puede determinar lo que significa la semántica de las marcas CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de la implementación.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="7d4a6-152">Si no puede o no determinar si una entrada es un duplicado, permita siempre que se copie la entrada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="7d4a6-153">Si se CREATE_REPLACE marca, copie siempre la entrada independientemente de si CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT está establecida y si la entrada es un duplicado.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="7d4a6-154">Si CREATE_REPLACE está establecido y CREATE_CHECK_DUP_STRICT, compruebe si hay duplicados.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="7d4a6-155">Si se determina que una entrada es un duplicado, no copie la entrada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="7d4a6-156">No es necesario que admita CREATE_REPLACE; no admitir CREATE_REPLACE significa que puede ignorarlo de forma segura y realizar siempre una copia.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="7d4a6-157">Devuelve la advertencia MAPI_W_PARTIAL_COMPLETION solo si no se puede copiar una entrada no duplicada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7d4a6-158">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="7d4a6-158">Notes to callers</span></span>

<span data-ttu-id="7d4a6-159">Use las CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT para indicar al proveedor cómo desea que el contenedor realice la comprobación de entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="7d4a6-160">Si necesita agregar una entrada independientemente de si se trata de un duplicado, no establezca ninguna de estas marcas ni establezca la marca CREATE_REPLACE.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="7d4a6-161">CREATE_REPLACE indica que no le importa si una entrada es un duplicado; siempre desea que reemplace la entrada original.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d4a6-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d4a6-162">See also</span></span>



[<span data-ttu-id="7d4a6-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="7d4a6-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="7d4a6-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="7d4a6-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="7d4a6-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d4a6-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="7d4a6-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="7d4a6-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="7d4a6-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7d4a6-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

