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
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816788"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Hace referencia a**: Outlook 
  
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
  

