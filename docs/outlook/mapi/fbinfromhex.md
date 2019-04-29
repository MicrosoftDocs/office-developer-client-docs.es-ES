---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414938"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte una representación de cadena de un número hexadecimal en datos binarios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parameters

 _SZ_
  
> a Puntero a la cadena ASCII terminada en null que se va a convertir. No es una cadena Unicode. Los caracteres válidos incluyen los caracteres hexadecimales del 0 al 9 y los caracteres en mayúsculas y minúsculas de la a a la F.
    
 _pb_
  
> contempla Puntero al número binario devuelto.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> La cadena se convirtió correctamente en un número binario. 
    
FALSE 
  
> La cadena de entrada contiene caracteres hexadecimales ASCII no válidos.
    
## <a name="see-also"></a>Ver también



[ScBinFromHexBounded](scbinfromhexbounded.md)

