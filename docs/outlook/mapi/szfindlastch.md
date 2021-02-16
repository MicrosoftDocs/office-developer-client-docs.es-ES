---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421259"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca la última aparición de un carácter en una cadena terminada en null. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Puntero a la cadena terminada en null en la que se va a buscar. 
    
 _ch_
  
> [entrada] Carácter que se va a buscar.
    
## <a name="return-value"></a>Valor devuelto

 **SzFindLastCh** devuelve un puntero a la última aparición del carácter de la cadena. Si el carácter no se produce en ninguna parte de la cadena o si el parámetro  _lpsz_ es NULL, se devuelve un valor NULL. 
  
## <a name="remarks"></a>Comentarios

La **función SzFindLastCh** solo busca una coincidencia exacta; es sensible a las diferencias entre mayúsculas y minúsculas. Se admiten búsquedas en los formatos Unicode y DBCS. 
  

