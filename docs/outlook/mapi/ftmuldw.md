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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816890"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _Multiplicador_
  
> [entrada] Una palabra doble que contiene el multiplicador de entero sin signo de 32 bits. 
    
 _Multiplicando_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits a ser multiplicado por el valor en el parámetro _multiplicador_ . 
    
## <a name="return-value"></a>Valor devuelto

La función **FtMulDw** devuelve una estructura **FILETIME** que contiene el producto de los dos enteros. No se modifican los dos parámetros de entrada. 
  

