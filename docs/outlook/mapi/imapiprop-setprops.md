---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817412"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Hace referencia a**: Outlook 
  
Actualiza las propiedades de uno o más.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parámetros

 _cValues_
  
> [entrada] El recuento de valores de la propiedad indicada por el parámetro _lpPropArray_ . El parámetro _cValues_ no debe ser 0. 
    
 _lpPropArray_
  
> [entrada] Un puntero a una matriz de estructuras [SPropValue](spropvalue.md) que contienen valores de propiedad para actualizarse. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no hay necesidad de información de error. Si _lppProblems_ es un puntero válido en la entrada, **SetProps** devuelve información detallada acerca de los errores en la actualización de una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se han actualizado correctamente.
    
Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.
    
MAPI_E_COMPUTED 
  
> La propiedad no se puede actualizar porque es de sólo lectura, calculada por el proveedor de servicios que es responsable del objeto.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado para modificar un objeto de sólo lectura o para obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> La propiedad no se puede actualizar porque es mayor que el tamaño de búfer de procedimiento remoto (RPC) de la llamada.
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por la implementación de la llamada.
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

Omitir la etiqueta de propiedad de **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) y todas las propiedades con un tipo de **PT_ERROR**. No realice cambios o informar de los problemas en la estructura **SPropProblemArray** . 
  
Devolver MAPI_E_INVALID_PARAMETER si una propiedad de tipo **pt Object** está incluida en la matriz de valores de propiedad. También se devuelven este error si se incluye una propiedad de varios valores en la matriz y sus miembros **cValues** se establece en 0. 
  
Si la llamada se realiza correctamente en general, pero hay problemas con la configuración de algunas de las propiedades, devuelve S_OK y colocar la información acerca de los problemas en la entrada correspondiente de la estructura de **SPropProblemArray** que señala el parámetro _lppProblems_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Según el proveedor de servicio, es posible que también podrá cambiar el tipo de propiedad, se pasa una etiqueta de propiedad que contiene un tipo diferente que se utilizó anteriormente con un identificador de la propiedad determinada.
  
Si incluye una etiqueta de propiedad para una propiedad que no es compatible con el objeto y la implementación de **SetProps** permite la creación de nuevas propiedades, la propiedad se agrega al objeto. Se descarta cualquier valor anterior almacenado con el identificador de la propiedad que se usó para la nueva propiedad. 
  
Tenga en cuenta que el valor devuelto de S_OK no garantiza que todas las propiedades se han actualizado correctamente. Algunos proveedores de la memoria caché **SetProps** llamadas hasta que reciben una llamada que requiere la intervención del proveedor, como [IMAPIProp::SaveChanges](imapiprop-savechanges.md) o [IMAPIProp::GetProps](imapiprop-getprops.md). Por lo tanto, es posible recibir los valores de error que se relacionan con la llamada **SetProps** con las llamadas posteriores. 
  
Si **SetProps** devuelve S_OK, compruebe la estructura de **SPropProblemArray** que señala _lppProblems_ para problemas de actualización de las propiedades individuales. Si **SetProps** devuelve un error, no comprobar la matriz de problema (propiedad). En su lugar, llame al método del objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
  
Al actualizar las propiedades de gran tamaño, **SetProps** puede producir un error y devolver MAPI_E_NOT_ENOUGH_MEMORY. No hay ningún tamaño máximo para las propiedades y objetos diferentes pueden tener distintos límites. Si se trabaja con las propiedades potencialmente grandes, estar preparado para llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con IID_IStream como el identificador de interfaz si **SetProps** devuelve este valor de error. 
  
Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la estructura **SPropProblemArray** . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI usa el método **IMAPIProp::SetProps** volver a escribir una propiedad en un objeto después de que la propiedad se ha editado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

