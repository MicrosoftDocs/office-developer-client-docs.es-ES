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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412621"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Actualiza una o varias propiedades.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parámetros

 _cValues_
  
> [entrada] Recuento de valores de propiedad a los que apunta el _parámetro lpPropArray._ El  _parámetro cValues_ no debe ser 0. 
    
 _lpPropArray_
  
> [entrada] Puntero a una matriz de [estructuras SPropValue](spropvalue.md) que contienen valores de propiedad que se actualizarán. 
    
 _lppProblems_
  
> [entrada, salida] En la entrada, un puntero a un puntero a una [estructura SPropProblemArray;](spropproblemarray.md) de lo contrario, NULL, que indica que no es necesario obtener información de error. Si  _lppProblems_ es un puntero válido en la entrada, **SetProps** devuelve información detallada acerca de los errores al actualizar una o más propiedades. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las propiedades se actualizaron correctamente.
    
Los siguientes valores se pueden devolver en la estructura **SPropProblemArray,** pero no como valores devueltos para **SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_COMPUTED 
  
> La propiedad no se puede actualizar porque es de solo lectura, calculada por el proveedor de servicios responsable del objeto.
    
MAPI_E_INVALID_TYPE 
  
> El tipo de propiedad no es válido.
    
MAPI_E_NO_ACCESS 
  
> Se intentó modificar un objeto de solo lectura o obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> La propiedad no se puede actualizar porque es mayor que el tamaño del búfer de llamada a procedimiento remoto (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> El tipo de propiedad no es el tipo esperado por la implementación de llamada.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Ignore la **etiqueta PR_NULL** propiedad ([PidTagNull](pidtagnull-canonical-property.md)) y todas las propiedades con un tipo **de PT_ERROR**. No realice cambios ni informe de problemas en la **estructura SPropProblemArray.** 
  
Devuelve MAPI_E_INVALID_PARAMETER si se incluye una propiedad de **tipo PT_OBJECT** en la matriz de valores de propiedad. Devuelve también este error si se incluye una propiedad de varios valores en la matriz y su **miembro cValues** está establecido en 0. 
  
Si la llamada se realiza correctamente en general, pero hay problemas con la configuración de algunas de las propiedades, devuelva S_OK y coloque información sobre los problemas en la entrada adecuada de la estructura **SPropProblemArray** a la que apunta el parámetro _lppProblems._ 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Según el proveedor de servicios, es posible que también pueda cambiar el tipo de propiedad pasando una etiqueta de propiedad que contenga un tipo diferente del que se usó anteriormente con un identificador de propiedad determinado.
  
Si incluye una etiqueta de propiedad para una propiedad que no es compatible con el objeto y la implementación de **SetProps** permite la creación de nuevas propiedades, la propiedad se agrega al objeto. Se descarta cualquier valor anterior almacenado con el identificador de propiedad que se usó para la nueva propiedad. 
  
Tenga en cuenta que S_OK valor devuelto no garantiza que todas las propiedades se actualizaron correctamente. Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md). Por lo tanto, es posible recibir valores de error relacionados con la llamada **SetProps** con las llamadas posteriores. 
  
Si **SetProps** devuelve S_OK, compruebe la estructura **SPropProblemArray** a la que  _apunta lppProblems_ en busca de problemas para actualizar propiedades individuales. Si **SetProps devuelve** un error, no compruebe la matriz del problema de la propiedad. En su lugar, llame al método [IMAPIProp::GetLastError del](imapiprop-getlasterror.md) objeto. 
  
Al actualizar propiedades de gran tamaño, **SetProps** puede producir un error y devolver MAPI_E_NOT_ENOUGH_MEMORY. No hay un tamaño máximo para las propiedades y los distintos objetos pueden tener límites diferentes. Si se trata de propiedades potencialmente grandes, esté preparado para llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con IID_IStream como identificador de interfaz si **SetProps** devuelve este valor de error. 
  
Llama a [la función MAPIFreeBuffer](mapifreebuffer.md) para liberar la **estructura SPropProblemArray.** 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI usa el **método IMAPIProp::SetProps** para volver a escribir una propiedad en un objeto después de editar la propiedad.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

