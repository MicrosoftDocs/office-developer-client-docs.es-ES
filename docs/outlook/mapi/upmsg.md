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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338874"
---
# <a name="upmsg"></a>UPMSG

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar un elemento de Outlook durante el [Estado de carga del mensaje](upload-message-state.md).
  
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
  
> [salida]/[in] Flags para determinar el comportamiento adecuado durante la carga. 
    
  - UPM_ASSOC
    
    - contempla El elemento está asociado.
    
  - UPM_NEW
    
    - contempla Nuevo elemento. 
    
  - UPM_MOV
    
    - contempla El elemento se movió aquí.
    
  - UPM_MOD_PROPS
    
    - contempla Se modificaron las propiedades del elemento.
    
  - UPM_HEADER
    
    - contempla Item es un encabezado de mensaje.
    
  - UPM_OK
    
    - a La carga se realizó correctamente. El cliente lo establece después de cargar la información en el servidor.
    
  - UPM_MOVED
    
    - a El elemento se movió correctamente.
    
  - UPM_COMMIT
    
    - a Confirmar el estado de carga ahora.
    
  - UPM_DELETE
    
    - a Eliminar elemento ahora.
    
  - UPM_SAVE
    
    - a Guarde los cambios realizados en el elemento.
    
_PMSG_
  
> contempla Objeto de elemento abierto. Consulte mapidefs. h para obtener la definición de tipo de **LPMESSAGE**. 
    
_MEID_
  
> contempla IDENTIFICADOR de entrada del elemento.
    
_binReserved1_
  
> a Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_binReserved2_
  
> a Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_feid_
  
> contempla IDENTIFICADOR de entrada de la carpeta de origen, si se movió el elemento.
    
_binChg_
  
> contempla Cambiar la clave del elemento de destino, si se movió el elemento. Consulte mapidefs. h para obtener la definición de tipo de **SBinary**. 
    
_binPcl_
  
> contempla Cambiar la lista del elemento de destino, si se movió el elemento. Consulte mapidefs. h para obtener la definición de tipo de **SBinary**. 
    
_skeySrc_
  
> contempla Clave de origen del elemento de origen, si se movió el elemento.
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)
- [MEID](meid.md)
- [SKEY](skey.md)

