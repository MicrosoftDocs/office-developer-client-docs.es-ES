---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818294"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Se aplica a**: Outlook 
  
Una versión independiente de orden de bytes de una estructura [GUID](guid.md) que se utiliza para identificar de forma única un proveedor de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macro relacionado:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Miembros

 **AB**
  
> Una matriz que contiene un identificador de 16 bytes.
    
## <a name="remarks"></a>Notas

Una estructura **MAPIUID** es una estructura **GUID** poner en orden de bytes del procesador de Intel®. 
  
MAPI crea **MAPIUID** estructuras de una manera que hace que sea muy raro que dos elementos diferentes que tienen el mismo identificador. Estructuras **MAPIUID** pueden almacenarse como propiedades binarias o como archivos, sin tener en cuenta el orden de bytes del equipo almacenar y acceder a la información. 
  
 Se usan las estructuras **MAPIUID** : 
  
- Para identificar una sección de perfil.
    
- En la entrada de identificadores de mensaje de almacenan y objetos de la libreta para identificar el proveedor de servicio responsable de direcciones.
    
- En la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de los mensajes.
    
Para generar un identificador **MAPIUID** para una clave de búsqueda, proveedores de servicios de llamar a [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Cuando un cliente transmite un mensaje a través de una red, debe utilizar un formato de transmisión o de protocolo que no cambia el orden de bytes de datos **MAPIUID** . 
  
Para obtener más información acerca de cómo se usan las estructuras **MAPIUID** , consulte los temas siguientes: 
  
[Registrar identificadores únicos de proveedor de servicio](registering-service-provider-unique-identifiers.md)
  
[Establecer el orden de transporte](setting-transport-order.md)
  
## <a name="see-also"></a>Ver también



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Estructuras MAPI](mapi-structures.md)

