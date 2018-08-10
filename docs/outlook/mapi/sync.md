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
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820821"
---
# <a name="sync"></a>SYNC

  
  
**Hace referencia a**: Outlook 
  
Información para iniciar la sincronización entre un almacén local y un servidor. Esta información se usa durante la [sincronización de estado](synchronize-state.md).
  
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

## <a name="members"></a>Members

 _ulFlags_
  
- [out] o [in] una máscara de bits de los siguientes indicadores que modifica el comportamiento durante la sincronización:
    
- UPS_UPLOAD_ONLY
    
  - [entrada] El cliente llevará a cabo solo carga. Outlook sólo devuelve las carpetas localmente modificadas.
    
- UPS_DNLOAD_ONLY
    
  - [entrada] El cliente llevará a cabo sólo descarga. Outlook no debe borrar bits de carga para las carpetas.
    
- UPS_THESE_FOLDERS
    
  - [entrada] El cliente va a sincronizar un conjunto especificado de carpetas con los identificadores de entrada proporcionado. Este indicador se puede combinar con marca de la **UPS_UPLOAD_ONLY** o **UPS_DNLOAD_ONLY** . 
    
- UPS_OK
    
  - [out] Sincronización realizada correctamente. El cliente establece esto después de cargar o se complete una sincronización completa.
    
- 
    
    > [!NOTE]
    > Aunque el cliente puede cargar o totalmente sincronizar (cargar, a continuación, descargue) carpetas y elementos con la API de replicación, el cliente especifica *ulFlags* con una única dirección de la replicación en un momento: el **UPS_UPLOAD_ONLY** o Marca **UPS_DNLOAD_ONLY** . En el caso de una sincronización completa, el cliente realiza primero una carga con el indicador **UPS_UPLOAD_ONLY** y, a continuación, una descarga con la marca **UPS_DNLOAD_ONLY** . 
  
 _pwzPath_
  
- [out] Ruta de acceso en el almacén local.
    
 _Reserved1_
  
- Este miembro está reservado para el uso interno de Outlook y no se admite.
    
 _Reservado2_
  
- Este miembro está reservado para el uso interno de Outlook y no se admite.
    
 *PEL* 
  
- [entrada] Ésta es la lista de identificadores de las carpetas para sincronizar si se ha establecido **UPS_THESE_FOLDERS** de entrada. Vea mapidefs.h para la definición de tipo de **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- [entrada] Esto es una matriz de las opciones de carpeta para carpetas correspondientes en *pel* si se ha establecido **UPS_THESE_FOLDERS** . Estas opciones de carpeta se usan cuando se carga cada una de las carpetas que aparecen en *pel* durante la [carga de estado de la carpeta](upload-folder-state.md). Para obtener más información acerca de las opciones de carpeta, consulte **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)

