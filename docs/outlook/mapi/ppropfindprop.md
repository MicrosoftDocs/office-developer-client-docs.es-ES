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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820450"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Se aplica a**: Outlook 
  
Establecer las búsquedas para una propiedad especificada en una propiedad.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Sintaxis

 _rgprop_
  
> [entrada] Matriz de estructuras [SPropValue](spropvalue.md) que definen las propiedades que se desea buscar. 
    
 _cprop_
  
> [entrada] Recuento de propiedades en el conjunto de propiedades indicada por el parámetro _rgprop_ . 
    
 _ulPropTag_
  
> [entrada] Etiqueta de propiedad de la propiedad Buscar en el conjunto de propiedades indicado por el parámetro _rgprop_ . 
    
## <a name="return-value"></a>Valor devuelto

 **PpropFindProp** devuelve una estructura [SPropValue](spropvalue.md) definición de la propiedad que coincide con la etiqueta de propiedad de entrada, o NULL si no hay ninguna coincidencia. 
  
## <a name="remarks"></a>Notas

Si la etiqueta de propiedad determinada indica una propiedad de tipo PT_UNSPECIFIED, la función **PpropFindProp** busca a una coincidencia sólo para el identificador de la propiedad en la etiqueta. De lo contrario, busca a una coincidencia para la etiqueta de propiedad completa, incluido el tipo de propiedad y devuelve la propiedad identificada. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI usa el método **PpropFindProp** para buscar establecer propiedades en una propiedad que se agrega a la lista.  <br/> |
   
## <a name="see-also"></a>Ver también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

