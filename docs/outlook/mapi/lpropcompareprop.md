---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357438"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos valores de propiedad para determinar si son iguales. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValueA_
  
> a Puntero a una estructura [SPropValue](spropvalue.md) que define el primer valor de la propiedad que se va a comparar. 
    
 _lpSPropValueB_
  
> a Puntero a una estructura **SPropValue** que define el segundo valor de la propiedad que se va a comparar. 
    
## <a name="return-value"></a>Valor devuelto

 **LPropCompareProp** devuelve uno de los siguientes valores para la mayoría de los tipos de propiedades: 
  
- Menor que cero si el valor indicado por el parámetro _lpSPropValueA_ es menor que el indicado por el parámetro _lpSPropValueB_ . 
    
- Mayor que cero si el valor indicado por _lpSPropValueA_ es mayor que el indicado por _lpSPropValueB_.
    
- Cero si el valor indicado por _lpSPropValueA_ es igual al valor indicado por _lpSPropValueB_. 
    
Para los tipos de propiedad que no tienen ninguna ordenación intrínseca, como los tipos booleanos o de error, la función **LPropCompareProp** devuelve un valor no definido si los dos valores de propiedad no son iguales. Este valor no definido es distinto de cero y es coherente en todas las llamadas. 
  
## <a name="remarks"></a>Comentarios

Use la función **LPropCompareProp** sólo si los tipos de las dos propiedades que se van a comparar son iguales. 
  
Antes de llamar a **LPropCompareProp**, una aplicación cliente o un proveedor de servicios debe recuperar primero las propiedades para la comparación con una llamada al método [IMAPIProp:: GetProps](imapiprop-getprops.md) . Cuando un cliente o proveedor llama a **LPropCompareProp**, la función examina primero las etiquetas de propiedad para asegurarse de que la comparación de valores de propiedad es válida. A continuación, la función compara los valores de la propiedad y devuelve un valor adecuado. 
  
Si los valores de la propiedad no son iguales, **LPropCompareProp** determina cuál es el mayor. Las propiedades que comparan **LPropCompareProp** no tienen que pertenecer al mismo objeto. 
  

