---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816892"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Se aplica a**: Outlook 
  
Agrega un entero de 64 bits sin signo a otro, de forma opcional mediante una marca de transporte.
  
|||
|:-----|:-----|
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Sintaxis

 _FT1_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar. 
    
 _pies2_
  
> [entrada] Una estructura FILETIME que contiene el segundo entero de 64 bits sin signo que se va a agregar.
    
 _pwCarry_
  
> [entrada, salida, opcional] En la entrada, un puntero a la entrada de llevar a cabo marca. En la salida, un puntero al resultado de la adición encontrará. Este parámetro puede ser NULL si el resultado de transporte no es necesario.
    
## <a name="return-value"></a>Valor devuelto

La función **FtAdcFt** devuelve una estructura **FILETIME** que contiene la suma de los dos números enteros. No se modifican los dos parámetros de entrada. Si **pwCarry** no es NULL, contiene el resultado de transporte para la suma, 0 o 1. 
  
## <a name="remarks"></a>Notas

La función **FtAdcFt** es idéntica a **FtAddFt** cuando _pwCarry_ es NULL. Si _pwCarry_ no es NULL y puntos en 0, **FtAdcFt** devuelve el mismo valor **FILETIME** que devuelve **FtAddFt** . 
  
## <a name="see-also"></a>Ver también



[FtAddFt](ftaddft.md)

