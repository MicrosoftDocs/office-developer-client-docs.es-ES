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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816897"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**Se aplica a**: Outlook 
  
Agrega un entero de 64 bits sin signo a otra.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Sintaxis

 _Addend1_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el primer entero de 64 bits sin signo que se va a agregar. 
    
 _Addend2_
  
> [entrada] Una estructura **FILETIME** que contiene el segundo entero de 64 bits sin signo que se va a agregar. 
    
## <a name="return-value"></a>Valor devuelto

La función **FtAddFt** devuelve una estructura **FILETIME** que contiene la suma de los dos números enteros. No se modifican los dos parámetros de entrada. 
  

