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
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421945"
---
# <a name="szfindch"></a>SzFindCh
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca la primera aparición de un carácter en una cadena terminada en null. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parámetros

_lpsz_
  
> [entrada] Puntero a la cadena terminada en null en la que se buscará. 
    
_ch_
  
> [entrada] Carácter que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

**SzFindCh** devuelve un puntero a la primera aparición del carácter de la cadena. Si el carácter no se produce en ninguna parte de la cadena o si el parámetro  _lpsz_ es NULL, se devuelve un valor NULL. 
  
## <a name="remarks"></a>Comentarios

La **función SzFindCh** solo busca una coincidencia exacta; es sensible a las diferencias entre mayúsculas y minúsculas. Se admiten búsquedas en los formatos Unicode y DBCS. 
  

