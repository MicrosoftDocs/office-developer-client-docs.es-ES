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
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299464"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte un número binario en una representación de cadena de un número hexadecimal. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Parameters

 _pb_
  
> a Puntero a los datos binarios que se van a convertir. 
    
 _cb_
  
> a Tamaño, en bytes, de los datos binarios a los que apunta el parámetro _PB_ . 
    
 _SZ_
  
> contempla Puntero a una cadena ASCII terminada en null que representa los datos binarios en dígitos hexadecimales.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

La función **HexFromBin** toma un puntero a una unidad de datos binarios cuyo tamaño se indica mediante el parámetro _CB_ . Devuelve en la cadena _SZ_ , dentro de (2 * _CB_) + 1 bytes de memoria, una representación de esta información binaria en números hexadecimales. Si el valor de byte es decimal 10, por ejemplo, la cadena hexadecimal será 0A, por lo que un byte convierte a dos bytes en la cadena. 
  

