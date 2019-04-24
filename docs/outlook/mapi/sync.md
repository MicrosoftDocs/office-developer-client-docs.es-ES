---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349598"
---
# <a name="sync"></a>SYNC

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para iniciar la sincronización entre un almacén local y un servidor. Esta información se usa durante el [Estado Synchronize](synchronize-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a>Miembros

 _ulFlags_
  
- [salida]/[in] una máscara de máscara de los siguientes indicadores que modifica el comportamiento durante la sincronización:
    
- UPS_UPLOAD_ONLY
    
  - a El cliente solo realizará la carga. Outlook solo devuelve las carpetas modificadas localmente.
    
- UPS_DNLOAD_ONLY
    
  - a El cliente solo va a realizar la descarga. Outlook no debe borrar los bits de carga de las carpetas.
    
- UPS_THESE_FOLDERS
    
  - a El cliente va a sincronizar un conjunto de carpetas especificado con los identificadores de entrada proporcionados. Esta marca se puede combinar con la marca **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY** . 
    
- UPS_OK
    
  - contempla La sincronización se realizó correctamente. El cliente lo establece después de la carga o se completa una sincronización completa.
    
- 
    
    > [!NOTE]
    > Aunque el cliente puede cargar o sincronizar completamente (cargar y luego descargar) carpetas y elementos con la API de replicación, el cliente especifica *ulFlags* con una sola dirección de la replicación a la vez, ya sea el **UPS_UPLOAD_ONLY** o Marca **UPS_DNLOAD_ONLY** . En el caso de una sincronización completa, el cliente primero realiza una carga con la marca **UPS_UPLOAD_ONLY** y, a continuación, una descarga con la marca **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- contempla Ruta de acceso al almacén local.
    
 _Reserved1_
  
- Este miembro está reservado para uso interno de Outlook y no es compatible.
    
 _Reserved2_
  
- Este miembro está reservado para uso interno de Outlook y no es compatible.
    
 *PEL* 
  
- a Esta es la lista de identificadores de entrada de las carpetas que se va a sincronizar si se ha establecido **UPS_THESE_FOLDERS** . Consulte mapidefs. h para obtener la definición de tipo de **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- a Se trata de una matriz de opciones de carpeta para las carpetas correspondientes en *PEL* si se ha establecido **UPS_THESE_FOLDERS** . Estas opciones de carpeta se usan al cargar cada una de las carpetas que aparecen en *PEL* durante el [Estado de carga](upload-folder-state.md)de la carpeta. Para obtener más información acerca de las opciones de carpeta, consulte **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

