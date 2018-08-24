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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585125"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Puntero a la cadena terminada en null que se desea buscar. El parámetro _lpsz_ no debe superar los caracteres, de 65536. 
    
 _lpszKey_
  
> [entrada] Puntero a la subcadena terminada en null que se va a buscar. El parámetro _lpszKey_ no debe superar los caracteres, de 65536. 
    
## <a name="return-value"></a>Valor devuelto

 **SzFindSz** devuelve un puntero al primer carácter de la primera aparición de la subcadena en la cadena. Si la subcadena no se producen en cualquier lugar en la cadena, si _lpszKey_ es mayor que _lpsz_o si ninguno de estos parámetros es NULL, se devuelve un valor null. 
  
## <a name="remarks"></a>Comentarios

La función **SzFindSz** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas. Se admiten las búsquedas en formatos de Unicode y DBCS. Es el límite de longitud en ambos parámetros en caracteres, no necesariamente bytes. 
  

