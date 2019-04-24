---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350735"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca una propiedad especificada en un conjunto de propiedades.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameters

 _rgprop_
  
> a Matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se van a buscar. 
    
 _cprop_
  
> a Número de propiedades en el conjunto de propiedades indicado por el parámetro _rgprop_ . 
    
 _ulPropTag_
  
> a Etiqueta de propiedad de la propiedad que se va a buscar en el conjunto de propiedades indicado por el parámetro _rgprop_ . 
    
## <a name="return-value"></a>Valor devuelto

 **PpropFindProp** devuelve una estructura [SPropValue](spropvalue.md) que define la propiedad que coincide con la etiqueta de propiedad Input o null si no hay ninguna coincidencia. 
  
## <a name="remarks"></a>Comentarios

Si la etiqueta de propiedad dada indica una propiedad de tipo PT_UNSPECIFIED, la función **PpropFindProp** busca una coincidencia solo para el identificador de propiedad en la etiqueta. De lo contrario, busca una coincidencia para toda la etiqueta de propiedad, incluido el tipo de propiedad, y devuelve la propiedad identificada. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: BuildDataItem  <br/> |MFCMAPI usa el método **PpropFindProp** para buscar las propiedades en un conjunto de propiedades que se agrega a la lista.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

