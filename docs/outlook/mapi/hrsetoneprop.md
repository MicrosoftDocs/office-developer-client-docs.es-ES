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
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347771"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o cambia el valor de una propiedad única en una interfaz de propiedades, es decir, una interfaz derivada de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameters

 _proveedor_
  
> a Puntero a una interfaz de [IMAPIProp](imapipropiunknown.md) en la que se va a establecer o cambiar el valor de la propiedad. 
    
 _pprop_
  
> a Puntero a la estructura [SPropValue](spropvalue.md) que define el valor que se va a establecer en la propiedad _PMP_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

A diferencia del método [IMAPIProp:: SetProps](imapiprop-setprops.md) , la función **HrSetOneProp** nunca devuelve ninguna advertencia. Dado que sólo establece una propiedad, simplemente se realiza correctamente o produce un error. Para establecer o cambiar varias propiedades, **SetProps** es más rápido. 
  
Puede recuperar una sola propiedad con la función [HrGetOneProp](hrgetoneprop.md) . 
  

