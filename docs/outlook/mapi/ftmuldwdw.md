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
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327982"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Multiplica un entero unsigned 32-bit por otro.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parameters

 _Multiplicand_
  
> a Una palabra doble que contiene el entero de 32 bits sin signo que se va a multiplicar por el valor en el parámetro _multiplicador_ . 
    
 _Multiplicador_
  
> a Una palabra doble que contiene el multiplicador de enteros de 32 bits sin signo.
    
## <a name="return-value"></a>Valor devuelto

La función **FtMulDwDw** devuelve una estructura [FILETIME](filetime.md) que contiene el producto de los dos enteros. Los dos parámetros de entrada permanecen sin cambios. 
  

