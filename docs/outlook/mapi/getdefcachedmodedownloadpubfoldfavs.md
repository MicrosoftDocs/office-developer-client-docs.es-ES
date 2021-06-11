---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417710"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si el modo Exchange caché para la carpeta Favoritos de **carpetas** públicas está habilitado y si se aplica mediante directiva. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameters

 _pfPolicy_
  
> [salida] **true** si la directiva aplica el valor devuelto, **false** si no lo es. 
    
## <a name="return-values"></a>Valores devueltos

 **true**
  
- El almacenamiento en caché está habilitado.
    
 **false**
  
- El almacenamiento en caché está deshabilitado.
    
## <a name="see-also"></a>Vea también



[GetDefCachedMode](getdefcachedmode.md)

