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
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581730"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si está habilitado el modo de intercambio en caché para la carpeta **Favoritos de carpetas públicas** y, si esto se aplica mediante una directiva. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |Msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parámetros

 _pfPolicy_
  
> [out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está. 
    
## <a name="return-values"></a>Valores devueltos

 **True**
  
- Almacenamiento en caché está habilitado.
    
 **False**
  
- Se deshabilita el almacenamiento en caché.
    
## <a name="see-also"></a>Recursos adicionales



[GetDefCachedMode](getdefcachedmode.md)

