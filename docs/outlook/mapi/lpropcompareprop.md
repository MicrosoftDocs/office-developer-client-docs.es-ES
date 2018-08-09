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
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818053"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Hace referencia a**: Outlook 
  
Compara dos valores de propiedad para determinar si son iguales. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parámetros

 _lpSPropValueA_
  
> [entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir el primer valor de propiedad que se va a comparar. 
    
 _lpSPropValueB_
  
> [entrada] Puntero a una estructura de **SPropValue** define el segundo valor de propiedad que se va a comparar. 
    
## <a name="return-value"></a>Valor devuelto

 **LPropCompareProp** devuelve uno de los siguientes valores para la mayoría de los tipos de propiedad: 
  
- Menor que cero si el valor indicado por el parámetro _lpSPropValueA_ es menor que la indicada por el parámetro _lpSPropValueB_ . 
    
- Mayor que cero si el valor indicado por _lpSPropValueA_ es mayor que el indicado por _lpSPropValueB_.
    
- Cero si el valor indicado por _lpSPropValueA_ es igual al valor indicado por _lpSPropValueB_. 
    
Para los tipos de propiedad que no tienen ningún orden intrínsecas, como Boolean o error, la función **LPropCompareProp** devuelve un valor undefined si los valores de dos propiedad no son iguales. Este valor undefined es distinto de cero y coherente a través de llamadas. 
  
## <a name="remarks"></a>Comentarios

Use la función **LPropCompareProp** sólo si los tipos de las dos propiedades que se va a comparar son las mismas. 
  
Antes de llamar a **LPropCompareProp**, una aplicación de cliente o un proveedor de servicios en primer lugar debe recuperar las propiedades para realizar una comparación con una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) . Cuando un cliente o proveedor de llamadas **LPropCompareProp**, la función primero examina las etiquetas de propiedad para asegurarse de la comparación de valores de propiedad es válida. La función, a continuación, compara los valores de propiedad, devolver un valor apropiado. 
  
Si los valores de propiedad no son iguales, **LPropCompareProp** determina cuál es el mayor. No es necesario que las propiedades que se comparan **LPropCompareProp** pertenecen al mismo objeto. 
  

