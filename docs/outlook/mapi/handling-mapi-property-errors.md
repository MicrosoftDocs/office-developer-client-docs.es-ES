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
# <a name="handling-mapi-property-errors"></a>Tratamiento de errores MAPI (propiedad)

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En lugar de �xito o fracaso completo, de los siguientes m�todos de **IMAPIProp** informan parcialmente correcta: 
  
[GetProps](imapiprop-getprops.md)
  
[SetProps](imapiprop-setprops.md)
  
[DeleteProps](imapiprop-deleteprops.md)
  
[CopyTo](imapiprop-copyto.md)
  
[CopyProps](imapiprop-copyprops.md)
  
**GetProps** informes parcialmente correcta cuando puede recuperar al menos una de las propiedades solicitadas para un objeto. **GetProps** indica �xito parcial devolver la advertencia MAPI_W_ERRORS_RETURNED y colocando informaci�n acerca de las propiedades no est� disponibles en la matriz de valores de propiedad que se�ala el par�metro **lppPropArray**. La entrada de una propiedad no est� disponible en esta matriz contiene PT_ERROR para el tipo de propiedad en el miembro **ulPropTag** y MAPI_E_NOT_FOUND o cualquier otro valor de error apropiado para el miembro **Value**. Por ejemplo, si un cliente llama **GetProps** m�todo de una carpeta para recuperar propiedades de tres y el tercero no est� disponible, el proveedor de almacenamiento de mensajes coloca PT_ERROR en el tercer tipo de propiedad en la matriz de valores de propiedad y MAPI_E_NOT_FOUND en el tercer valor de la propiedad. 
  
Los otros m�todos de **IMAPIProp** notificar parcialmente correcta de forma diferente. Estos m�todos informan �xito parcial devuelve S_OK y colocando informaci�n de error en una estructura [SPropProblemArray](spropproblemarray.md) . A diferencia de la matriz de valores de propiedad en **GetProps** que contiene los datos independientemente de si el m�todo se ha realizado correctamente o no se pudo, la matriz de problema de propiedad en estos m�todos existe s�lo si hay errores y s�lo si el autor de la llamada ha registrado inter�s en aprender acerca de los errores. Los autores de llamadas deben especificar un puntero v�lido **SPropProblemArray** para registrar para obtener informaci�n de error. 
  
Cuando se devuelve un valor de error de **SetProps**, **DeleteProps**, **CopyTo**o **CopyProps**, esto indica un error en lugar de �xito parcial. La matriz de problema (propiedad), si est� disponible, no es v�lida. No deben intentar tener acceso a datos que se conserva en la estructura de los clientes ni debe intentar liberar la propia estructura. La respuesta adecuada consiste en llamar [IMAPIProp::GetLastError](imapiprop-getlasterror.md). 
  
**GetLastError** es similar a la funci�n del mismo nombre proporcionado en el SDK de Windows. Ambos proporcionan que informaci�n m�s detallada sobre un error que est� disponible con el valor devuelto. Ambas devuelven informaci�n sobre el error anterior que se ha producido. La diferencia es que la funci�n de Win32 **GetLastError** informa sobre un error generado por el subproceso de llamada y el m�todo **IMAPIProp::GetLastError** informa sobre un error generado por el objeto actual. Es decir, si un cliente llama a **DeleteProps** en un mensaje y MAPI_E_NO_ACCESS se devuelve para indicar que el mensaje es de s�lo lectura, **GetLastError** devuelve datos proporcionados por el mensaje. 
  
## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

