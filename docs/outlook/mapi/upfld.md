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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360483"
---
# <a name="upfld"></a>UPFLD

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar una carpeta durante el estado de [carga](upload-folder-state.md)de la carpeta.
  
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
  
>  [salida]/[in] Flags para determinar las acciones adecuadas para uplaod. 
    
  - UPF_NEW
    
    - contempla La carpeta es nueva.
    
  - UPF_MOD_PARENT
    
    - contempla La carpeta se ha movido.
    
  - UPF_MOD_PROPS
    
    - contempla Las propiedades de la carpeta se han modificado.
    
  - UPF_DEL
    
    - contempla Se ha eliminado la carpeta.
    
  - UPF_OK
    
    - a La carga se realizó correctamente. El cliente lo establece después de cargar la información de la carpeta en el servidor.
    
_pfld_
  
> contempla Objeto Folder abierto que se va a cargar.
    
_feid_
  
> [salida] Id. de entrada de la carpeta.
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md) 
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

