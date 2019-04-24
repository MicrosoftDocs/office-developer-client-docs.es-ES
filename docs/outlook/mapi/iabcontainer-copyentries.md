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
# <a name="iabcontainercopyentries"></a><span data-ttu-id="c9f8f-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="c9f8f-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="c9f8f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9f8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9f8f-105">Copia una o más entradas, normalmente usuarios de mensajería o listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c9f8f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c9f8f-106">Parameters</span></span>

 <span data-ttu-id="c9f8f-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="c9f8f-107">_lpEntries_</span></span>
  
> <span data-ttu-id="c9f8f-108">a Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que contiene los identificadores de entrada de las entradas que se van a copiar.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="c9f8f-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c9f8f-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c9f8f-110">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="c9f8f-111">El parámetro _ulUIParam_ debe ser cero si el indicador AB_NO_DIALOG está establecido en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="c9f8f-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c9f8f-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c9f8f-112">_lpProgress_</span></span>
  
> <span data-ttu-id="c9f8f-113">a Un puntero a un objeto Progress que muestra un indicador de progreso o NULL.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="c9f8f-114">Si _lpProgress_ es null, debe mostrarse un indicador de progreso mediante el objeto Progress proporcionado por MAPI a través del método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f8f-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="c9f8f-115">El parámetro _lpProgress_ se omite si la marca AB_NO_DIALOG se establece en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="c9f8f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9f8f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="c9f8f-117">a Una máscara de máscara de marcadores que controla cómo se realiza la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="c9f8f-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c9f8f-118">The following flags can be set:</span></span>
    
<span data-ttu-id="c9f8f-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c9f8f-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="c9f8f-120">SuPrime la visualización de un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="c9f8f-121">Si no se establece esta marca, se muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="c9f8f-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="c9f8f-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="c9f8f-123">Indica que se debe realizar un nivel flexible de comprobación de entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c9f8f-124">La implementación de la comprobación de entradas duplicadas perdidas es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c9f8f-125">Por ejemplo, un proveedor puede definir una coincidencia perdida como dos entradas que tienen el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="c9f8f-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="c9f8f-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="c9f8f-127">Indica que se debe realizar un nivel estricto de comprobación de entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c9f8f-128">La implementación de una comprobación de entrada de duplicados estrictas es específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c9f8f-129">Por ejemplo, un proveedor puede definir una coincidencia estricta como dos entradas que tienen el mismo nombre para mostrar y la misma dirección de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="c9f8f-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="c9f8f-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="c9f8f-131">Indica que una nueva entrada debe reemplazar a una existente si se determina que los dos son duplicados.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9f8f-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9f8f-132">Return value</span></span>

<span data-ttu-id="c9f8f-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9f8f-133">S_OK</span></span> 
  
> <span data-ttu-id="c9f8f-134">La operación de copia se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="c9f8f-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c9f8f-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c9f8f-136">La operación de copia se realizó en general, pero no se pudo copiar una o más de las entradas.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="c9f8f-137">Cuando se devuelve este valor, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c9f8f-138">Para comprobar este valor, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="c9f8f-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c9f8f-139">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c9f8f-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9f8f-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9f8f-140">Remarks</span></span>

<span data-ttu-id="c9f8f-141">El método **IABContainer:: CopyEntries** copia entradas del mismo contenedor o de un contenedor diferente.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="c9f8f-142">Una llamada a **CopyEntries** es equivalente funcionalmente a realizar las siguientes llamadas para cada entrada que se va a copiar:</span><span class="sxs-lookup"><span data-stu-id="c9f8f-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="c9f8f-143">El método [IABContainer:: CreateEntry](iabcontainer-createentry.md) para crear la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="c9f8f-144">El método [IMAPIProp:: GetProps](imapiprop-getprops.md) para leer las propiedades de la entrada que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="c9f8f-145">El método [IMAPIProp:: SetProps](imapiprop-setprops.md) para escribir propiedades en la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="c9f8f-146">El método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del nuevo elemento que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="c9f8f-147">El método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) del nuevo elemento para liberar la referencia del contenedor.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c9f8f-148">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="c9f8f-148">Notes to implementers</span></span>

<span data-ttu-id="c9f8f-149">Todos los contenedores que admiten el método **IABContainer:: CopyEntries** deben ser modificables.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="c9f8f-150">Establezca la marca AB_MODIFIABLE del contenedor en su propiedad **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) para indicar que es modificable.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="c9f8f-151">Debe admitir todas las marcas; sin embargo, la interpretación y el uso de estas marcas son específicos de la implementación, es decir, puede determinar cuál es la semántica de las marcas CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT en el contexto de la implementación.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="c9f8f-152">Si no puede o no determina si una entrada es un duplicado, permita siempre que se copie la entrada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="c9f8f-153">Si se establece la marca CREATE_REPLACE, siempre se copia la entrada independientemente de si se ha establecido CREATE_CHECK_DUP_LOOSE o CREATE_CHECK_DUP_STRICT y si la entrada es un duplicado.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="c9f8f-154">Si CREATE_REPLACE no está establecido y CREATE_CHECK_DUP_STRICT está establecido, compruebe si hay duplicados.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="c9f8f-155">Si una entrada se determina como duplicada, no copie la entrada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="c9f8f-156">No es necesario que admita CREATE_REPLACE; no admitir CREATE_REPLACE significa que puede ignorarlo sin problemas y realizar siempre una copia.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="c9f8f-157">DeVuelva la advertencia MAPI_W_PARTIAL_COMPLETION solo si no se puede copiar una entrada no duplicada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9f8f-158">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c9f8f-158">Notes to callers</span></span>

<span data-ttu-id="c9f8f-159">Use las marcas CREATE_CHECK_DUP_LOOSE y CREATE_CHECK_DUP_STRICT para indicar al proveedor cómo desea que el contenedor realice la comprobación de entrada duplicada.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="c9f8f-160">Si necesita tener una entrada agregada independientemente de si es un duplicado, no establezca ninguno de estos indicadores o establezca la marca CREATE_REPLACE.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="c9f8f-161">CREATE_REPLACE indica que no le interesa si una entrada es un duplicado; siempre desea que reemplace la entrada original.</span><span class="sxs-lookup"><span data-stu-id="c9f8f-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9f8f-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9f8f-162">See also</span></span>



[<span data-ttu-id="c9f8f-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="c9f8f-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="c9f8f-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="c9f8f-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="c9f8f-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9f8f-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="c9f8f-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c9f8f-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c9f8f-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c9f8f-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

