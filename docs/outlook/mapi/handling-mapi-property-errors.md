---
title: Tratamiento de errores MAPI (propiedad)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 82f37e2a6f6834c7a8553a3d9d364f7e657d81da
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579511"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="fdc17-103">Tratamiento de errores MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fdc17-103">Handling MAPI property errors</span></span>

<span data-ttu-id="fdc17-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdc17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdc17-105">En lugar de �xito o fracaso completo, de los siguientes m�todos de **IMAPIProp** informan parcialmente correcta:</span><span class="sxs-lookup"><span data-stu-id="fdc17-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="fdc17-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="fdc17-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="fdc17-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="fdc17-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="fdc17-108">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="fdc17-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="fdc17-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="fdc17-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="fdc17-110">CopyProps</span><span class="sxs-lookup"><span data-stu-id="fdc17-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="fdc17-p101">**GetProps** informes parcialmente correcta cuando puede recuperar al menos una de las propiedades solicitadas para un objeto. **GetProps** indica �xito parcial devolver la advertencia MAPI_W_ERRORS_RETURNED y colocando informaci�n acerca de las propiedades no est� disponibles en la matriz de valores de propiedad que se�ala el par�metro **lppPropArray**. La entrada de una propiedad no est� disponible en esta matriz contiene PT_ERROR para el tipo de propiedad en el miembro **ulPropTag** y MAPI_E_NOT_FOUND o cualquier otro valor de error apropiado para el miembro **Value**. Por ejemplo, si un cliente llama **GetProps** m�todo de una carpeta para recuperar propiedades de tres y el tercero no est� disponible, el proveedor de almacenamiento de mensajes coloca PT_ERROR en el tercer tipo de propiedad en la matriz de valores de propiedad y MAPI_E_NOT_FOUND en el tercer valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p101">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="fdc17-p102">Los otros m�todos de **IMAPIProp** notificar parcialmente correcta de forma diferente. Estos m�todos informan �xito parcial devuelve S_OK y colocando informaci�n de error en una estructura [SPropProblemArray](spropproblemarray.md) . A diferencia de la matriz de valores de propiedad en **GetProps** que contiene los datos independientemente de si el m�todo se ha realizado correctamente o no se pudo, la matriz de problema de propiedad en estos m�todos existe s�lo si hay errores y s�lo si el autor de la llamada ha registrado inter�s en aprender acerca de los errores. Los autores de llamadas deben especificar un puntero v�lido **SPropProblemArray** para registrar para obtener informaci�n de error.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p102">The other **IMAPIProp** methods report partial success differently. These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure. Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors. Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="fdc17-p103">Cuando se devuelve un valor de error de **SetProps**, **DeleteProps**, **CopyTo**o **CopyProps**, esto indica un error en lugar de �xito parcial. La matriz de problema (propiedad), si est� disponible, no es v�lida. No deben intentar tener acceso a datos que se conserva en la estructura de los clientes ni debe intentar liberar la propia estructura. La respuesta adecuada consiste en llamar [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="fdc17-p103">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success. The property problem array, if available, is not valid. Clients should not try to access data held in the structure nor should they try to free the structure itself. The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="fdc17-p104">**GetLastError** es similar a la funci�n del mismo nombre proporcionado en el SDK de Windows. Ambos proporcionan que informaci�n m�s detallada sobre un error que est� disponible con el valor devuelto. Ambas devuelven informaci�n sobre el error anterior que se ha producido. La diferencia es que la funci�n de Win32 **GetLastError** informa sobre un error generado por el subproceso de llamada y el m�todo **IMAPIProp::GetLastError** informa sobre un error generado por el objeto actual. Es decir, si un cliente llama a **DeleteProps** en un mensaje y MAPI_E_NO_ACCESS se devuelve para indicar que el mensaje es de s�lo lectura, **GetLastError** devuelve datos proporcionados por el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fdc17-p104">**GetLastError** is similar to the function of the same name provided in the Windows SDK. Both provide more detailed information about an error than is available with the return value. They both return information about the previous error that has occurred. The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object. That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fdc17-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdc17-128">See also</span></span>

- [<span data-ttu-id="fdc17-129">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fdc17-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

