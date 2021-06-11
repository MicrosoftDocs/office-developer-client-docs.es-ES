---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412915"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Multiplica un entero de 32 bits sin signo por otro.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parameters

 _Multiplicand_
  
> [in] Palabra doble que contiene el entero de 32 bits sin signo que se va a multiplicar por el valor del parámetro _Multiplier._ 
    
 _Multiplicador_
  
> [in] Palabra doble que contiene el multiplicador entero sin signo de 32 bits.
    
## <a name="return-value"></a>Valor devuelto

La **función FtMulDwDw** devuelve una [estructura FILETIME](filetime.md) que contiene el producto de los dos enteros. Los dos parámetros de entrada permanecen sin cambios. 
  

