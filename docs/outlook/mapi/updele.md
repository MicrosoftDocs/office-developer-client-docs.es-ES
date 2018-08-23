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
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566589"
---
# <a name="updele"></a>UPDELE

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información extendida para los elementos que se han eliminado en un almacén local. Esta información se usa durante la [carga Eliminar estado](upload-delete-status-state.md).
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [out] o [in] indicadores para determinar el comportamiento adecuado durante la carga.
    
  - UPD_ASSOC
    
    - [out] Elemento está asociado.
    
  - UPD_MOV
    
    - [out] Elemento se ha movido.
    
  - UPD_OK 
    
    - [entrada] Carga fue correcta. El cliente establece esto después de cargar información al servidor.
    
  - UPD_MOVED
    
    - [entrada] Elemento se ha movido correctamente.
    
  - UPD_UPDATE
    
    - [entrada] Elemento de origen de marcar como modificado.
    
  - UPD_COMMIT
    
    - [entrada] Confirmar el estado de carga ahora (entrada de 0).
    
_SKEY_
  
> [out] Clave de origen del elemento.
    
_dwReservado_
  
> [out] Este miembro está reservado para el uso interno de Outlook y no se admite.
    
_binChg_
  
> [out] Cambiar la clave del elemento de destino si el elemento se ha movido.
    
_binPcl_
  
> [out] Cambiar la lista de elemento de destino si el elemento se ha movido.
    
_skeyDst_
  
> [out] Clave de origen del elemento de destino si el elemento se ha movido.
    
_pupmov_
  
> [out] Información de la carpeta de destino si el elemento se ha movido.
    
## <a name="see-also"></a>Recursos adicionales

- [Información sobre la API de replicación](about-the-replication-api.md) 
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [SKEY](skey.md)
- [UPDEL](updel.md)
- [UPMOV](upmov.md)

