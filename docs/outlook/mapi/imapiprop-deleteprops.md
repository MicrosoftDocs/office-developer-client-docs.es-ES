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
# <a name="imapipropdeleteprops"></a><span data-ttu-id="9d586-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="9d586-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="9d586-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d586-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d586-105">Elimina una o más propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9d586-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="9d586-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9d586-106">Parameters</span></span>

 <span data-ttu-id="9d586-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="9d586-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="9d586-108">a Un puntero a una matriz de etiquetas de propiedad que indica las propiedades que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="9d586-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="9d586-109">El miembro **cValues** de la estructura [SPropTagArray](sproptagarray.md) a la que apunta _lpPropTagArray_ no debe ser cero, y el propio parámetro _lpPropTagArray_ no debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9d586-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="9d586-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="9d586-110">_lppProblems_</span></span>
  
> <span data-ttu-id="9d586-111">[in, out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no se necesita información de error.</span><span class="sxs-lookup"><span data-stu-id="9d586-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="9d586-112">Si _lppProblems_ es un puntero válido en la entrada, **DeleteProps** devuelve información detallada sobre los errores al eliminar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="9d586-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d586-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d586-113">Return value</span></span>

<span data-ttu-id="9d586-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d586-114">S_OK</span></span> 
  
> <span data-ttu-id="9d586-115">Las propiedades se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d586-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="9d586-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9d586-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9d586-117">El autor de la llamada no tiene permisos suficientes para eliminar propiedades.</span><span class="sxs-lookup"><span data-stu-id="9d586-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d586-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d586-118">Remarks</span></span>

<span data-ttu-id="9d586-119">El método **IMAPIProp::D eleteprops** quita una o más propiedades del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="9d586-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9d586-120">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="9d586-120">Notes to implementers</span></span>

<span data-ttu-id="9d586-121">No es necesario permitir que se eliminen propiedades de todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="9d586-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="9d586-122">Si el objeto no es modificable, devuelva MAPI_E_NO_ACCESS del método **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="9d586-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9d586-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9d586-123">Notes to callers</span></span>

<span data-ttu-id="9d586-124">No es necesario establecer el tipo de propiedad para cada etiqueta de propiedad en la matriz de etiquetas de propiedad a la que señala el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="9d586-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="9d586-125">Los tipos de propiedad se omiten; solo se usan los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d586-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="9d586-126">Tenga en cuenta que algunos objetos no permiten la modificación y que estos objetos devuelven MAPI_E_NO_ACCESS del método **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="9d586-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="9d586-127">Otros objetos permiten eliminar algunas propiedades, pero no otras.</span><span class="sxs-lookup"><span data-stu-id="9d586-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="9d586-128">Cuando hay un problema al eliminar solo algunas de las propiedades, **DeleteProps** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="9d586-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="9d586-129">Si ha pasado un puntero válido en el parámetro _lppProblems_ , **DeleteProps** establecerá el puntero a una estructura **SPropProblemArray** que contiene información detallada sobre los problemas de cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d586-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="9d586-130">Por ejemplo, si va a eliminar todas las propiedades de un mensaje y hay un problema con uno o varios de sus datos adjuntos, la estructura **SPropProblemArray** contendrá una entrada para el **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9d586-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="9d586-131">La estructura a la que apunta _lppProblems_ solo es válida si **DeleteProps** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="9d586-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="9d586-132">Si **DeleteProps** devuelve un error, no intente usar la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="9d586-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="9d586-133">En su lugar, llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) del objeto para obtener más información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="9d586-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="9d586-134">Libere la estructura **SPropProblemArray** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9d586-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9d586-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9d586-135">MFCMAPI reference</span></span>

<span data-ttu-id="9d586-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9d586-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9d586-137">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="9d586-137">**File**</span></span>|<span data-ttu-id="9d586-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="9d586-138">**Function**</span></span>|<span data-ttu-id="9d586-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9d586-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d586-140">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="9d586-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9d586-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="9d586-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="9d586-142">MFCMAPI usa el método **IMAPIProp::D eleteprops** para eliminar una propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9d586-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d586-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="9d586-143">See also</span></span>



[<span data-ttu-id="9d586-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9d586-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="9d586-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9d586-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9d586-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="9d586-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="9d586-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9d586-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9d586-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="9d586-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="9d586-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="9d586-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="9d586-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d586-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="9d586-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="9d586-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

