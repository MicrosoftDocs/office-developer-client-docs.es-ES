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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582913"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una lista de identificadores de entrada MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parámetros

 _lpEntryList_
  
> [entrada] Puntero a una estructura [ENTRYLIST](entrylist.md) que contiene una matriz de identificadores de entrada que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Uno o varios de los identificadores de entrada listada no son válidos. 
    
FALSE 
  
> Todos los identificadores de entrada enumerados son válidos.
    
## <a name="remarks"></a>Comentarios

La función **FBadEntryList** determina si se ha generado correctamente la lista de identificador de entrada. Un ejemplo de un identificador no válido es uno para qué memoria se ha asignado incorrectamente o un identificador de un tamaño incorrecto. 
  

