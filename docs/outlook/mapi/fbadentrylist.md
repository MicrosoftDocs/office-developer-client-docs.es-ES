---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427776"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una lista de identificadores de entrada MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parámetros

 _lpEntryList_
  
> [in] Puntero a una [estructura ENTRYLIST](entrylist.md) que contiene una matriz de identificadores de entrada que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Uno o varios de los identificadores de entrada enumerados no son válidos. 
    
FALSE 
  
> Todos los identificadores de entrada enumerados son válidos.
    
## <a name="remarks"></a>Comentarios

La **función FBadEntryList** determina si la lista de identificadores de entrada se ha generado correctamente. Un ejemplo de un identificador no válido es uno para el que la memoria se ha asignado incorrectamente o un identificador de un tamaño incorrecto. 
  

