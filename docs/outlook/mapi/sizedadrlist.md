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
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423464"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una [estructura ADRLIST](adrlist.md) con el nombre especificado que contiene un número especificado de estructuras [ADRENTRY.](adrentry.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parameters

_ _centries_
  
> Recuento de **estructuras ADRENTRY** que se incluirán en la nueva **estructura ADRLIST.** 
    
_ _name_
  
> Nombre de la nueva **estructura ADRLIST.** 
    
## <a name="remarks"></a>Comentarios

La **macro SizedADRLIST** permite definir una lista de destinatarios que tiene límites explícitos cuando se conocen los requisitos de longitud de la matriz. El código siguiente muestra cómo convertir el resultado de la macro **SizedADRLIST** en un **puntero de estructura ADRLIST:** 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Vea también

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

