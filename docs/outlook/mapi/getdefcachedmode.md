---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412747"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si el modo caché de Exchange para el almacén de Exchange privado está habilitado y si esto se aplica mediante la directiva.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportado por:  <br/> |msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parámetros

 _pfPolicy_
  
> [salida] **true** si la directiva aplica el valor devuelto, **false** si no lo es. 
    
## <a name="return-values"></a>Valores devueltos

 **true**
  
- El almacenamiento en caché está habilitado.
    
 **false**
  
- El almacenamiento en caché está deshabilitado.
    
## <a name="see-also"></a>Consulte también



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

