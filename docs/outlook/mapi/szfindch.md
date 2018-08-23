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
ms.openlocfilehash: 8426f782eb5fbf8a125833c51b25ccd605acbd64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573526"
---
# <a name="szfindch"></a>SzFindCh
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  

