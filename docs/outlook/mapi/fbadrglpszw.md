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
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565917"
---
# <a name="fbadrglpszw"></a>FBadRglpszW

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    

