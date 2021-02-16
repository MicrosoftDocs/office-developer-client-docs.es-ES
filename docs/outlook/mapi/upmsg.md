---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427272"
---
# <a name="upmsg"></a>UPMSG

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar un elemento de Outlook durante el estado [del mensaje de carga.](upload-message-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a>Miembros

 _ulFlags_
  
> [out]/[in] Marcas para determinar el comportamiento adecuado durante la carga. 
    
  - UPM_ASSOC
    
    - [salida] El elemento está asociado.
    
  - UPM_NEW
    
    - [salida] Nuevo elemento. 
    
  - UPM_MOV
    
    - [salida] El elemento se movió aquí.
    
  - UPM_MOD_PROPS
    
    - [salida] Se modificaron las propiedades del elemento.
    
  - UPM_HEADER
    
    - [salida] El elemento es un encabezado de mensaje.
    
  - UPM_OK
    
    - [entrada] La carga se ha realizado correctamente. El cliente establece esto después de cargar información en el servidor.
    
  - UPM_MOVED
    
    - [entrada] El elemento se movió correctamente.
    
  - UPM_COMMIT
    
    - [entrada] Confirma el estado de carga ahora.
    
  - UPM_DELETE
    
    - [entrada] Eliminar elemento ahora.
    
  - UPM_SAVE
    
    - [entrada] Guarde los cambios en el elemento.
    
_pmsg_
  
> [salida] Abrir objeto de elemento. Vea mapidefs.h para obtener la definición de tipo **de LPMESSAGE**. 
    
_meid_
  
> [salida] Identificador de entrada del elemento.
    
_binReserved1_
  
> [entrada] Este miembro está reservado para el uso interno de Outlook y no es compatible. 
    
_binReserved2_
  
> [entrada] Este miembro está reservado para el uso interno de Outlook y no es compatible. 
    
_feid_
  
> [salida] Identificador de entrada de la carpeta de origen, si se movió el elemento.
    
_binChg_
  
> [salida] Cambiar la clave del elemento de destino, si se movió el elemento. Vea mapidefs.h para obtener la definición de tipo **de SBinary**. 
    
_binPcl_
  
> [salida] Cambiar la lista del elemento de destino, si se movió el elemento. Vea mapidefs.h para obtener la definición de tipo **de SBinary**. 
    
_skeySrc_
  
> [salida] Clave de origen del elemento de origen, si se movió el elemento.
    
## <a name="see-also"></a>Consulte también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

