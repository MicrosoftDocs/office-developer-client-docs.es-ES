---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315991"
---
# <a name="entryid"></a>ENTRYID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de entrada para un objeto MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Máscara de máscara de los marcadores que proporcionan información que describe el objeto. El proveedor solo puede establecer el primer byte de las marcas, **abFlags [0]**; los otros tres están reservados. Estas marcas no deben establecerse para los identificadores de entrada permanentes; solo se establecen para los identificadores de entrada a corto plazo. Para los clientes, esta estructura es de solo lectura. Se pueden establecer los siguientes indicadores en **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> El identificador de entrada no puede usarse como un destinatario en un mensaje.
    
MAPI_NOTRESERVED 
  
> Otros usuarios no pueden tener acceso al identificador de entrada.
    
MAPI_NOW 
  
> El identificador de entrada no se puede usar en otros momentos.
    
MAPI_SHORTTERM 
  
> El identificador de entrada es a corto plazo. Se deben establecer todos los demás valores de este byte, a menos que estén habilitados otros usos del identificador de entrada.
    
MAPI_THISSESSION 
  
> El identificador de entrada no se puede usar en otras sesiones.
    
 **listín**
  
> Indica una matriz de datos binarios que usan los proveedores de servicios. La aplicación cliente no puede usar esta matriz.
    
## <a name="remarks"></a>Comentarios

El almacén de mensajes y los proveedores de libreta de direcciones usan la estructura **EntryID** para crear identificadores únicos para sus objetos. Los identificadores de entrada se usan para identificar los siguientes tipos de objetos: 
  
- Almacenes de mensajes
    
- Folders
    
- Mensajes
    
- Contenedores de libretas de direcciones
    
- Listas de distribución
    
- Usuarios de mensajería
    
- Objetos de estado
    
- Secciones de perfil
    
Cada proveedor utiliza un formato para la estructura **EntryID** que tiene sentido para ese proveedor. 
  
Los identificadores de entrada no pueden compararse directamente porque un objeto puede estar representado por dos valores binarios distintos. Para determinar si dos identificadores de entrada representan el mismo objeto, llame al método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) . 
  
Cuando un cliente llama al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto para recuperar su identificador de entrada, el objeto devuelve la forma más permanente del identificador de entrada. Un cliente puede comprobar que un identificador de entrada es de largo plazo comprobando que ninguno de los indicadores está establecido en el primer byte del miembro **abFlags** . 
  
Cuando un cliente obtiene acceso a un identificador de entrada a través de una columna de una tabla, lo más probable es que este identificador de entrada sea a corto plazo en lugar de largo plazo. Los identificadores de entrada a corto plazo pueden usarse para abrir sus objetos correspondientes sólo en la sesión MAPI actual. Un cliente puede comprobar que un identificador de entrada es de corto plazo comprobando que todas las marcas se establecen en el primer byte del miembro **abFlags** . 
  
Algunos identificadores de entrada son a corto plazo, pero tienen un uso a largo plazo. Dicho identificador de entrada tendrá uno o más de los indicadores adecuados establecidos en el primer byte de su miembro **abFlags** . 
  
Una estructura **EntryID** se asemeja a una estructura [FLATENTRY](flatentry.md) . Sin embargo, hay algunas diferencias: 
  
- Una estructura **EntryID** no almacena el tamaño del identificador de entrada; una estructura **FLATENTRY** . 
    
- Una estructura **EntryID** almacena los datos de la marca y el resto del identificador de entrada por separado; una estructura **FLATENTRY** almacena los datos de la marca con el resto del identificador de entrada. 
    
- Se pasa una estructura **EntryID** como parámetro a los métodos de la interfaz [IMAPIProp](imapipropiunknown.md) y a los siguientes métodos **OpenEntry** : [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [IMAPISupport:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [IMSLogon:: OpenEntry](imslogon-openentry.md)
    
- Se usa una estructura **EntryID** para almacenar un identificador de entrada en el disco. Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes. 
    
Los clientes siempre deben pasar los identificadores de entrada alineados naturalmente. Aunque los proveedores deben controlar los identificadores de entrada alineados arbitrariamente, los clientes no deben esperar este comportamiento. Si no se pasa un identificador de entrada con buena alineación a un método, se puede producir un error de alineación en los procesadores RISC. 
  
El factor de alineación natural, normalmente 8 bytes, es el tipo de datos más grande que admite la CPU y suele ser el mismo factor de alineación que usa el asignador de memoria del sistema. Una dirección de memoria muy alineada de forma natural permite que la CPU tenga acceso a cualquier tipo de datos que admite en esa dirección sin generar un error de alineación. Para las CPU RISC, el tipo de datos de N bytes de tamaño debe estar alineado normalmente en un múltiplo par de N bytes, donde la dirección es un múltiplo par de N.
  
Para obtener más información, consulte identificadores de [entrada](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Vea también



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propiedad canónica PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

