---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563880"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara una lista de destinatarios para usarlo más adelante mediante el sistema de mensajería. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada. Se puede establecer la marca siguiente:
    
MAPI_CACHE_ONLY
  
> Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación de cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y tener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor. Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.
    
 _lpSPropTagArray_
  
> [entrada] Un puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indican las propiedades, si lo hay, que requieren actualización. El parámetro _lpSPropTagArray_ puede ser NULL. 
    
 _lpRecipList_
  
> [entrada] Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios se ha preparado correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios de llaman al método **PrepareRecips** para hacer lo siguiente: 
  
- Asegúrese de que todos los destinatarios en el parámetro _lpRecipList_ tienen los identificadores de entrada a largo plazo. 
    
- Asegúrese de que cada destinatario en el parámetro _lpRecipList_ tiene las propiedades enumeradas en el parámetro _lpSPropTagArray_ y que estas propiedades aparecen al principio de la lista de destinatarios. 
    
MAPI convierte los identificadores de entrada a corto plazo de cada destinatario en los identificadores de entrada a largo plazo. Si es necesario, los identificadores de entrada a largo plazo de los destinatarios se recuperan desde el proveedor de libreta de direcciones adecuado y se solicitan las propiedades adicionales.
  
En una entrada de destinatarios individual, las propiedades solicitadas se ordenan en primer lugar, seguido de todas las propiedades que ya estaban presentes para la entrada. Si una o varias de las propiedades solicitadas en el parámetro _lpSPropTagArray_ no se controlan mediante el proveedor de libreta de direcciones adecuado, sus tipos de propiedad se establecerá en PT_ERROR. Sus valores de propiedad se establecerá en a MAPI_E_NOT_FOUND o a otro valor que proporciona un motivo más específico, ¿por qué las propiedades no están disponibles. Cada estructura [SPropValue](spropvalue.md) incluido en el parámetro _lpRecipList_ debe asignarse por separado mediante el uso de las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) para que se puede liberar de forma individual. 
  
Para obtener información sobre PT_ERROR, vea [Tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Recursos adicionales



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

