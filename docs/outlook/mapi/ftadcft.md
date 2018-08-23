---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f073dbb9655585ee56ab38be35bea4ef320042c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569774"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _FT1_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar. 
    
 _pies2_
  
> [entrada] Una estructura FILETIME que contiene el segundo entero de 64 bits sin signo que se va a agregar.
    
 _pwCarry_
  
> [entrada, salida, opcional] En la entrada, un puntero a la entrada de llevar a cabo marca. En la salida, un puntero al resultado de la adición encontrará. Este parámetro puede ser NULL si el resultado de transporte no es necesario.
    
## <a name="return-value"></a>Valor devuelto

La función **FtAdcFt** devuelve una estructura **FILETIME** que contiene la suma de los dos números enteros. No se modifican los dos parámetros de entrada. Si **pwCarry** no es NULL, contiene el resultado de transporte para la suma, 0 o 1. 
  
## <a name="remarks"></a>Comentarios

La función **FtAdcFt** es idéntica a **FtAddFt** cuando _pwCarry_ es NULL. Si _pwCarry_ no es NULL y puntos en 0, **FtAdcFt** devuelve el mismo valor **FILETIME** que devuelve **FtAddFt** . 
  
## <a name="see-also"></a>Recursos adicionales



[FtAddFt](ftaddft.md)

