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
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591397"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si está habilitado el modo de intercambio en caché para el almacén de Exchange privado y, si esto se aplica mediante una directiva.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Exportada por:  <br/> |Msmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

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



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

