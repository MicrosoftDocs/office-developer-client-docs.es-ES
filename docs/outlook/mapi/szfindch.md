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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345244"
---
# <a name="szfindch"></a>SzFindCh
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca la primera aparición de un carácter en una cadena terminada en NULL. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parameters

_lpsz_
  
> a Puntero a la cadena terminada en null en la que se va a realizar la búsqueda. 
    
_CH_
  
> a El carácter que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

**SzFindCh** devuelve un puntero a la primera aparición del carácter en la cadena. Si el carácter no aparece en ninguna parte de la cadena o si el parámetro _lpsz_ es null, se devuelve un valor null. 
  
## <a name="remarks"></a>Comentarios

La función **SzFindCh** busca sólo una coincidencia exacta; es sensible a las diferencias de mayúsculas y minúsculas y diacríticos. Se admiten las búsquedas en los formatos Unicode y DBCS. 
  

