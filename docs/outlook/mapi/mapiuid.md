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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432208"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Versión independiente de ordenación de bytes de una estructura [GUID](guid.md) que se usa para identificar de forma exclusiva a un proveedor de servicios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Macro relacionada:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **listín**
  
> Matriz que contiene un identificador de 16 bytes.
    
## <a name="remarks"></a>Comentarios

Una estructura **MAPIUID** es una estructura **GUID** que se coloca en el orden de bytes del procesador Intel ®. 
  
MAPI crea estructuras **MAPIUID** de una forma que hace que sea muy raro que dos elementos distintos tengan el mismo identificador. Las estructuras **MAPIUID** se pueden almacenar como propiedades binarias o como archivos, sin tener en cuenta el orden de bytes del almacenamiento de los equipos o el acceso a la información. 
  
 Las estructuras **MAPIUID** se usan: 
  
- Para identificar una sección de perfil.
    
- En los identificadores de entrada de los objetos de la libreta de direcciones y del almacén de mensajes para identificar al proveedor de servicios responsable.
    
- En la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de los mensajes.
    
Para generar un identificador de **MAPIUID** para una clave de búsqueda, los proveedores de servicios llaman a [IMAPISupport:: NewUID](imapisupport-newuid.md).
  
Cuando un cliente transmite un mensaje a través de una red, debe usar un protocolo o formato de transmisión que no cambia el orden de los bytes de los datos de **MAPIUID** . 
  
Para obtener más información acerca de cómo se usan las estructuras de **MAPIUID** , consulte los siguientes temas: 
  
[Registro de identificadores únicos del proveedor de servicios](registering-service-provider-unique-identifiers.md)
  
[Establecer el orden de transporte](setting-transport-order.md)
  
## <a name="see-also"></a>Ver también



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Estructuras MAPI](mapi-structures.md)

