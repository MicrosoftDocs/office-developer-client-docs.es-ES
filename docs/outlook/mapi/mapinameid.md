---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411683"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una propiedad con nombre. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a>Members

 **lpguid**
  
> Puntero a una [estructura GUID](guid.md) que define un conjunto de propiedades determinado; este miembro no puede ser NULL. Los valores válidos son los siguientes: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Un valor definido por el cliente
  
> 
    
 **ulKind**
  
> Valor que describe el tipo de valor en el **miembro Kind.** Los valores válidos son los siguientes: 
    
MNID_ID 
  
> El **miembro Kind** contiene un valor entero que representa el nombre de la propiedad. 
    
MNID_STRING 
  
> El **miembro Kind** contiene una cadena de caracteres Unicode que representa el nombre de la propiedad. 
    
 **Kind**
  
> Union que describe el nombre de la propiedad con nombre. El nombre puede ser un valor entero, almacenado en **lID** o una cadena de caracteres Unicode, almacenado en **lpwstrName**.
    
## <a name="remarks"></a>Comentarios

La **estructura MAPINAMEID** se usa para describir propiedades con nombre que tienen identificadores en 0x8000. Un conjunto de propiedades es una parte importante de una propiedad con nombre. Por ejemplo PS_PUBLIC_STRINGS o PS_ROUTING_ADDRTYPE son conjuntos de propiedades definidos por MAPI. 
  
Las propiedades con nombre permiten a los clientes definir propiedades personalizadas en un espacio de nombres más grande del que está disponible en el intervalo de identificadores de propiedades definido por MAPI. Los nombres de propiedad no se pueden usar para obtener los valores de propiedad directamente; primero deben asignarse a identificadores de propiedades mediante el método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Para objetos concretos, como mensajes, MAPI reserva un intervalo de identificadores de propiedad para propiedades personalizadas. Por lo tanto, para estos objetos, los clientes no tienen que usar propiedades con nombre y pueden guardar la sobrecarga asociada. 
  
Para obtener más información acerca de las propiedades con nombre, vea [Named Properties](mapi-named-properties.md).
  
## <a name="see-also"></a>Vea también



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Estructuras MAPI](mapi-structures.md)

