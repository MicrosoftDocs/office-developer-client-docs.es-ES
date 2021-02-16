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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433811"
---
# <a name="sync"></a>SYNC

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para iniciar la sincronización entre un almacén local y un servidor. Esta información se usa durante el [estado de sincronización.](synchronize-state.md)
  
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
  
- [out]/[in] Máscara de bits de las siguientes marcas que modifica el comportamiento durante la sincronización:
    
- UPS_UPLOAD_ONLY
    
  - [entrada] El cliente solo realizará la carga. Outlook solo devuelve carpetas modificadas localmente.
    
- UPS_DNLOAD_ONLY
    
  - [entrada] El cliente solo realizará la descarga. Outlook no debe borrar los bits de carga de las carpetas.
    
- UPS_THESE_FOLDERS
    
  - [entrada] El cliente sincronizará un conjunto especificado de carpetas con los identificadores de entrada proporcionados. Esta marca se puede combinar con la **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY** marca. 
    
- UPS_OK
    
  - [salida] La sincronización se ha realizado correctamente. El cliente establece esto después de cargar o de completar una sincronización completa.
    
- 
    
    > [!NOTE]
    > Aunque el cliente puede cargar o sincronizar completamente (cargar y descargar) carpetas y elementos con la API de replicación, el cliente especifica *ulFlags* con una sola dirección de la replicación a la vez, ya sea la marca **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY.** En el caso de una sincronización completa, el cliente primero realiza una carga con la marca **UPS_UPLOAD_ONLY** y, a continuación, una descarga con la **marca UPS_DNLOAD_ONLY** usuario. 
  
 _pwzPath_
  
- [salida] Ruta de acceso al almacén local.
    
 _Reserved1_
  
- Este miembro está reservado para el uso interno de Outlook y no es compatible.
    
 _Reserved2_
  
- Este miembro está reservado para el uso interno de Outlook y no es compatible.
    
 *pel* 
  
- [entrada] Esta es la lista de identificadores de entrada de las carpetas que se sincronizarán **si UPS_THESE_FOLDERS** se ha establecido. Vea mapidefs.h para obtener la definición de tipo **de LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- [entrada] Se trata de una matriz de opciones de carpeta para las carpetas  *correspondientes*  en pel **si UPS_THESE_FOLDERS** se ha establecido. Estas opciones de carpeta se usan al cargar cada una de las carpetas enumeradas en *pel* durante el estado [de carga de la carpeta.](upload-folder-state.md) Para obtener más información acerca de las opciones de carpeta, **[vea UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

