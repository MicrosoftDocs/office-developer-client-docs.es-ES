---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eb3e0d5a96121f63166da2025743b7ef89f4ecf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432243"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una restricción usada para limitar una vista de tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Parámetros

 _lpres_
  
> a Estructura [SRestriction](srestriction.md) que define la restricción que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La restricción especificada o una o varias de sus subrestricciones no son válidas. 
    
FALSE 
  
> La restricción especificada y todas sus subrestricciones son válidas.
    
## <a name="remarks"></a>Comentarios

Una vez validada la restricción, se puede pasar en llamadas al método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir la tabla a determinadas filas, al método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar una fila de tabla y a los métodos de [IMAPIContainer](imapicontainerimapiprop.md) interfaz para realizar una restricción en un objeto contenedor. 
  

