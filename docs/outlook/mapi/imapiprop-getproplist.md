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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316572"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve las etiquetas de propiedad de todas las propiedades. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el formato de las cadenas en las etiquetas de propiedad devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas devueltas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _lppPropTagArray_
  
> contempla Un puntero a un puntero a la matriz de etiquetas de propiedades que contiene las etiquetas de todas las propiedades del objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Todas las etiquetas de propiedad se devolvieron correctamente.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: GetPropList** recupera la etiqueta de propiedad para cada propiedad admitida actualmente por un objeto. Si el objeto no admite actualmente ninguna propiedad, **GetPropList** devuelve una matriz de etiquetas de propiedad con el miembro **cValues** establecido en 0. 
  
El ámbito de las propiedades devueltas por **GetPropList** varía de un proveedor a un proveedor. Algunos proveedores de servicios excluyen las propiedades para las que el autor de la llamada no tiene acceso. Todos los proveedores devuelven propiedades de tipo **PT Object**.
  
Si el objeto no admite Unicode, **GetPropList** devuelve MAPI_E_BAD_CHARWIDTH, incluso si no hay ninguna propiedad de cadena definida para el objeto. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los proveedores de transporte remoto implementan **GetPropList** exactamente como se especifica aquí. No hay ninguna preocupación especial. Por supuesto, la implementación debe devolver la misma lista de propiedades que admita el método [IMAPIProp:: GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la matriz de etiquetas de propiedad a la que apunta _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI usa el método **IMAPIProp:: GetPropList** para obtener una lista de propiedades para pasar a **GetProps**.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

