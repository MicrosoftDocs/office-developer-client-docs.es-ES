---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431361"
---
# <a name="upfld"></a>UPFLD

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar una carpeta durante el estado [de carga de la carpeta.](upload-folder-state.md)
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a>Miembros

_ulFlags_
  
>  [out]/[in] Marcas para determinar las acciones apropiadas para el uplaod. 
    
  - UPF_NEW
    
    - [salida] La carpeta es nueva.
    
  - UPF_MOD_PARENT
    
    - [salida] Se ha movido la carpeta.
    
  - UPF_MOD_PROPS
    
    - [salida] Se han modificado las propiedades de carpeta.
    
  - UPF_DEL
    
    - [salida] Se eliminó la carpeta.
    
  - UPF_OK
    
    - [entrada] La carga se ha realizado correctamente. El cliente establece esto después de cargar la información de la carpeta en el servidor.
    
_pfld_
  
> [salida] Objeto de carpeta abierta que se debe cargar.
    
_feid_
  
> [salida] Id. de entrada de la carpeta.
    
## <a name="see-also"></a>Consulte también

- [Información sobre la API de replicación](about-the-replication-api.md) 
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

