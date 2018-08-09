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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818252"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Hace referencia a**: Outlook 
  
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
  
> Establece el puntero a una estructura [GUID](guid.md) definición de una propiedad determinada; Este miembro no puede ser NULL. Los valores válidos son los siguientes: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Un valor definido por el cliente
  
> 
    
 **ulKind**
  
> Valor que describe el tipo de valor en el miembro de **tipo** . Los valores válidos son los siguientes: 
    
MNID_ID 
  
> El miembro de **tipo** contiene un valor entero que representa el nombre de la propiedad. 
    
MNID_STRING 
  
> El **tipo** de miembro contiene una cadena de caracteres Unicode que representa el nombre de la propiedad. 
    
 **Clase**
  
> Unión que describe el nombre de la propiedad con nombre. El nombre puede ser un valor entero, que se almacenan en **tapa**, o una cadena de caracteres Unicode, que se almacenan en **lpwstrName**.
    
## <a name="remarks"></a>Comentarios

La estructura **MAPINAMEID** se usa para describir las propiedades de las propiedades con nombre que tienen identificadores más 0 x 8000. Un conjunto de propiedades es una parte importante de una propiedad con nombre. Por ejemplo PS_PUBLIC_STRINGS o PS_ROUTING_ADDRTYPE son conjuntos de propiedades definidos por MAPI. 
  
Propiedades con nombre que los clientes puedan definir propiedades personalizadas en un espacio de nombres más grande que se encuentra disponible en el intervalo de identificadores de propiedad definida por el de MAPI. Los nombres de propiedad no se puede usar para obtener los valores de propiedad directamente; que deben en primer lugar se asignadas a identificadores de propiedad a través del método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . De determinados objetos, como mensajes, MAPI reserva un intervalo de identificadores de propiedad para las propiedades personalizadas. Por lo tanto, para estos objetos, los clientes no es necesario usar propiedades con nombre y puede guardar el asociado sobrecarga. 
  
Para obtener más información acerca de las propiedades con nombre, vea [Las propiedades con nombre](mapi-named-properties.md).
  
## <a name="see-also"></a>Vea también



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Estructuras MAPI](mapi-structures.md)

