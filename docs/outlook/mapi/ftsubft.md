---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816900"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Se aplica a**: Outlook 
  
Resta un entero sin signo de 64 bits de otro. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Sintaxis

 _Minuendo_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo desde la que el valor en el parámetro _sustraendo_ es que se va a restar. 
    
 _Sustraendo_
  
> [entrada] Una estructura **FILETIME** que contiene el entero sin signo de 64 bits que se resta el valor indicado por el parámetro _minuendo_ . 
    
## <a name="return-value"></a>Valor devuelto

La función **FtSubFt** devuelve una estructura **FILETIME** que contiene el resultado de la resta. No se modifican los dos parámetros de entrada. 
  

