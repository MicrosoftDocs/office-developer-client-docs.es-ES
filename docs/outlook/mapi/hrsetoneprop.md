---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817074"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Hace referencia a**: Outlook 
  
Establece o cambia el valor de una propiedad única en una interfaz (propiedad), es decir, una interfaz que se deriva de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parámetros

 _médico principal_
  
> [entrada] Puntero a una interfaz de [IMAPIProp](imapipropiunknown.md) en el que se puede establecer o cambiar el valor de la propiedad. 
    
 _pprop_
  
> [entrada] Puntero a la estructura de [SPropValue](spropvalue.md) define el valor que se establecerá en la propiedad _médico principal_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

A diferencia del método [IMAPIProp::SetProps](imapiprop-setprops.md) , la función **HrSetOneProp** no devuelve nunca si hay alguna advertencia. Ya que se establece sólo una propiedad, que simplemente se realiza correctamente o se produce un error. Para configurar o cambiar las propiedades de varios, **SetProps** es más rápido. 
  
Puede recuperar una sola propiedad con la función [HrGetOneProp](hrgetoneprop.md) . 
  

