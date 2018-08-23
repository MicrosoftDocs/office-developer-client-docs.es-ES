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
ms.openlocfilehash: 8540176b7675917dde7c618c40142605e9622282
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586224"
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
  
> Máscara de bits de indicadores que proporcionan información que describe el objeto. Solo el primer byte de los indicadores, **abFlags [0]**, se puede establecer por el proveedor; los otros tres están reservados. Estos marcadores no se deben establecer para los identificadores de entrada permanente; sólo se establecen para los identificadores de entrada a corto plazo. A los clientes, esta estructura es de sólo lectura. Las siguientes marcas se pueden establecer en **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> El identificador de entrada no se puede usar como un destinatario de un mensaje.
    
MAPI_NOTRESERVED 
  
> Otros usuarios no pueden obtener acceso al identificador de entrada.
    
MAPI_NOW 
  
> El identificador de entrada no se puede usar en otros momentos.
    
MAPI_SHORTTERM 
  
> El identificador de entrada es a corto plazo. Todos los otros valores de este byte deben estar establecidos a menos que se habilitan otros usos del identificador de entrada.
    
MAPI_THISSESSION 
  
> El identificador de entrada no se puede usar en otras sesiones.
    
 **AB**
  
> Indica una matriz de datos binarios que se usan en los proveedores de servicios. La aplicación cliente no puede utilizar esta matriz.
    
## <a name="remarks"></a>Comentarios

Se utiliza la estructura de la **propiedad ENTRYID** por mensaje almacenar y proveedores para construir identificadores únicos para sus objetos de la libreta de direcciones. Los identificadores de entrada se utilizan para identificar los siguientes tipos de objetos: 
  
- Almacenes de mensajes
    
- Folders
    
- Mensajes
    
- Contenedores de libretas de direcciones
    
- Listas de distribución
    
- Los usuarios de mensajería
    
- Objetos de estado
    
- Secciones del perfil
    
Cada proveedor usa un formato para la estructura de la **propiedad ENTRYID** que tenga sentido para ese proveedor. 
  
Los identificadores de entrada no pueden compararse directamente porque un objeto puede estar representado por dos valores binarios distintos. Para determinar si dos identificadores de entrada representan el mismo objeto, llame al método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
Cuando un cliente llama a un método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar su identificador de entrada, el objeto devuelve el formulario más permanente del identificador de entrada. Un cliente puede comprobar que un identificador de entrada es a largo plazo mediante la comprobación de que ninguno de los indicadores se establecen en el primer byte del miembro **abFlags** . 
  
Cuando un cliente tiene acceso a un identificador de entrada a través de una columna de una tabla, más probable es que este identificador de entrada es a corto plazo en lugar de a largo plazo. Los identificadores de entrada a corto plazo se pueden usar para abrir sus objetos correspondientes sólo en la sesión MAPI actual. Un cliente puede comprobar que un identificador de entrada es a corto plazo mediante la comprobación de que todas las marcas se establecen en el primer byte del miembro **abFlags** . 
  
Algunos identificadores de entrada son a corto plazo, pero tienen un uso a largo plazo. Este tipo de identificador de entrada tendrá uno o varios de los indicadores adecuados establecidos en el primer byte de su miembro **abFlags** . 
  
Una estructura de la **propiedad ENTRYID** es similar a una estructura [FLATENTRY](flatentry.md) . Sin embargo, hay algunas diferencias: 
  
- Una estructura de la **propiedad ENTRYID** no almacena el tamaño del identificador de entrada; una estructura **FLATENTRY** lo hace. 
    
- Una estructura de **ENTRYID** almacena los datos de marca y el resto de los identificadores de entrada por separado; una estructura **FLATENTRY** almacena los datos de marca con el resto del identificador de entrada. 
    
- Una estructura de **ENTRYID** se pasa como parámetro a los métodos de la interfaz de [IMAPIProp](imapipropiunknown.md) y a los siguientes métodos de **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Una estructura de **ENTRYID** se usa para almacenar un identificador de entrada en el disco. Una estructura **FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o páselo en una secuencia de bytes. 
    
Los clientes siempre deben pasar los identificadores de entrada alineado con naturalidad. Aunque los proveedores deben administrar los identificadores de entrada arbitrariamente alineado, los clientes no deben esperar este comportamiento. Error al pasar un identificador de entrada alineadas buen a un método puede causar un error de alineación en procesadores RISC. 
  
El factor de alineación natural, normalmente de 8 bytes, es el tipo de datos más grande, compatible con la CPU y suele ser el mismo factor de alineación usado por el asignador de memoria del sistema. Una dirección de memoria con naturalidad alineado permite la CPU tener acceso a cualquier tipo de datos que admite en esa dirección sin que se genere un error de alineación. Para CPU RISC, un tipo de datos de tamaño N bytes debe normalmente se alinea en un múltiplo de N bytes, con la dirección que se va a un múltiplo de N.
  
Para obtener más información, vea [Identificadores de entrada](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Recursos adicionales



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propiedad canónica PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Estructuras MAPI](mapi-structures.md)

