---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 82a7ecc8fbad0baf67b49c80c5a62cb8df94dfd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817107"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Hace referencia a**: Outlook 
  
Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Par�metros

_ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de texto de las cadenas devueltas. Se puede establecer la marca siguiente:
    
  - MAPI_CACHE_ONLY: Usar solo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
_lpPropTagArray_
  
> [entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indican las propiedades que requieren la actualización, si hay alguno. El parámetro _lpPropTagArray_ puede ser NULL. 
    
_lpRecipList_
  
> [entrada] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios se ha preparado correctamente.
    
MAPI_E_NOT_FOUND 
  
> No existen uno o varios de los destinatarios en el parámetro _lpRecipList_ . 
    
## <a name="return-value"></a>Valor devuelto

Un cliente llama al método MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) para modificar o reorganizar un conjunto de propiedades para uno o más destinatarios. Los destinatarios pueden o no pueden formar parte de la lista de destinatarios de un mensaje saliente. MAPI transfiere esta llamada al método **IABLogon::PrepareRecips** de un proveedor libreta de direcciones. 
  
**IABLogon::PrepareRecips** realiza cuatro tareas principales: 
  
- Se asegura de que todos los destinatarios en la lista de direcciones apunta por el parámetro _lpRecipList_ tiene un identificador de entrada a largo plazo. 
    
- Se asegura de que todos los destinatarios tienen las propiedades especificadas en la matriz de valores de la propiedad indicada por el parámetro _lpPropTagArray_ . 
    
- Se asegura de que las propiedades de la matriz de valores de propiedad aparecen antes de las demás propiedades que existían antes de la llamada.
    
- Se asegura de que el orden de las propiedades de [ADRENTRY](adrentry.md) estructura cada destinatario de la estructura de **ADRLIST** es la misma que en la matriz de valores de propiedad. 
    
La estructura **ADRENTRY** en el parámetro _lpRecipList_ contiene una estructura **ADRENTRY** para cada destinatario. Cada estructura **ADRENTRY** contiene una matriz de estructuras [SPropValue](spropvalue.md) para describir las propiedades del destinatario. Cuando se devuelve **IABLogon::PrepareRecips** , la matriz de la estructura de **SPropValue** para cada destinatario incluye las propiedades de la _lpPropTagArray_ seguido de las demás propiedades para el destinatario. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

La implementación de **IABLogon::PrepareRecips** implica la colocación de propiedades en un orden específico, recuperación de valores de propiedad y convertir los identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo. Las propiedades que se solicitan en el parámetro _lpPropTagArray_ deben ser al principio de la matriz de valores de propiedad asociado con la estructura **ADRENTRY** de cada destinatario en el parámetro _lpRecipList_ . Si no existen valores de estas propiedades, abra la lista de usuarios o distribución mensajería asociada mediante su identificador de entrada y recuperar los valores de propiedad que faltan. 
  
Asigne cada estructura **SPropValue** pasada por separado en _lpRecipList_ para que se pueden liberar las estructuras de forma individual. Si debe asignar espacio adicional para cualquier estructura **SPropValue** , por ejemplo, para almacenar los datos para una propiedad de cadena, use la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar espacio adicional para la matriz de valores de propiedad completa. Utilice la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de valores de propiedad original y, a continuación, utilice la función [MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional que se requiere. 
  
Para implementar **IABLogon::PrepareRecips**, use el procedimiento siguiente:
  
1. Compruebe si hay entradas en el parámetro _lpPropTagArray_ . Si la matriz de valores de propiedad está vacía, no hay ningún trabajo que hacer. Devolver un valor correcto. 
    
2. Proceso de cada destinatario en el parámetro _lpRecipList_ . Hay un miembro de la estructura **ADRENTRY** para cada destinatario en la lista. Omitir los siguientes tipos de destinatarios: 
    
   - Destinatarios sin un identificador de entrada en el miembro **rgPropVals** de su estructura **ADRENTRY** (es decir, los destinatarios sin resolver). 
    
   - Destinatarios con un identificador de entrada que no pertenecen a su proveedor. Estos destinatarios se pasan a otro proveedor de libreta de direcciones.
    
3. Abra al destinatario y recuperar las propiedades que ya están configuradas para el destinatario.
    
4. Combinar la matriz de valores de propiedad especificada en la _lpRecipList_ con la matriz de propiedades devuelto desde **GetProps**. Si se produce la misma propiedad en ambas matrices de propiedad, utilice el valor de _lpRecipList_.
    
5. Si la matriz de valores de propiedad _lpRecipList_ es lo suficientemente grande como para contener todas las propiedades necesarias, reemplace acaba con la matriz combinada. Si la matriz de valores de propiedad _lpRecipList_ no es lo suficientemente grande, reemplace con una matriz recién asignada. Asegúrese de que la nueva matriz tiene un valor actualizado en cada uno de sus miembros **cValues** . 
    
6. Si no reconoce una o varias de las propiedades en el parámetro _lpPropTagArray_ , establecer el tipo de propiedad en estructura **ADRENTRY** del destinatario a PT_ERROR y el valor de la propiedad a MAPI_E_NOT_FOUND o a otro valor que proporciona un mayor motivo específico de la no disponibilidad de la propiedad. Para obtener información sobre PT_ERROR, vea [Tipos de propiedades](property-types.md).
    
> [!NOTE]
> Reasignar nunca en la estructura **ADRLIST** que se pasó a **IABLogon::PrepareRecips** o cambiar su número de entradas. 
  
## <a name="see-also"></a>Vea también

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

