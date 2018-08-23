---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574744"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una estructura de [ADRLIST](adrlist.md) con el nombre especificado que contiene un número especificado de estructuras [ADRENTRY](adrentry.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parámetros

__centries_
  
> Recuento de las estructuras **ADRENTRY** que se deben incluir en la nueva estructura **ADRLIST** . 
    
__nombre_
  
> Nombre de la nueva estructura **ADRLIST** . 
    
## <a name="remarks"></a>Comentarios

La macro **SizedADRLIST** le permite definir una lista de destinatarios que tiene límites explícitos cuando se conocen los requisitos de longitud de la matriz. El código siguiente muestra cómo convertir el resultado de la macro **SizedADRLIST** a un puntero de estructura **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Recursos adicionales

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

