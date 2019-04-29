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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435225"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca la primera aparición de una subcadena terminada en null en una cadena terminada en NULL. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> a Puntero a la cadena terminada en null en la que se va a realizar la búsqueda. El parámetro _lpsz_ no debe superar los 65536 caracteres. 
    
 _lpszKey_
  
> a Puntero a la subcadena terminada en null que se va a buscar. El parámetro _lpszKey_ no debe superar los 65536 caracteres. 
    
## <a name="return-value"></a>Valor devuelto

 **SzFindSz** devuelve un puntero al primer carácter de la primera aparición de la subcadena en la cadena. Si la subcadena no aparece en ninguna parte de la cadena, si _lpszKey_ es mayor que _lpsz_o si cualquiera de los parámetros es null, se devuelve un valor null. 
  
## <a name="remarks"></a>Comentarios

La función **SzFindSz** busca sólo una coincidencia exacta; es sensible a las diferencias de mayúsculas y minúsculas y diacríticos. Se admiten las búsquedas en formatos Unicode y DBCS. El límite de longitud de ambos parámetros está en caracteres, no necesariamente bytes. 
  

