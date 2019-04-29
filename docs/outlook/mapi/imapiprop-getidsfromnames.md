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
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433587"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona los identificadores de propiedad que corresponden a uno o más nombres de propiedad.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Parameters

 _cPropNames_
  
> a El número de nombres de propiedad a los que apunta el parámetro _lppPropNames_ . Si _lppPropNames_ es null, el parámetro _cPropNames_ debe ser 0. 
    
 _lppPropNames_
  
> a Un puntero a una matriz de nombres de propiedad o NULL. Pasar identificadores de propiedad de solicitudes NULL para todos los nombres de propiedad en todos los conjuntos de propiedades sobre los que el objeto tiene información. El parámetro _lppPropNames_ no debe ser null si el indicador MAPI_CREATE está establecido en el parámetro _ulFlags_ . 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que indica cómo se deben devolver los identificadores de propiedad. Se puede establecer la siguiente marca:
    
MAPI_CREATE 
  
> Asigna un identificador de propiedad, si aún no se ha asignado ninguno, a uno o varios de los nombres incluidos en la matriz de nombres de propiedad a la que apunta _lppPropNames_. Esta marca registra internamente el identificador en la tabla de asignación de nombre a identificador.
    
 _lppPropTags_
  
> contempla Un puntero a un puntero a una matriz de etiquetas de propiedad que contiene los identificadores de propiedad existentes o recién asignados. Los tipos de propiedad de las etiquetas de propiedad de esta matriz se establecen en **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los identificadores de los nombres de propiedad especificados se han devuelto correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no admite propiedades con nombre.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Memoria inSuficiente para recuperar los identificadores.
    
MAPI_E_TOO_BIG 
  
> No se puede realizar la operación porque requiere que se devuelvan demasiadas etiquetas de propiedad.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó en general, pero no se pudieron devolver uno o más identificadores de propiedad. El tipo de propiedad correspondiente para cada propiedad no disponible se establece en **PT_ERROR** y su identificador en cero. Cuando se devuelve esta advertencia, controlar la llamada correctamente. Para probar esta advertencia, use la macro **HR_FAILED** . Consulte [uso de macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: GetIDsFromNames** recupera una matriz de etiquetas de propiedad que contiene los identificadores de propiedad para una o más propiedades con nombre. Se puede llamar a **IMAPIProp:: GetIDsFromNames** para hacer lo siguiente: 
  
- Crear identificadores para los nombres nuevos.
    
- Recuperar identificadores para nombres específicos.
    
- Recupere los identificadores de todas las propiedades con nombre que se incluyen en la asignación del objeto.
    
Los proveedores de almacenamiento de mensajes suelen usar las propiedades con nombre para las carpetas y los mensajes. Es posible que otros objetos, como usuarios de mensajería y secciones de perfil, no admitan la Asociación de nombres con los identificadores de propiedad y puedan devolver MAPI_E_NO_SUPPORT de **GetIDsFromNames**.
  
Si hay un error que devuelve un identificador para un nombre en particular, **GetIDsFromNames** devuelve MAPI_W_ERRORS_RETURNED y establece el tipo de propiedad en la entrada de matriz de etiquetas de propiedad que corresponde al nombre a **PT_ERROR** y el identificador a cero. 
  
La asignación de nombre a identificador se representa mediante la propiedad **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de un objeto. **PR_MAPPING_SIGNATURE** contiene una estructura [MAPIUID](mapiuid.md) que indica el proveedor de servicios responsable del objeto. Si la propiedad **PR_MAPPING_SIGNATURE** es la misma para dos objetos, supongamos que estos objetos usan la misma asignación de nombre a identificador. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Los identificadores que se devuelven en la matriz de etiquetas de propiedad a la que señala el parámetro _lppPropNames_ deben estar en el intervalo de 0X8000 a 0xFFFE. Las entradas de esta matriz deben estar en el mismo orden que los nombres pasados en la matriz de nombres de propiedad a la que señala _lppPropNames_. 
  
Si admite propiedades con nombre en un contenedor, use la misma asignación de nombre a identificador para todos los objetos del contenedor (es decir, no use una asignación diferente para cada carpeta del almacén de mensajes o cada mensaje de la carpeta).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Debido a que los tipos de propiedad de los identificadores devueltos en la matriz de etiquetas de propiedad a la que apunta _lppPropTags_ se establecen en **PT_UNSPECIFIED**, deberá llamar al método [IMAPIProp:: SetProps](imapiprop-setprops.md) para recuperar los tipos precisos. 
  
Si mueve o copia objetos con propiedades con nombre y los objetos de origen y de destino tienen distintas firmas de asignación, tal y como indican los valores de sus propiedades **PR_MAPPING_SIGNATURE** , debe conservar los nombres durante estas operaciones. Para conservar los nombres de propiedad, ajuste los identificadores de propiedad correspondientes para que correspondan a la asignación de nombre a identificador del objeto de destino. 
  
Algunos objetos tienen un límite en cuanto al número de identificadores de propiedad a los que se puede asignar nombre. Si una llamada a **GetIDsFromNames** hace que se supere este límite, el método devuelve MAPI_E_TOO_BIG. En este caso, consulte por identificador. 
  
Para obtener más información, consulte [MAPI con nombre de propiedades](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed  <br/> |MFCMAPI usa el método **IMAPIProp:: GetIDsFromNames** para obtener etiquetas de propiedad para todas las propiedades con nombre que se han asignado.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Propiedades con nombre MAPI](mapi-named-properties.md)
  
[Uso de macros para el control de errores](using-macros-for-error-handling.md)

