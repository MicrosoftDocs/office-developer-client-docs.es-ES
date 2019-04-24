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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299891"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si está habilitado el modo caché de Exchange para la carpeta favoritos de la **carpeta pública** y si lo exige la Directiva. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|ExPortado por:  <br/> |MSMAPI32. dll  <br/> |
|Llamado por:  <br/> |Client  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameters

 _pfPolicy_
  
> contempla **true** si la Directiva aplica el valor devuelto, **false** en caso contrario. 
    
## <a name="return-values"></a>Valores devueltos

 **true**
  
- El almacenamiento en caché está habilitado.
    
 **false**
  
- El almacenamiento en caché está deshabilitado.
    
## <a name="see-also"></a>Vea también



[GetDefCachedMode](getdefcachedmode.md)

