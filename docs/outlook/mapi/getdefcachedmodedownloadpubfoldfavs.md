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
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816943"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Hace referencia a**: Outlook 
  
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
    
## <a name="see-also"></a>Vea también



[GetDefCachedMode](getdefcachedmode.md)

