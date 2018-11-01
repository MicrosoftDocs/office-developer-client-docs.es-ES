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
ms.openlocfilehash: a0d86b9b0342beea6b33db0219cb5889d2e63f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592076"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="ce63b-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="ce63b-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="ce63b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce63b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce63b-105">Elimina una o más propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ce63b-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ce63b-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ce63b-106">Parameters</span></span>

 <span data-ttu-id="ce63b-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="ce63b-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="ce63b-108">[entrada] Un puntero a una matriz de etiquetas de propiedad que indican las propiedades para eliminar.</span><span class="sxs-lookup"><span data-stu-id="ce63b-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="ce63b-109">El miembro **cValues** de la estructura del [elemento SPropTagArray](sproptagarray.md) que señala _lpPropTagArray_ no debe ser cero, y el parámetro _lpPropTagArray_ propio no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ce63b-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="ce63b-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="ce63b-110">_lppProblems_</span></span>
  
> <span data-ttu-id="ce63b-111">[entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no es necesario para obtener información de error.</span><span class="sxs-lookup"><span data-stu-id="ce63b-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="ce63b-112">Si _lppProblems_ es un puntero válido en la entrada, **DeleteProps** devuelve información detallada acerca de los errores al eliminar una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce63b-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce63b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce63b-113">Return value</span></span>

<span data-ttu-id="ce63b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce63b-114">S_OK</span></span> 
  
> <span data-ttu-id="ce63b-115">Las propiedades se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce63b-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="ce63b-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ce63b-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ce63b-117">El autor de la llamada no tiene permisos suficientes para eliminar propiedades.</span><span class="sxs-lookup"><span data-stu-id="ce63b-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce63b-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce63b-118">Remarks</span></span>

<span data-ttu-id="ce63b-119">El método **IMAPIProp::DeleteProps** quita una o varias propiedades del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="ce63b-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ce63b-120">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ce63b-120">Notes to implementers</span></span>

<span data-ttu-id="ce63b-121">No es necesario que permitir que las propiedades que se eliminará de todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="ce63b-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="ce63b-122">Si el objeto no es modificable, devuelva MAPI_E_NO_ACCESS desde el método **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="ce63b-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce63b-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ce63b-123">Notes to callers</span></span>

<span data-ttu-id="ce63b-124">No es necesario que establecer el tipo de propiedad para cada etiqueta de la propiedad en la matriz de etiqueta de la propiedad indicada por el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="ce63b-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="ce63b-125">Tipos de propiedad se omiten; se usan sólo los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ce63b-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="ce63b-126">Tenga en cuenta que algunos objetos no permitir la modificación y que estos objetos devuelven MAPI_E_NO_ACCESS desde el método **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="ce63b-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="ce63b-127">Permitir que otros objetos de algunas propiedades que se va a eliminar, pero no para otros.</span><span class="sxs-lookup"><span data-stu-id="ce63b-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="ce63b-128">Cuando hay un problema al eliminar sólo algunas de las propiedades, **DeleteProps** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="ce63b-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="ce63b-129">Si han transcurrido un puntero válido en el parámetro _lppProblems_ , **DeleteProps** establecerá el puntero a una estructura **SPropProblemArray** que contiene información detallada acerca de los problemas con cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="ce63b-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="ce63b-130">Por ejemplo, si se va a eliminar todas las propiedades de un mensaje y hay un problema con uno o varios de sus datos adjuntos, la estructura **SPropProblemArray** contendrá una entrada para el **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) (propiedad).</span><span class="sxs-lookup"><span data-stu-id="ce63b-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="ce63b-131">La estructura que señala _lppProblems_ sólo es válida si **DeleteProps** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="ce63b-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="ce63b-132">Si **DeleteProps** devuelve un error, no intente utilizar la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="ce63b-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="ce63b-133">En su lugar, llame al método del objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para obtener más información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="ce63b-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="ce63b-134">Libere la estructura **SPropProblemArray** devuelta mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ce63b-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce63b-135">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce63b-135">MFCMAPI reference</span></span>

<span data-ttu-id="ce63b-136">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ce63b-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce63b-137">**File**</span><span class="sxs-lookup"><span data-stu-id="ce63b-137">**File**</span></span>|<span data-ttu-id="ce63b-138">**Función**</span><span class="sxs-lookup"><span data-stu-id="ce63b-138">**Function**</span></span>|<span data-ttu-id="ce63b-139">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ce63b-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce63b-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ce63b-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ce63b-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="ce63b-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="ce63b-142">MFCMAPI usa el método **IMAPIProp::DeleteProps** para eliminar una propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ce63b-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce63b-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce63b-143">See also</span></span>



[<span data-ttu-id="ce63b-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ce63b-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="ce63b-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ce63b-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="ce63b-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ce63b-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="ce63b-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ce63b-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ce63b-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="ce63b-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="ce63b-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ce63b-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="ce63b-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce63b-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="ce63b-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ce63b-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

