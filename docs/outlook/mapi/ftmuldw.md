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
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583998"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Multiplica a un entero de 64 bits sin signo por un entero sin signo de 32 bits.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Parámetros

 _Multiplicador_
  
> [entrada] Una palabra doble que contiene el multiplicador de entero sin signo de 32 bits. 
    
 _Multiplicando_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits a ser multiplicado por el valor en el parámetro _multiplicador_ . 
    
## <a name="return-value"></a>Valor devuelto

La función **FtMulDw** devuelve una estructura **FILETIME** que contiene el producto de los dos enteros. No se modifican los dos parámetros de entrada. 
  

