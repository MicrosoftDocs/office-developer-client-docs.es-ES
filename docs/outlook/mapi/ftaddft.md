---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404767"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un entero de 64 bits sin signo a otro.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Parámetros

 _Addend1_
  
> [entrada] Estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar. 
    
 _Addend2_
  
> [entrada] Estructura **FILETIME** que contiene el segundo entero de 64 bits sin signo que se va a agregar. 
    
## <a name="return-value"></a>Valor devuelto

La **función FtAddFt** devuelve una **estructura FILETIME** que contiene la suma de los dos enteros. Los dos parámetros de entrada permanecen sin cambios. 
  

