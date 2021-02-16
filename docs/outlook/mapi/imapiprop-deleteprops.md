---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409240"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="38268-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="38268-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="38268-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38268-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38268-105">Elimina una o más propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="38268-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="38268-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38268-106">Parameters</span></span>

 <span data-ttu-id="38268-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="38268-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="38268-108">[entrada] Puntero a una matriz de etiquetas de propiedad que indican las propiedades que se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="38268-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="38268-109">El **miembro cValues** de la estructura [SPropTagArray](sproptagarray.md) a la que apunta  _lpPropTagArray_ no debe ser cero y el propio parámetro  _lpPropTagArray_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="38268-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="38268-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="38268-110">_lppProblems_</span></span>
  
> <span data-ttu-id="38268-111">[entrada, salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo contrario, NULL, que indica que no es necesario obtener información de errores.</span><span class="sxs-lookup"><span data-stu-id="38268-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="38268-112">Si  _lppProblems_ es un puntero válido en la entrada, **DeleteProps** devuelve información detallada sobre los errores al eliminar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="38268-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38268-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38268-113">Return value</span></span>

<span data-ttu-id="38268-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="38268-114">S_OK</span></span> 
  
> <span data-ttu-id="38268-115">Las propiedades se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="38268-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="38268-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="38268-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="38268-117">El llamador no tiene permisos suficientes para eliminar propiedades.</span><span class="sxs-lookup"><span data-stu-id="38268-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38268-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38268-118">Remarks</span></span>

<span data-ttu-id="38268-119">El **método IMAPIProp::D eleteProps** quita una o más propiedades del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="38268-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="38268-120">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="38268-120">Notes to implementers</span></span>

<span data-ttu-id="38268-121">No es necesario permitir que las propiedades se eliminen de todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="38268-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="38268-122">Si el objeto no es modificable, devuelva MAPI_E_NO_ACCESS del **método DeleteProps.**</span><span class="sxs-lookup"><span data-stu-id="38268-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="38268-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="38268-123">Notes to callers</span></span>

<span data-ttu-id="38268-124">No es necesario establecer el tipo de propiedad para cada etiqueta de propiedad en la matriz de etiquetas de propiedad a la que apunta el parámetro _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="38268-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="38268-125">Los tipos de propiedad se omiten; solo se usan los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="38268-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="38268-126">Tenga en cuenta que algunos objetos no permiten la modificación y que estos objetos devuelven MAPI_E_NO_ACCESS del **método DeleteProps.**</span><span class="sxs-lookup"><span data-stu-id="38268-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="38268-127">Otros objetos permiten que algunas propiedades se eliminen, pero no otras.</span><span class="sxs-lookup"><span data-stu-id="38268-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="38268-128">Cuando se produce un problema al eliminar solo algunas de las propiedades, **DeleteProps** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="38268-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="38268-129">Si ha pasado un puntero válido en el parámetro  _lppProblems,_ **DeleteProps** establecerá el puntero en una estructura **SPropProblemArray** que contiene información detallada sobre los problemas con cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="38268-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="38268-130">Por ejemplo, si elimina todas las propiedades de un mensaje y hay un problema con uno o varios de sus datos adjuntos, la estructura **SPropProblemArray** contendrá una entrada para la propiedad **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="38268-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="38268-131">La estructura a la que  _apunta lppProblems_ solo es válida si **DeleteProps** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="38268-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="38268-132">Si **DeleteProps devuelve** un error, no intente usar la **estructura SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="38268-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="38268-133">En su lugar, llame al método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) del objeto para obtener más información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="38268-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="38268-134">Libera la estructura **SPropProblemArray** devuelta llamando a la [función MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="38268-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38268-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38268-135">MFCMAPI reference</span></span>

<span data-ttu-id="38268-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="38268-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38268-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="38268-137">**File**</span></span>|<span data-ttu-id="38268-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="38268-138">**Function**</span></span>|<span data-ttu-id="38268-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="38268-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38268-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="38268-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="38268-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="38268-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="38268-142">MFCMAPI usa el **método IMAPIProp::D eleteProps** para eliminar una propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="38268-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38268-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38268-143">See also</span></span>



[<span data-ttu-id="38268-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="38268-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="38268-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="38268-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="38268-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="38268-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="38268-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="38268-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="38268-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="38268-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="38268-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="38268-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="38268-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38268-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="38268-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="38268-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

