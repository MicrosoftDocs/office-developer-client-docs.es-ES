---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816894"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Hace referencia a**: Outlook 
  
Un entero sin signo de 32 bits se multiplica por otro.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parámetros

 _Multiplicando_
  
> [entrada] Una palabra doble que contiene el entero sin signo de 32 bits a ser multiplicado por el valor en el parámetro _multiplicador_ . 
    
 _Multiplicador_
  
> [entrada] Una palabra doble que contiene el multiplicador de entero sin signo de 32 bits.
    
## <a name="return-value"></a>Valor devuelto

La función **FtMulDwDw** devuelve una estructura [FILETIME](filetime.md) que contiene el producto de los dos enteros. No se modifican los dos parámetros de entrada. 
  

