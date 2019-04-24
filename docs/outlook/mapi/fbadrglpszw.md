---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341058"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida todas las cadenas de una matriz de cadenas Unicode. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Parámetros

 _lppszW_
  
> a Puntero a una matriz de cadenas Unicode terminadas en NULL. 
    
 _cStrings_
  
> a Número de cadenas en la matriz a las que apunta el parámetro _lppszW_ . 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una o varias de las cadenas de la matriz especificada no son válidas. 
    
FALSE 
  
> Las cadenas de la matriz especificada son válidas.
    

