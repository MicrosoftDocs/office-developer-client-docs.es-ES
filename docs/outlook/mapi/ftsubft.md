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
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408421"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Resta un entero de 64 bits sin signo de otro. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Parameters

 _Minuend_
  
> [in] Estructura [FILETIME](filetime.md) que contiene el entero de 64 bits sin signo del que se va a restar el valor del _parámetro Subtrahend._ 
    
 _Subtrahend_
  
> [in] Estructura **FILETIME** que contiene el entero de 64 bits sin signo que se resta del valor indicado por el _parámetro Minuend._ 
    
## <a name="return-value"></a>Valor devuelto

La **función FtSubFt** devuelve una **estructura FILETIME** que contiene el resultado de la resta. Los dos parámetros de entrada permanecen sin cambios. 
  

