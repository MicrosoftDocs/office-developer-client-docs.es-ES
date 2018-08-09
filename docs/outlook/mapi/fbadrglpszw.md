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
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816790"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Hace referencia a**: Outlook 
  
Valida todas las cadenas de una matriz de cadenas Unicode. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a>Parámetros

 _lppszW_
  
> [entrada] Puntero a una matriz de cadenas de Unicode terminada en null. 
    
 _objetos CString_
  
> [entrada] Recuento de las cadenas en la matriz indicada por el parámetro _lppszW_ . 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una o varias de las cadenas de la matriz especificada no son válidos. 
    
FALSE 
  
> Las cadenas de la matriz especificada son válidas.
    

