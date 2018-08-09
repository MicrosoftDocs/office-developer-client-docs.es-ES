---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0457007334ad8cc69dade3abd5859dd0d5f7af7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817406"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Hace referencia a**: Outlook 
  
Devuelve las etiquetas de propiedad para todas las propiedades. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el formato de las cadenas en las etiquetas de propiedades que se devuelven. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> Las cadenas devueltas están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
 _lppPropTagArray_
  
> [out] Un puntero a un puntero a la matriz de la etiqueta de propiedad que contiene las etiquetas para todas las propiedades del objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se han devuelto todas las etiquetas de propiedad correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp::GetPropList** recupera la etiqueta de propiedad para cada propiedad actualmente admitido por un objeto. Si el objeto no es compatible actualmente con todas las propiedades, **GetPropList** devuelve una matriz de etiqueta de propiedad con el miembro **cValues** establece en 0. 
  
El ámbito de las propiedades devueltas por **GetPropList** varía en función de un proveedor a otro. Algunos proveedores de servicios de excluyen esas propiedades para que el autor de la llamada no tiene acceso. Todos los proveedores de devolverán las propiedades de tipo **pt Object**.
  
Si el objeto no es compatible con Unicode, **GetPropList** devuelve MAPI_E_BAD_CHARWIDTH, incluso si no hay ninguna propiedad de cadena definida para el objeto. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Los proveedores de transporte remoto implementan **GetPropList** exactamente como se especifica aquí. No existen problemas especiales. La implementación debe, devolver por supuesto, la misma lista de propiedades como compatible con el método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de etiqueta de propiedad que señala _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa el método **IMAPIProp::GetPropList** para obtener una lista de propiedades que se pase a **GetProps**.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

