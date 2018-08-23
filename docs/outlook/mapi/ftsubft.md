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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578265"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _Minuendo_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo desde la que el valor en el parámetro _sustraendo_ es que se va a restar. 
    
 _Sustraendo_
  
> [entrada] Una estructura **FILETIME** que contiene el entero sin signo de 64 bits que se resta el valor indicado por el parámetro _minuendo_ . 
    
## <a name="return-value"></a>Valor devuelto

La función **FtSubFt** devuelve una estructura **FILETIME** que contiene el resultado de la resta. No se modifican los dos parámetros de entrada. 
  

