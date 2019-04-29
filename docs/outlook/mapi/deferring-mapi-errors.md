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
ms.openlocfilehash: 0cf56a92190acfab1a941bc8d3ad0acc1f3e1f89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427342"
---
# <a name="deferring-mapi-errors"></a>Aplazamiento de errores de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos m�todos de interfaz aceptan la marca MAPI_DEFERRED_ERRORS como un par�metro de entrada. Cuando se establece este indicador, el m�todo no tiene que devolver inmediatamente con un valor; puede permitir que el autor de la llamada saber el resultado de la llamada en alg�n momento posterior.
  
Aplazamiento de errores ayuda a los proveedores de servicios en su implementaci�n de m�todos complejos, realizar el procesamiento m�s r�pido. En lugar de controlar muchas solicitudes y devolver un valor para cada uno, el aplazamiento de errores permite las llamadas a se agrupan en el proveedor de servicios. N�mero de solicitudes de procesamiento a la vez disminuye el tr�fico de red, lo que mejora el rendimiento. Aplazamiento de errores es especialmente �til en las llamadas a eliminar o copiar propiedades, que pueden ser operaciones mucho tiempo. 
  
Cuando un cliente realiza una llamada sin establecer el indicador MAPI_DEFERRED_ERRORS que s�lo se pueden gestionar de una manera diferida, los proveedores de servicios o bien pueden diferir los errores independientemente o devolver MAPI_E_TOO_COMPLEX. La mayor�a de los clientes deben aplazar errores como una estrategia preferible a errores la llamada. 
  
Establecer el MAPI_DEFERRED_ERRORS marca cambia error del cliente en una implementaci�n de control en que se puede entregar la informaci�n devuelta en cualquier momento, en lugar de a la vez planeada. Es posible que un error que se devuelve cuando es demasiado tarde para realizar cualquier operaci�n sobre �l o despu�s de datos acerca de la solicitud original ya no est�n disponibles. Por ejemplo, si un cliente llama a **IMsgStore::OpenEntry** para abrir una carpeta eliminada con conjunto MAPI_DEFERRED_ERRORS, el cliente no tiene que saber del problema hasta que se realiza una llamada de **IMAPIProp::GetProps** para recuperar una de las propiedades de la carpeta. **GetProps**, a continuaci�n, devolver� MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Ver también



[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)

