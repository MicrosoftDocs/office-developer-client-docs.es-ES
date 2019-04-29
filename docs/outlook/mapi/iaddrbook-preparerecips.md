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
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414280"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara una lista de destinatarios para su uso posterior por parte del sistema de mensajería. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre la entrada. Se puede establecer la siguiente marca:
    
MAPI_CACHE_ONLY
  
> Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo de intercambio en caché y obtenga acceso a una entrada de dicha libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
 _lpSPropTagArray_
  
> a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedades que indican las propiedades, si las hay, que requieren actualización. El parámetro _lpSPropTagArray_ puede ser null. 
    
 _lpRecipList_
  
> a Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios se ha preparado correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes y los proveedores de servicios llaman al método **PrepareRecips** para hacer lo siguiente: 
  
- Asegúrese de que todos los destinatarios del parámetro _lpRecipList_ tienen identificadores de entrada a largo plazo. 
    
- Asegúrese de que cada uno de los destinatarios del parámetro _lpRecipList_ tiene las propiedades enumeradas en el parámetro _lpSPropTagArray_ y que estas propiedades aparecen al principio de la lista de destinatarios. 
    
MAPI convierte los identificadores de entrada a corto plazo de cada destinatario en identificadores de entrada a largo plazo. Si es necesario, los identificadores de entrada a largo plazo de los destinatarios se recuperan del proveedor de libreta de direcciones adecuado y se solicitan propiedades adicionales.
  
En una entrada de destinatario individual, las propiedades solicitadas se ordenan primero, seguidas de las propiedades que ya estaban presentes para la entrada. Si una o varias de las propiedades solicitadas en el parámetro _lpSPropTagArray_ no están controladas por el proveedor de libreta de direcciones adecuado, sus tipos de propiedad se establecerán en PT_ERROR. Sus valores de propiedad se establecerán en MAPI_E_NOT_FOUND o en otro valor que proporcione una razón más específica por la que las propiedades no están disponibles. Cada estructura [SPropValue](spropvalue.md) incluida en el parámetro _lpRecipList_ debe asignarse por separado mediante las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) , de modo que se pueda liberar de forma individual. 
  
Para obtener información sobre PT_ERROR, vea [tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Ver también



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

