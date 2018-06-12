---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820832"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Se aplica a**: Outlook 
  
Busca la primera aparición de una subcadena terminada en null en una cadena terminada en null. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Sintaxis

 _lpsz_
  
> [entrada] Puntero a la cadena terminada en null que se desea buscar. El parámetro _lpsz_ no debe superar los caracteres, de 65536. 
    
 _lpszKey_
  
> [entrada] Puntero a la subcadena terminada en null que se va a buscar. El parámetro _lpszKey_ no debe superar los caracteres, de 65536. 
    
## <a name="return-value"></a>Valor devuelto

 **SzFindSz** devuelve un puntero al primer carácter de la primera aparición de la subcadena en la cadena. Si la subcadena no se producen en cualquier lugar en la cadena, si _lpszKey_ es mayor que _lpsz_o si ninguno de estos parámetros es NULL, se devuelve un valor null. 
  
## <a name="remarks"></a>Notas

La función **SzFindSz** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas. Se admiten las búsquedas en formatos de Unicode y DBCS. Es el límite de longitud en ambos parámetros en caracteres, no necesariamente bytes. 
  

