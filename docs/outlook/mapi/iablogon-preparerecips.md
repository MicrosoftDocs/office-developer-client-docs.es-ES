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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348947"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara una lista de destinatarios para su uso posterior por parte del sistema de mensajería.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

_ulFlags_
  
> a Máscara de máscara de marcadores que controla el tipo de texto en las cadenas devueltas. Se puede establecer la siguiente marca:
    
  - MAPI_CACHE_ONLY: Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres. Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor. Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.
    
_lpPropTagArray_
  
> a Un puntero a una estructura [SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedades que indican las propiedades que requieren actualización, si las hay. El parámetro _lpPropTagArray_ puede ser null. 
    
_lpRecipList_
  
> a Un puntero a una estructura [ADRLIST](adrlist.md) que contiene la lista de destinatarios. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La lista de destinatarios se ha preparado correctamente.
    
MAPI_E_NOT_FOUND 
  
> Uno o más de los destinatarios en el parámetro _lpRecipList_ no existe. 
    
## <a name="return-value"></a>Valor devuelto

Un cliente llama al método [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) para modificar o reorganizar un conjunto de propiedades para uno o más destinatarios. Es posible que los destinatarios no formen parte de la lista de destinatarios de un mensaje saliente. MAPI transfiere esta llamada a un método **IABLogon::P reparerecips** del proveedor de la libreta de direcciones. 
  
**IABLogon::P reparerecips** realiza cuatro tareas principales: 
  
- Garantiza que todos los destinatarios de la lista de direcciones a la que apunta el parámetro _lpRecipList_ tienen un identificador de entrada a largo plazo. 
    
- Garantiza que todos los destinatarios tienen las propiedades especificadas en la matriz de valores de propiedad a la que señala el parámetro _lpPropTagArray_ . 
    
- Garantiza que las propiedades de la matriz de valores de propiedad aparecen antes de cualquier otra propiedad que existía antes de la llamada.
    
- Garantiza que el orden de las propiedades de la estructura [ADRENTRY](adrentry.md) de cada destinatario en la estructura **ADRLIST** es el mismo que en la matriz de valores de propiedad. 
    
La estructura **ADRENTRY** del parámetro _lpRecipList_ contiene una estructura **ADRENTRY** para cada destinatario. Cada estructura **ADRENTRY** contiene una matriz de estructuras [SPropValue](spropvalue.md) para describir las propiedades del destinatario. Cuando **IABLogon::P reparerecips** devuelve, la matriz de estructura **SPropValue** para cada destinatario incluye las propiedades de la _lpPropTagArray_ seguida de las otras propiedades del destinatario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Implementar **IABLogon::P reparerecips** implica colocar propiedades en un orden específico, recuperar valores de propiedad y convertir los identificadores de entrada a corto plazo en identificadores de entrada a largo plazo. Las propiedades que se solicitan en el parámetro _lpPropTagArray_ deben estar al principio de la matriz de valores de propiedad asociada a la estructura **ADRENTRY** de cada destinatario en el parámetro _lpRecipList_ . Si no existen los valores de estas propiedades, abra el usuario de mensajería o la lista de distribución asociada mediante su identificador de entrada y recupere los valores de propiedad que faltan. 
  
Asigne cada estructura **SPropValue** pasada en _lpRecipList_ por separado para que las estructuras puedan liberarse de forma individual. Si tiene que asignar espacio adicional para cualquier estructura de **SPropValue** , por ejemplo, para almacenar los datos de una propiedad de cadena, use la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar espacio adicional para la matriz de valores de propiedad completa. Use la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de valores de propiedad originales y, a continuación, use la función [MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional que sea necesaria. 
  
Para implementar **IABLogon::P reparerecips**, use el procedimiento siguiente:
  
1. Compruebe las entradas en el parámetro _lpPropTagArray_ . Si la matriz de valores de propiedad está vacía, no hay trabajo por hacer. Devolver un valor correcto. 
    
2. Procese cada uno de los destinatarios en el parámetro _lpRecipList_ . Hay un miembro de estructura **ADRENTRY** para cada destinatario de la lista. Ignore los siguientes tipos de destinatarios: 
    
   - Los destinatarios sin un identificador de entrada en el miembro **rgPropVals** de su estructura **ADRENTRY** (es decir, los destinatarios sin resolver). 
    
   - Destinatarios con un identificador de entrada que no pertenece a su proveedor. Estos destinatarios se pasarán a otro proveedor de libreta de direcciones.
    
3. Abra el destinatario y recupere las propiedades que ya están establecidas para el destinatario.
    
4. Combina la matriz de valores de propiedad especificada en _lpRecipList_ con la matriz de propiedades devuelta desde **GetProps**. Si la misma propiedad se produce en ambas matrices de propiedades, use el valor de _lpRecipList_.
    
5. Si la matriz de valores de la propiedad _lpRecipList_ es lo suficientemente grande como para contener todas las propiedades necesarias, simplemente reemplácela por la matriz combinada. Si la matriz de valores de propiedad _lpRecipList_ no es lo suficientemente grande, reemplácela por una matriz recién asignada. Asegúrese de que la nueva matriz tiene un valor actualizado en cada uno de sus miembros **cValues** . 
    
6. Si no reconoce una o varias propiedades en el parámetro _lpPropTagArray_ , establezca el tipo de propiedad en la estructura **ADRENTRY** del destinatario en PT_ERROR y el valor de la propiedad en MAPI_E_NOT_FOUND o en otro valor que proporcione más razón específica para la no disponibilidad de la propiedad. Para obtener información sobre PT_ERROR, vea [tipos de propiedades](property-types.md).
    
> [!NOTE]
> No reasigne nunca la estructura **ADRLIST** que se pasa a **IABLogon::P reparerecips** o cambie el número de entradas. 
  
## <a name="see-also"></a>Vea también

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propiedad canónica PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

