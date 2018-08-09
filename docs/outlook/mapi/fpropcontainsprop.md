---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: abf33e4167d836aeb88fdefb30ba05840e80ce63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816874"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Hace referencia a**: Outlook 
  
Compara dos valores de propiedad, por lo general cadenas o matrices binario, para ver si contiene uno del otro. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parámetros

_lpSPropValueDst_
  
> [entrada] Puntero a una estructura [SPropValue](spropvalue.md) definir el valor de la propiedad que es posible que contienen la cadena de búsqueda que señala el parámetro _lpSPropValueSrc_ . 
    
_lpSPropValueSrc_
  
> [entrada] Puntero a una estructura **SPropValue** definición de la cadena de búsqueda que busca **FPropContainsProp** en el valor de la propiedad indicada por el parámetro _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> [entrada] Configuración de opción definir el nivel de precisión para usar en la comparación. 

  - Los **16 bits inferiores** se aplican a las propiedades de tipo PT_BINARY y PT_STRING8. Debe establecer en exactamente uno de los siguientes valores:
      
    - FL_FULLSTRING: La cadena de búsqueda _lpSPropValueSrc_ debe ser igual que el valor de la propiedad identificado por _lpSPropValueDst_.
        
    - FL_PREFIX: La cadena de búsqueda _lpSPropValueSrc_ debe aparecer al principio del valor de la propiedad identificado por _lpSPropValueDst_. Los dos valores se deben comparar sólo hasta la longitud de la cadena de búsqueda indicada por _lpSPropValueSrc_. 
        
    - FL_SUBSTRING: La cadena de búsqueda _lpSPropValueSrc_ debe estar incluida en cualquier lugar en el valor de la propiedad identificado por _lpSPropValueDst_. 
      
  - Los **16 bits superiores** se aplican sólo a las propiedades de tipo PT_STRING8. Se pueden establecer en los valores siguientes en cualquier combinación:
    
    - FL_IGNORECASE: La comparación debe realizarse sin tener en cuenta entre mayúsculas y minúsculas. 
        
    - FL_IGNORENONSPACE: La comparación debe omitir caracteres sin espacios definidos por el Unicode como marcas diacríticas. 
        
    - FL_LOOSE: La comparación debería indicar una coincidencia siempre que sea posible, mayúsculas de minúsculas sensibilidad y caracteres sin espacios.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Los parámetros son válidos y se encuentra la cadena de búsqueda _lpSPropValueSrc_ como se especifica en el valor de la propiedad _lpSPropValueDst_ . 
    
FALSE 
  
> Los valores de propiedad que se comparan no son de tipo PT_STRING8 o PT_BINARY, los valores de propiedad son de tipos diferentes, o no se encuentra la cadena de búsqueda _lpSPropValueSrc_ como se especifica en el valor de la propiedad _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Comentarios

El método de comparación depende de los tipos de propiedad especificados en las definiciones de propiedad [SPropValue](spropvalue.md) y la heurística nivel aproximada proporcionada en el parámetro _ulFuzzyLevel_ . Las funciones [FPropCompareProp](fpropcompareprop.md) y **FPropContainsProp** se pueden usar para preparar las restricciones para generar una tabla. 
  
Se omiten los 16 bits superiores de _ulFuzzyLevel_ para el tipo de propiedad PT_BINARY. Si la configuración de _ulFuzzyLevel_ está falta o no es válido, se realiza una coincidencia exacta de la cadena completa. Para obtener más información acerca de la contención de propiedad, vea la estructura [SContentRestriction](scontentrestriction.md) . 
  

