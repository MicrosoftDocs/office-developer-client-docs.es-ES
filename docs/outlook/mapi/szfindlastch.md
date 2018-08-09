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
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820830"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Hace referencia a**: Outlook 
  
Busca la última aparición de un carácter en una cadena terminada en null. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **SzFindLastCh** devuelve un puntero a la última aparición del carácter en la cadena. Si el carácter no se produce en cualquier lugar en la cadena, o si el parámetro _lpsz_ es NULL, se devuelve un valor null. 
  
## <a name="remarks"></a>Comentarios

La función **SzFindLastCh** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas. Se admiten las búsquedas en los formatos de Unicode y DBCS. 
  

