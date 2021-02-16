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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406342"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Busca una propiedad especificada en un conjunto de propiedades.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parámetros

 _rgprop_
  
> [entrada] Matriz de [estructuras SPropValue](spropvalue.md) que definen las propiedades que se buscarán. 
    
 _cprop_
  
> [entrada] Número de propiedades del conjunto de propiedades indicado por el _parámetro rgprop._ 
    
 _ulPropTag_
  
> [entrada] Etiqueta de propiedad de la propiedad que se debe buscar en el conjunto de propiedades indicado por el _parámetro rgprop._ 
    
## <a name="return-value"></a>Valor devuelto

 **PpropFindProp** devuelve una estructura [SPropValue](spropvalue.md) que define la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia. 
  
## <a name="remarks"></a>Comentarios

Si la etiqueta de propiedad determinada indica una propiedad de tipo PT_UNSPECIFIED, la función **PpropFindProp** solo encuentra una coincidencia para el identificador de propiedad en la etiqueta. De lo contrario, busca una coincidencia para la etiqueta de propiedad completa, incluido el tipo de propiedad, y devuelve la propiedad identificada. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI usa el **método PpropFindProp para** buscar propiedades en un conjunto de propiedades que se agrega a la lista.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

