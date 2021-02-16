---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424885"
---
# <a name="updele"></a>UPDELE

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información ampliada para los elementos que se han eliminado en un almacén local. Esta información se usa durante el estado [de eliminación de carga.](upload-delete-status-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a>Miembros

_ulFlags_
  
> [out]/[in] Marcas para determinar el comportamiento apropiado durante la carga.
    
  - UPD_ASSOC
    
    - [salida] El elemento está asociado.
    
  - UPD_MOV
    
    - [salida] El elemento se movió.
    
  - UPD_OK 
    
    - [entrada] La carga se ha realizado correctamente. El cliente establece esto después de cargar información en el servidor.
    
  - UPD_MOVED
    
    - [entrada] El elemento se movió correctamente.
    
  - UPD_UPDATE
    
    - [entrada] Marca el elemento de origen como modificado.
    
  - UPD_COMMIT
    
    - [entrada] Confirmar el estado de carga ahora (entrada 0).
    
_skey_
  
> [salida] Clave de origen del elemento.
    
_dwReserved_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible.
    
_binChg_
  
> [salida] Cambiar la clave del elemento de destino si se ha movido el elemento.
    
_binPcl_
  
> [salida] Cambiar la lista del elemento de destino si se ha movido el elemento.
    
_skeyDst_
  
> [salida] Clave de origen del elemento de destino si se ha movido el elemento.
    
_mov_
  
> [salida] Información de la carpeta de destino si se ha movido el elemento.
    
## <a name="see-also"></a>Consulte también

- [Información sobre la API de replicación](about-the-replication-api.md) 
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

