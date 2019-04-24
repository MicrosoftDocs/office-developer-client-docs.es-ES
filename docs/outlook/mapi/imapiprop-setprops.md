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
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341016"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Actualiza una o más propiedades.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _cValues_
  
> a El número de valores de propiedad a los que apunta el parámetro _lpPropArray_ . El parámetro _cValues_ no debe ser 0. 
    
 _lpPropArray_
  
> a Un puntero a una matriz de estructuras [SPropValue](spropvalue.md) que contiene los valores de propiedad que se van a actualizar. 
    
 _lppProblems_
  
> [in, out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no es necesaria información de error. Si _lppProblems_ es un puntero válido en la entrada, **SetProps** devuelve información detallada sobre los errores de actualización de una o varias propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se actualizaron correctamente.
    
Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para **SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_COMPUTED 
  
> La propiedad no se puede actualizar porque es de solo lectura, calculada por el proveedor de servicios responsable del objeto.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar un objeto de solo lectura o tener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> La propiedad no se puede actualizar porque es mayor que el tamaño del búfer de la llamada a procedimiento remoto (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por la implementación que realiza la llamada.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Ignore la etiqueta de propiedad **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) y todas las propiedades con un tipo de **PT_ERROR**. No realice cambios ni informe de problemas en la estructura **SPropProblemArray** . 
  
Devuelve MAPI_E_INVALID_PARAMETER si una propiedad de tipo **PT Object** se incluye en la matriz de valores de propiedad. También devuelve este error si se incluye una propiedad de varios valores en la matriz y su miembro **cValues** se establece en 0. 
  
Si la llamada se realiza correctamente, pero hay problemas para establecer algunas de las propiedades, devuelva S_OK y coloque la información sobre los problemas en la entrada correspondiente a la estructura **SPropProblemArray** a la que apunta el parámetro _lppProblems_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Dependiendo del proveedor de servicios, es posible que también pueda cambiar el tipo de propiedad pasando una etiqueta de propiedad que contenga un tipo diferente de la utilizada anteriormente con un identificador de propiedad determinado.
  
Si incluye una etiqueta de propiedad para una propiedad que no es compatible con el objeto y la implementación de **SetProps** permite la creación de nuevas propiedades, la propiedad se agrega al objeto. Se descarta cualquier valor anterior almacenado con el identificador de propiedad usado para la nueva propiedad. 
  
Tenga en cuenta que el valor devuelto S_OK no garantiza que todas las propiedades se actualicen correctamente. Algunos proveedores llaman a **SetProps** de caché hasta que reciben una llamada que requiere la intervención del proveedor, como [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) o [IMAPIProp:: GetProps](imapiprop-getprops.md). Por lo tanto, es posible recibir valores de error relacionados con la llamada de **SetProps** con las llamadas posteriores. 
  
Si **SetProps** Devuelve S_OK, Compruebe la estructura **SPropProblemArray** apuntado por _lppProblems_ para ver si hay problemas al actualizar propiedades individuales. Si **SetProps** devuelve un error, no Compruebe la matriz de problemas de propiedad. En su lugar, llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) del objeto. 
  
Cuando se actualizan propiedades de gran tamaño, **SetProps** puede producir un error y devolver MAPI_E_NOT_ENOUGH_MEMORY. No hay ningún tamaño máximo para las propiedades y los distintos objetos pueden tener distintos límites. Si trabaja con propiedades potencialmente grandes, prepárese para llamar al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con IID_IStream como identificador de interfaz si **SetProps** devuelve este valor de error. 
  
Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la estructura **SPropProblemArray** . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Editor. cpp  <br/> |CPropertyEditor:: WriteSPropValueToObject  <br/> |MFCMAPI usa el método **IMAPIProp:: SetProps** para volver a escribir una propiedad en un objeto después de que se haya editado la propiedad.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

