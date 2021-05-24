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
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589183"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o cambia el valor de una sola propiedad en una interfaz de propiedad, es decir, una interfaz derivada de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameters

 _pmp_
  
> [in] Puntero a una [interfaz IMAPIProp](imapipropiunknown.md) en la que se va a establecer o cambiar el valor de la propiedad. 
    
 _pprop_
  
> [in] Puntero a la [estructura SPropValue](spropvalue.md) que define el valor que se va a establecer en la _propiedad pmp._ 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

A diferencia [del método IMAPIProp::SetProps,](imapiprop-setprops.md) la **función HrSetOneProp** nunca devuelve ninguna advertencia. Dado que establece solo una propiedad, simplemente se realiza correctamente o se produce un error. Para establecer o cambiar varias propiedades, **SetProps** es más rápido. 
  
Puede recuperar una sola propiedad con la [función HrGetOneProp.](hrgetoneprop.md) 
  

