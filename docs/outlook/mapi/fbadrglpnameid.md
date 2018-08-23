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
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588149"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Valida una matriz de estructuras que describen las propiedades con nombre y comprueba su asignación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapival.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Parámetros

 _lppNameId_
  
> [entrada] Puntero a una matriz de estructuras [MAPINAMEID](mapinameid.md) que describen las propiedades con nombre. 
    
 _CNAME_
  
> [entrada] Recuento de las estructuras de la propiedad con nombre en la matriz indicada por el parámetro _lppNameId_ . 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Una o varias de las estructuras de nombre de propiedad especificado no son válido. 
    
FALSE 
  
> Las estructuras de nombre de propiedad especificado son válidas.
    
## <a name="remarks"></a>Comentarios

La función **FBadRglpNameID** se puede usar al configurar para una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) o [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

