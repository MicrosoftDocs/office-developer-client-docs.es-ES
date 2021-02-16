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
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432635"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos valores de propiedad, generalmente cadenas o matrices binarias, para ver si uno contiene el otro. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parámetros

_lpSPropValueDst_
  
> [entrada] Puntero a una [estructura SPropValue](spropvalue.md) que define el valor de propiedad que puede contener la cadena de búsqueda a la que apunta el parámetro _lpSPropValueSrc._ 
    
_lpSPropValueSrc_
  
> [entrada] Puntero a una **estructura SPropValue** que define la cadena de búsqueda que **FPropContainsProp** busca en el valor de propiedad al que apunta el parámetro _lpSPropValueDst._ 
    
_ulFuzzyLevel_
  
> [entrada] Configuración de opciones que define el nivel de precisión que se debe usar en la comparación. 

  - Los **16 bits inferiores se** aplican a las propiedades de tipo PT_BINARY y PT_STRING8. Deben establecerse exactamente en uno de los siguientes valores:
      
    - FL_FULLSTRING: la cadena  _de búsqueda lpSPropValueSrc_ debe ser igual al valor de propiedad identificado por  _lpSPropValueDst_.
        
    - FL_PREFIX: la cadena de búsqueda  _lpSPropValueSrc_ debe aparecer al principio del valor de propiedad identificado por  _lpSPropValueDst_. Los dos valores deben compararse solo hasta la longitud de la cadena de búsqueda indicada por  _lpSPropValueSrc_. 
        
    - FL_SUBSTRING: la cadena de búsqueda  _lpSPropValueSrc_ debe estar contenida en cualquier parte del valor de propiedad identificado por  _lpSPropValueDst_. 
      
  - Los **16 bits superiores** solo se aplican a las propiedades de tipo PT_STRING8. Se pueden establecer en los siguientes valores en cualquier combinación:
    
    - FL_IGNORECASE: la comparación debe realizarse sin tener en cuenta la diferencia entre mayúsculas y minúsculas. 
        
    - FL_IGNORENONSPACE: la comparación debe omitir los caracteres no válidos definidos por Unicode, como los signos diacríticos. 
        
    - FL_LOOSE: la comparación debe indicar una coincidencia siempre que sea posible, ignorando la confidencialidad de mayúsculas y minúsculas y los caracteres que no coinciden.
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Todos los parámetros son válidos y la cadena de búsqueda _lpSPropValueSrc_ se incluye como se especifica en el valor de la propiedad _lpSPropValueDst._ 
    
FALSE 
  
> Los valores de propiedad que se están comparando no son del tipo PT_STRING8 o PT_BINARY, los valores de propiedad son de diferentes tipos o la cadena de búsqueda _lpSPropValueSrc_ no está contenida como se especifica en el valor de la propiedad _lpSPropValueDst._ 
    
## <a name="remarks"></a>Comentarios

El método de comparación depende de los tipos de propiedad especificados en las definiciones de la propiedad [SPropValue](spropvalue.md) y del nivel aproximada heurístico proporcionado en el _parámetro ulFuzzyLevel._ Las [funciones FPropCompareProp](fpropcompareprop.md) y **FPropContainsProp** se pueden usar para preparar restricciones para generar una tabla. 
  
Los 16 bits superiores de  _ulFuzzyLevel_ se omiten para el tipo de propiedad PT_BINARY. Si falta la configuración  _de ulFuzzyLevel_ o no es válida, se realiza una coincidencia exacta de cadena completa. Para obtener más información acerca de la contención de propiedades, vea la [estructura SContentRestriction.](scontentrestriction.md) 
  

