---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438116"
---
# <a name="uptbl"></a>UPTBL

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar el contenido de una carpeta durante el estado [de la tabla de carga.](upload-table-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a>Miembros

_ulFlags_
  
> [entrada] Marcas para determinar el comportamiento adecuado durante la carga.
    
  - UPT_OK
    
    - [entrada] La carga se ha realizado correctamente. El cliente establece esto después de cargar el contenido de la carpeta en el servidor.
    
_pstmReserved_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pszName_
  
> [salida] Nombre de la carpeta.
    
_feid_
  
> [salida] Id. de entrada de la carpeta.
    
_uintReserved_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_rgte_
  
> [salida] Estructura que contiene la siguiente información para los elementos normales (o no ocultos) y los elementos asociados (u ocultos) de la carpeta:  _rgte[0]_ es para los elementos normales y  _rgte[1]_ es para los elementos asociados. 
    
   - el número de elementos nuevos o modificados
   - el número de elementos leídos 
   - el número de elementos eliminados
    
 _iEnt_
  
> [salida] Índice para realizar un seguimiento de la carga del número de cambios especificados por  _cEnt_.
    
_cEnt_
  
> [salida] Número de cambios en la carpeta.
    
_movHead_
  
> [salida] Cadena de [estructuras UPMOV.](upmov.md) 
    
_pReserved_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible.
    
## <a name="see-also"></a>Consulte también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPTBLE](uptble.md)

