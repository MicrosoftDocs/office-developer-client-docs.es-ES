---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584838"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte a un número binario en una representación de cadena de un número hexadecimal. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parámetros

 _pb_
  
> [entrada] Puntero a los datos binarios que se va a convertir. 
    
 _cb_
  
> [entrada] Tamaño, en bytes, de los datos binarios que señala el parámetro _pb_ . 
    
 _sz_
  
> [out] Puntero a una cadena de ASCII terminada en null que representa los datos binarios de dígitos hexadecimales.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

La función **HexFromBin** toma un puntero a una unidad de datos binarios cuyo tamaño es indicada por el parámetro _cb_ . Devuelve en la cadena _sz_ , comprendido en (2 * _cb_) + 1 bytes de memoria, una representación de esta información binaria en números hexadecimales. Si el valor de tipo byte es 10 decimal, por ejemplo, la cadena hexadecimal será 0A, es así de un byte se convierte en dos bytes en la cadena. 
  

