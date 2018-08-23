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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592027"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  

