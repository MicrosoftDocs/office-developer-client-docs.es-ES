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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414616"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos valores de propiedad para determinar si son iguales. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parámetros

 _lpSPropValueA_
  
> [entrada] Puntero a una [estructura SPropValue](spropvalue.md) que define el primer valor de propiedad que se va a comparar. 
    
 _lpSPropValueB_
  
> [entrada] Puntero a una **estructura SPropValue** que define el segundo valor de propiedad que se va a comparar. 
    
## <a name="return-value"></a>Valor devuelto

 **LPropCompareProp** devuelve uno de los siguientes valores para la mayoría de los tipos de propiedad: 
  
- Menor que cero si el valor indicado por el parámetro _lpSPropValueA_ es menor que el indicado por el parámetro _lpSPropValueB._ 
    
- Mayor que cero si el valor indicado por  _lpSPropValueA_ es mayor que el indicado por  _lpSPropValueB_.
    
- Cero si el valor indicado por  _lpSPropValueA_ es igual al valor indicado por  _lpSPropValueB_. 
    
Para los tipos de propiedades que no tienen orden intrínseco, como los tipos booleanos o de error, la función **LPropCompareProp** devuelve un valor no definido si los dos valores de propiedad no son iguales. Este valor no definido es distinto de cero y es coherente en todas las llamadas. 
  
## <a name="remarks"></a>Comentarios

Use la **función LPropCompareProp** solo si los tipos de las dos propiedades que se van a comparar son los mismos. 
  
Antes de llamar a **LPropCompareProp**, una aplicación cliente o un proveedor de servicios debe recuperar primero las propiedades para comparar con una llamada al método [IMAPIProp::GetProps.](imapiprop-getprops.md) Cuando un cliente o proveedor llama a **LPropCompareProp**, la función examina primero las etiquetas de propiedad para asegurarse de que la comparación de valores de propiedad es válida. A continuación, la función compara los valores de propiedad y devuelve un valor adecuado. 
  
Si los valores de propiedad no son iguales, **LPropCompareProp** determina cuál es el mayor. Las propiedades que **compara LPropCompareProp** no tienen que pertenecer al mismo objeto. 
  

