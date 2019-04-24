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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341037"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una matriz de estructuras que describen las propiedades con nombre y comprueba su asignación. 
  
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
  
> a Puntero a una matriz de estructuras [MAPINAMEID](mapinameid.md) que describen las propiedades con nombre. 
    
 _CNAME_
  
> a Número de estructuras de propiedad con nombre en la matriz señalada por el parámetro _lppNameId_ . 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una o varias de las estructuras de nombres de propiedad especificadas no son válidas. 
    
FALSE 
  
> Las estructuras de nombres de propiedad especificadas son válidas.
    
## <a name="remarks"></a>Comentarios

La función **FBadRglpNameID** se puede usar al configurar una llamada a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) o [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

