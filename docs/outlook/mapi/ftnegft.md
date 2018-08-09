---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816905"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Hace referencia a**: Outlook 
  
Calcula el complemento de dos de un entero de 64 bits sin signo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Parámetros

 _FT_
  
> [entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits que se va a calcular el complemento de dos. 
    
## <a name="return-value"></a>Valor devuelto

La función **FtNegFt** devuelve una estructura **FILETIME** que contiene el complemento de dos del número entero. El parámetro de entrada no sufre cambios. 
  

