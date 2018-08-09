---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817414"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Hace referencia a**: Outlook 
  
Proporciona los identificadores de propiedad que se corresponden con uno o varios nombres de propiedad.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Parámetros

 _cPropNames_
  
> [entrada] El recuento de nombres de propiedad que señala el parámetro _lppPropNames_ . Si _lppPropNames_ es NULL, el parámetro _cPropNames_ debe ser 0. 
    
 _lppPropNames_
  
> [entrada] Un puntero a una matriz de nombres de propiedad o NULL. Si se pasa NULL solicita identificadores de propiedad para todos los nombres de propiedad en todos los conjuntos de propiedades acerca de que el objeto tiene información. El parámetro _lppPropNames_ no debe ser NULL si la marca MAPI_CREATE se establece en el parámetro _ulFlags indicado_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de marcadores que indica cómo se deben devolver los identificadores de propiedad. Se puede establecer la marca siguiente:
    
MAPI_CREATE 
  
> Asigna un identificador de la propiedad, si uno aún no se ha asignado, a uno o varios de los nombres incluidos en la matriz de nombre de propiedad que señala _lppPropNames_. Esta marca internamente registra el identificador en la tabla de asignación de nombre a identificador.
    
 _lppPropTags_
  
> [out] Un puntero a un puntero a una matriz de etiquetas (propiedad) que contiene los identificadores de propiedad existente o recién asignados. Los tipos de propiedad para las etiquetas de propiedad de esta matriz se establecen en **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los identificadores de los nombres de propiedad especificado correctamente se han devuelto.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite propiedades con nombre.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Memoria insuficiente estaba disponible para recuperar los identificadores.
    
MAPI_E_TOO_BIG 
  
> No se puede realizar la operación, ya que requiere demasiadas etiquetas de propiedad que se va a devolver.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada satisfactoria, pero no se podrían devolver uno o varios identificadores de propiedad. El tipo de propiedad correspondiente para cada propiedad no está disponible se establece en **PT_ERROR** y su identificador en cero. Cuando se devuelve esta advertencia, controlar la llamada como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Vea [uso de Macros para el tratamiento de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp::GetIDsFromNames** recupera una matriz de etiquetas de propiedad que mantenga los identificadores de propiedad para una o varias propiedades con nombre. Puede llamar a **IMAPIProp::GetIDsFromNames** para hacer lo siguiente: 
  
- Crear identificadores para nombres nuevos.
    
- Recuperar identificadores de nombres específicos.
    
- Recuperar los identificadores de todas las propiedades con nombre que se incluyen en la asignación del objeto.
    
Propiedades con nombre se usan normalmente por los proveedores de almacén de mensajes para las carpetas y mensajes. Otros objetos, como la mensajería de los usuarios y las secciones de perfil, puede que no admita la asociación de los nombres de los identificadores de propiedades y podrían devolver MAPI_E_NO_SUPPORT de **a GetIDsFromNames**.
  
Si se ha producido un error que devuelve un identificador para un nombre en particular, **a GetIDsFromNames** devuelve MAPI_W_ERRORS_RETURNED y establece el tipo de propiedad en la entrada de matriz de etiqueta de propiedad que se corresponde con el nombre **PT_ERROR** y el identificador a cero. 
  
Asignación de nombre a identificador está representado por una propiedad del objeto **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)). **PR_MAPPING_SIGNATURE** contiene una estructura [MAPIUID](mapiuid.md) que indica el proveedor de servicio responsable del objeto. Si la propiedad **PR_MAPPING_SIGNATURE** es el mismo para dos objetos, se supone que estos objetos utilizan la misma asignación de nombre a identificador. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Los identificadores que se pasan en la matriz de etiqueta de la propiedad indicada por el parámetro _lppPropNames_ deben estar en el intervalo de 0 x 8000 a 0xFFFE. Las entradas de esta matriz deben estar en el mismo orden que los nombres pasados en la matriz de nombre de la propiedad indicadas por _lppPropNames_. 
  
Si decide admitir propiedades con nombre en un contenedor, utilice la misma asignación de nombre a identificador para todos los objetos en el contenedor (es decir, no use una asignación distinta para cada carpeta en el almacén de mensajes o cada mensaje en la carpeta).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Debido a que los tipos de propiedad para los identificadores devueltos en la matriz de etiqueta de propiedad que señala _lppPropTags_ se establecen en **PT_UNSPECIFIED**, debe llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) para recuperar los tipos precisos. 
  
Si mover o copiar objetos con propiedades con nombre y los objetos de origen y de destino tienen firmas de asignación distinta indicada por los valores de sus propiedades **PR_MAPPING_SIGNATURE** , debe conservar los nombres durante estas operaciones. Para conservar los nombres de propiedad, ajustar los identificadores de propiedad correspondientes para que coincidan con la asignación del identificador del nombre del objeto de destino. 
  
Algunos objetos tienen un límite en el número de identificadores de propiedad que se puede asignar el nombre. Si una llamada a **GetIDsFromNames** hace que se supere este límite, el método devuelve MAPI_E_TOO_BIG. En este caso, la consulta por identificador. 
  
Para obtener más información, vea [Propiedades de nombre de MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI utiliza el método **IMAPIProp::GetIDsFromNames** para obtener las etiquetas de propiedad para todas las propiedades con nombre que se han asignado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Con el nombre de las propiedades de MAPI](mapi-named-properties.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

