---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434833"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una matriz de estructuras que describen propiedades con nombre y comprueba su asignación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Parámetros

 _lppNameId_
  
> [in] Puntero a una matriz de [estructuras MAPINAMEID](mapinameid.md) que describen las propiedades con nombre. 
    
 _cNames_
  
> [in] Recuento de estructuras de propiedades con nombre en la matriz a la que apunta el parámetro _lppNameId._ 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una o varias de las estructuras de nombre de propiedad especificadas no son válidas. 
    
FALSE 
  
> Todas las estructuras de nombre de propiedad especificadas son válidas.
    
## <a name="remarks"></a>Comentarios

La **función FBadRglpNameID** se puede usar al configurar una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) o [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

