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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415274"
---
# <a name="entryid"></a>ENTRYID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de entrada para un objeto MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
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
  
> Máscara de bits de marcas que proporcionan información que describe el objeto. Solo el proveedor puede establecer el primer byte de las marcas, **abFlags[0];** las otras tres están reservadas. Estas marcas no deben establecerse para identificadores de entrada permanentes; solo se establecen para identificadores de entrada a corto plazo. Para los clientes, esta estructura es de solo lectura. Las siguientes marcas se pueden establecer en **abFlags[0]**:
    
MAPI_NOTRECIP 
  
> El identificador de entrada no se puede usar como destinatario en un mensaje.
    
MAPI_NOTRESERVED 
  
> Otros usuarios no pueden tener acceso al identificador de entrada.
    
MAPI_NOW 
  
> El identificador de entrada no se puede usar en otras ocasiones.
    
MAPI_SHORTTERM 
  
> El identificador de entrada es a corto plazo. Todos los demás valores de este byte deben establecerse a menos que se habiliten otros usos del identificador de entrada.
    
MAPI_THISSESSION 
  
> El identificador de entrada no se puede usar en otras sesiones.
    
 **ab**
  
> Indica una matriz de datos binarios que usan los proveedores de servicios. La aplicación cliente no puede usar esta matriz.
    
## <a name="remarks"></a>Comentarios

Los **proveedores de libretas** de direcciones y el almacén de mensajes usan la estructura ENTRYID para crear identificadores únicos para sus objetos. Los identificadores de entrada se usan para identificar los siguientes tipos de objetos: 
  
- Almacenes de mensajes
    
- Folders
    
- Mensajes
    
- Contenedores de libreta de direcciones
    
- Listas de distribución
    
- Usuarios de mensajería
    
- Objetos de estado
    
- Secciones de perfil
    
Cada proveedor usa un formato para la **estructura ENTRYID** que tiene sentido para ese proveedor. 
  
Los identificadores de entrada no pueden compararse directamente porque un objeto puede estar representado por dos valores binarios distintos. Para determinar si dos identificadores de entrada representan el mismo objeto, llame al [método IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md) 
  
Cuando un cliente llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de un objeto para recuperar su identificador de entrada, el objeto devuelve la forma más permanente del identificador de entrada. Un cliente puede comprobar que un identificador de entrada es a largo plazo comprobando que ninguna de las marcas se establece en el primer byte del **miembro abFlags.** 
  
Cuando un cliente tiene acceso a un identificador de entrada a través de una columna de una tabla, lo más probable es que este identificador de entrada sea a corto plazo en lugar de a largo plazo. Los identificadores de entrada a corto plazo se pueden usar para abrir sus objetos correspondientes solo en la sesión MAPI actual. Un cliente puede comprobar que un identificador de entrada es a corto plazo comprobando que todas las marcas están establecidas en el primer byte del **miembro abFlags.** 
  
Algunos identificadores de entrada son a corto plazo, pero tienen un uso a largo plazo. Dicho identificador de entrada tendrá una o varias de las marcas adecuadas establecidas en el primer byte de su **miembro abFlags.** 
  
Una **estructura ENTRYID** es similar a una [estructura FLATENTRY.](flatentry.md) Sin embargo, hay algunas diferencias: 
  
- Una **estructura ENTRYID** no almacena el tamaño del identificador de entrada; una **estructura FLATENTRY** sí. 
    
- Una **estructura ENTRYID** almacena los datos de la marca y el resto del identificador de entrada por separado; una **estructura FLATENTRY** almacena los datos de la marca con el resto del identificador de entrada. 
    
- Una estructura **ENTRYID** se pasa como parámetro a los métodos de la interfaz [IMAPIProp](imapipropiunknown.md) y a los siguientes métodos **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Se **usa una estructura ENTRYID** para almacenar un identificador de entrada en el disco. Una **estructura FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes. 
    
Los clientes siempre deben pasar identificadores de entrada alineados de forma natural. Aunque los proveedores deben controlar identificadores de entrada alineados arbitrariamente, los clientes no deben esperar este comportamiento. Si no se pasa un identificador de entrada bien alineado a un método, se puede producir un error de alineación en los procesadores RISC. 
  
El factor de alineación natural, normalmente 8 bytes, es el tipo de datos más grande admitido por la CPU y, por lo general, el mismo factor de alineación usado por el asignador de memoria del sistema. Una dirección de memoria alineada de forma natural permite que la CPU obtenga acceso a cualquier tipo de datos que admita en esa dirección sin generar un error de alineación. En el caso de las CPU RISC, un tipo de datos de tamaño N bytes normalmente debe alinearse en un múltiplo par de N bytes, siendo la dirección un múltiplo par de N.
  
Para obtener más información, vea [Entry Identifiers](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Vea también



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propiedad canónica PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

