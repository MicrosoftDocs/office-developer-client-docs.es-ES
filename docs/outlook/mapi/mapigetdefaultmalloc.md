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
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592335"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera la dirección de la función de asignación de memoria MAPI predeterminada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a>Parámetros

Ninguno. 
  
## <a name="return-value"></a>Valor devuelto

La función **MAPIGetDefaultMalloc** devuelve un puntero a la función de asignación de memoria MAPI predeterminada. 
  

