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
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816794"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Hace referencia a**: Outlook 
  
Valida una restricción que se usa para limitar una vista de tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Parámetros

 _lpres_
  
> [entrada] Una estructura [SRestriction](srestriction.md) definición de la restricción que se va a validar. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La restricción especificada, o una o varias de sus subrestrictions, no están válido. 
    
FALSE 
  
> La restricción especificada y todas sus subrestrictions son válidos.
    
## <a name="remarks"></a>Comentarios

Una vez que se valida una restricción, puede pasarse en llamadas al método [IMAPITable:: Restrict](imapitable-restrict.md) para restringir la tabla a algunas filas, al método [IMAPITable:: FindRow](imapitable-findrow.md) para localizar una fila de tabla y a los métodos de la [IMAPIContainer](imapicontainerimapiprop.md) interfaz para llevar a cabo una restricción en un objeto contenedor. 
  

