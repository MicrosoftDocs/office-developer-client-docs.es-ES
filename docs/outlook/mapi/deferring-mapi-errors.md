---
title: Aplazamiento de errores de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3d2a46be04f235ba55aa5f2feef222ea7372b211
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569865"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="4b67a-103">Aplazamiento de errores de MAPI</span><span class="sxs-lookup"><span data-stu-id="4b67a-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="4b67a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b67a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b67a-p101">Algunos m�todos de interfaz aceptan la marca MAPI_DEFERRED_ERRORS como un par�metro de entrada. Cuando se establece este indicador, el m�todo no tiene que devolver inmediatamente con un valor; puede permitir que el autor de la llamada saber el resultado de la llamada en alg�n momento posterior.</span><span class="sxs-lookup"><span data-stu-id="4b67a-p101">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter. When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="4b67a-p102">Aplazamiento de errores ayuda a los proveedores de servicios en su implementaci�n de m�todos complejos, realizar el procesamiento m�s r�pido. En lugar de controlar muchas solicitudes y devolver un valor para cada uno, el aplazamiento de errores permite las llamadas a se agrupan en el proveedor de servicios. N�mero de solicitudes de procesamiento a la vez disminuye el tr�fico de red, lo que mejora el rendimiento. Aplazamiento de errores es especialmente �til en las llamadas a eliminar o copiar propiedades, que pueden ser operaciones mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b67a-p102">Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="4b67a-p103">Cuando un cliente realiza una llamada sin establecer el indicador MAPI_DEFERRED_ERRORS que s�lo se pueden gestionar de una manera diferida, los proveedores de servicios o bien pueden diferir los errores independientemente o devolver MAPI_E_TOO_COMPLEX. La mayor�a de los clientes deben aplazar errores como una estrategia preferible a errores la llamada.</span><span class="sxs-lookup"><span data-stu-id="4b67a-p103">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX. Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="4b67a-p104">Establecer el MAPI_DEFERRED_ERRORS marca cambia error del cliente en una implementaci�n de control en que se puede entregar la informaci�n devuelta en cualquier momento, en lugar de a la vez planeada. Es posible que un error que se devuelve cuando es demasiado tarde para realizar cualquier operaci�n sobre �l o despu�s de datos acerca de la solicitud original ya no est�n disponibles. Por ejemplo, si un cliente llama a **IMsgStore::OpenEntry** para abrir una carpeta eliminada con conjunto MAPI_DEFERRED_ERRORS, el cliente no tiene que saber del problema hasta que se realiza una llamada de **IMAPIProp::GetProps** para recuperar una de las propiedades de la carpeta. **GetProps**, a continuaci�n, devolver� MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="4b67a-p104">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b67a-117">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="4b67a-117">See also</span></span>



[<span data-ttu-id="4b67a-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4b67a-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="4b67a-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="4b67a-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

