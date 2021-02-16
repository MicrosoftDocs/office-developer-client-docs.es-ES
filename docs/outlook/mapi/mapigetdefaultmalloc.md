---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438207"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera la dirección de la función de asignación de memoria MAPI predeterminada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a>Parámetros

Ninguno. 
  
## <a name="return-value"></a>Valor devuelto

La **función MAPIGetDefaultMalloc** devuelve un puntero a la función de asignación de memoria MAPI predeterminada. 
  

