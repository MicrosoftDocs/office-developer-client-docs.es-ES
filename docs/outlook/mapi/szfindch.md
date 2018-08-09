---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820828"
---
# <a name="szfindch"></a>SzFindCh
 
**Hace referencia a**: Outlook 
  
Busca la primera aparición de un carácter en una cadena terminada en null. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parámetros

_lpsz_
  
> [entrada] Puntero a la cadena terminada en null que se desea buscar. 
    
_canales_
  
> [entrada] El carácter que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

**SzFindCh** devuelve un puntero a la primera aparición del carácter en la cadena. Si el carácter no se produce en cualquier lugar en la cadena, o si el parámetro _lpsz_ es NULL, se devuelve un valor null. 
  
## <a name="remarks"></a>Comentarios

La función **SzFindCh** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas. Se admiten las búsquedas en los formatos de Unicode y DBCS. 
  

