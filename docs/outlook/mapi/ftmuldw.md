---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406349"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Multiplica un entero de 64 bits sin signo por un entero de 32 bits sin signo.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Parameters

 _Multiplicador_
  
> [in] Palabra doble que contiene el multiplicador entero sin signo de 32 bits. 
    
 _Multiplicand_
  
> [in] Estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo que se va a multiplicar por el valor del parámetro _Multiplier._ 
    
## <a name="return-value"></a>Valor devuelto

La **función FtMulDw** devuelve una **estructura FILETIME** que contiene el producto de los dos enteros. Los dos parámetros de entrada permanecen sin cambios. 
  

