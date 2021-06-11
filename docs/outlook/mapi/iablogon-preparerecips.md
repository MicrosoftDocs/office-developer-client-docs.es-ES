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
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423863"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara una lista de destinatarios para su uso posterior por el sistema de mensajería.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

_ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de texto de las cadenas devueltas. Se puede establecer la siguiente marca:
    
  - MAPI_CACHE_ONLY: use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Esta marca solo es compatible con el Exchange libreta de direcciones.
    
_lpPropTagArray_
  
> [in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indican las propiedades que requieren actualización, si las hay. El  _parámetro lpPropTagArray_ puede ser NULL. 
    
_lpRecipList_
  
> [in] Puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios se preparó correctamente.
    
MAPI_E_NOT_FOUND 
  
> Uno o varios de los destinatarios del parámetro  _lpRecipList_ no existen. 
    
## <a name="return-value"></a>Valor devuelto

Un cliente llama al método [MAPI IAddrBook::P repareRecips](iaddrbook-preparerecips.md) para modificar o reorganizar un conjunto de propiedades para uno o varios destinatarios. Los destinatarios pueden o no formar parte de la lista de destinatarios de un mensaje saliente. MAPI transfiere esta llamada al método **IABLogon::P repareRecips** de un proveedor de libreta de direcciones. 
  
**IABLogon::P repareRecips** realiza cuatro tareas principales: 
  
- Garantiza que todos los destinatarios de la lista de direcciones a los que apunta el parámetro  _lpRecipList_ tengan un identificador de entrada a largo plazo. 
    
- Garantiza que todos los destinatarios tengan las propiedades especificadas en la matriz de valores de propiedad a la que apunta el _parámetro lpPropTagArray._ 
    
- Garantiza que las propiedades de la matriz de valores de propiedad aparezcan antes que cualquier otra propiedad que existiera antes de la llamada.
    
- Garantiza que el orden de las propiedades de la estructura [ADRENTRY](adrentry.md) de cada destinatario en la estructura **ADRLIST** sea el mismo que en la matriz de valores de propiedad. 
    
La **estructura ADRENTRY** del parámetro  _lpRecipList_ contiene una **estructura ADRENTRY** para cada destinatario. Cada **estructura ADRENTRY** contiene una matriz de [estructuras SPropValue](spropvalue.md) para describir las propiedades del destinatario. Cuando **devuelve IABLogon::P repareRecips,** la matriz de estructura **SPropValue** para cada destinatario incluye las propiedades de  _lpPropTagArray_ seguidas de las demás propiedades del destinatario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de **IABLogon::P repareRecips** implica poner propiedades en un orden específico, recuperar valores de propiedad y convertir identificadores de entrada a corto plazo en identificadores de entrada a largo plazo. Las propiedades que se solicitan en el parámetro _lpPropTagArray_ deben estar al principio de la matriz de valores de propiedad asociada con la estructura **ADRENTRY** de cada destinatario en el _parámetro lpRecipList._ Si los valores de estas propiedades no existen, abra la lista de distribución o el usuario de mensajería asociado mediante su identificador de entrada y recupere los valores de propiedad que faltan. 
  
Asigne cada **estructura SPropValue** pasada en  _lpRecipList_ por separado para que las estructuras se puedan liberar individualmente. Si debe asignar espacio adicional para cualquier estructura **SPropValue,** por ejemplo, para almacenar los datos de una propiedad de cadena, use la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar espacio adicional para la matriz de valores de propiedad completa. Use la [función MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de valores de propiedad original y, a continuación, use la [función MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional que sea necesaria. 
  
Para implementar **IABLogon::P repareRecips**, use el siguiente procedimiento:
  
1. Compruebe si hay entradas en el _parámetro lpPropTagArray._ Si la matriz de valores de propiedad está vacía, no hay trabajo que hacer. Devuelve un valor correcto. 
    
2. Procese cada destinatario en el _parámetro lpRecipList._ Hay un miembro **de la estructura ADRENTRY** para cada destinatario de la lista. Ignore los siguientes tipos de destinatarios: 
    
   - Destinatarios sin identificador de entrada en el **miembro rgPropVals** de su estructura **ADRENTRY** (es decir, destinatarios sin resolver). 
    
   - Destinatarios con un identificador de entrada que no pertenece a su proveedor. Estos destinatarios se pasarán a otro proveedor de libreta de direcciones.
    
3. Abra el destinatario y recupere las propiedades que ya están establecidas para el destinatario.
    
4. Combine la matriz de valores de propiedad especificada en  _lpRecipList_ con la matriz de propiedades devueltas de **GetProps**. Si se produce la misma propiedad en ambas matrices de propiedades, use el valor de  _lpRecipList_.
    
5. Si la matriz de valores de propiedad  _lpRecipList_ es lo suficientemente grande como para contener todas las propiedades necesarias, simplemente reemplázcala por la matriz combinada. Si la matriz de valores de propiedad  _lpRecipList_ no es lo suficientemente grande, reemplázcala por una matriz recién asignada. Asegúrese de que la nueva matriz tiene un valor actualizado en cada uno de sus **miembros de cValues.** 
    
6. Si no reconoce una o varias de las propiedades del parámetro  _lpPropTagArray,_ establezca el tipo de propiedad en la estructura **ADRENTRY** del destinatario en PT_ERROR y el valor de la propiedad en MAPI_E_NOT_FOUND o en otro valor que dé una razón más específica para la indisponibilidad de la propiedad. Para obtener información sobre PT_ERROR, vea [Tipos de propiedad](property-types.md).
    
> [!NOTE]
> Nunca volver a la estructura **ADRLIST** que se pasa a **IABLogon::P repareRecips** o cambiar su número de entradas. 
  
## <a name="see-also"></a>Vea también

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

