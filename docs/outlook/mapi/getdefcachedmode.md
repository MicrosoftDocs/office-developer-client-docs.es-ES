---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816944"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _pfPolicy_
  
> [out] **true** si se aplica el valor devuelto por la directiva, **false** si no lo está. 
    
## <a name="return-values"></a>Valores devueltos

 **True**
  
- Almacenamiento en caché está habilitado.
    
 **False**
  
- Se deshabilita el almacenamiento en caché.
    
## <a name="see-also"></a>Ver también



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

