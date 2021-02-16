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
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429708"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un entero de 64 bits sin signo a otro, opcionalmente usando una marca de transporte.
  
|||
|:-----|:-----|
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Parámetros

 _ft1_
  
> [entrada] Estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar. 
    
 _ft2_
  
> [entrada] Estructura FILETIME que contiene el segundo entero de 64 bits sin signo que se va a agregar.
    
 _pwCarry_
  
> [entrada, salida, opcional] En la entrada, un puntero a la marca de transporte entrante. En la salida, un puntero al resultado de transporte para la adición. Este parámetro puede ser NULL si no se requiere el resultado de transporte.
    
## <a name="return-value"></a>Valor devuelto

La **función FtAdcFt** devuelve una **estructura FILETIME** que contiene la suma de los dos enteros. Los dos parámetros de entrada permanecen sin cambios. Si **pwCarry** no es NULL, contiene el resultado de carga de la suma, ya sea 0 o 1. 
  
## <a name="remarks"></a>Comentarios

La **función FtAdcFt** es idéntica **a FtAddFt** cuando  _pwCarry_ es NULL. Si  _pwCarry_ no es NULL y apunta a 0, **FtAdcFt** devuelve el mismo **valor FILETIME** que **ftAddFt** devuelve. 
  
## <a name="see-also"></a>Consulte también



[FtAddFt](ftaddft.md)

