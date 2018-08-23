---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5f35474910f2257e18bcdc3b6b1dc661e2dc63a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563978"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a una interfaz que se puede usar para obtener acceso a una propiedad.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parámetros

 _ulPropTag_
  
> [entrada] La etiqueta de propiedad tener acceso a la propiedad. El identificador y el tipo deben ser incluidos en la etiqueta de propiedad.
    
 _lpiid_
  
> [entrada] Un puntero al identificador de la interfaz que se usará para tener acceso a la propiedad. El parámetro _lpiid_ no debe ser **null**.
    
 _ulInterfaceOptions_
  
> [entrada] Datos que se relación con la interfaz identificada mediante el parámetro _lpiid_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el acceso a la propiedad. Se pueden establecer los siguientes indicadores:
    
MAPI_CREATE 
  
> Si la propiedad no existe, se debe crear. Si la propiedad existe, debe descartarse el valor actual de la propiedad. Cuando un autor de la llamada establece la marca MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProperty** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el autor de la llamada. Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY es necesaria en estas situaciones:
    
  - Al abrir una propiedad de secuencia, como **IID_IStream**para modificarla.
    
  - Cuando abra un archivo adjunto de incrustación de mensajes, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) , se abre con **IID_IMessage**, que lo modifique.
    
 _lppUnk_
  
> [out] Un puntero a la interfaz que se usará para el acceso a la propiedad solicitada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El puntero de interfaz solicitada se devolvió correctamente.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz solicitada no se admite para esta propiedad.
    
MAPI_E_NO_ACCESS 
  
> El autor de la llamada no tiene permisos suficientes para tener acceso a la propiedad.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no puede proporcionar acceso a esta propiedad a través de la interfaz solicitada.
    
MAPI_E_NOT_FOUND 
  
> La propiedad solicitada no existe y no se ha establecido MAPI_CREATE en el parámetro _ulFlags indicado_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> El tipo de propiedad en la etiqueta se establece en PT_UNSPECIFIED.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp::OpenProperty** proporciona acceso a una propiedad a través de una interfaz determinada. **OpenProperty** es una alternativa a los métodos [IMAPIProp::GetProps](imapiprop-getprops.md) y [IMAPIProp::SetProps](imapiprop-setprops.md) . Cuando se produce un error debido a que la propiedad es demasiado grande o demasiado compleja **GetProps** o **SetProps** , llamar **OpenProperty**. **OpenProperty** normalmente se usa para tener acceso a las propiedades de tipo pt Object. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para obtener acceso a datos adjuntos de mensajes, abra la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) con un identificador de interfaz diferente, según el tipo de datos adjuntos. En la siguiente tabla se describe cómo llamar a **OpenProperty** para los diferentes tipos de datos adjuntos: 
  
|**Tipo de datos adjuntos**|**Identificador de interfaz que se utiliza**|
|:-----|:-----|
|Binario  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** es un derivado de la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que se basa en un archivo compuesto OLE 2.0. **IStreamDocfile** es la mejor opción para obtener acceso a los datos adjuntos de OLE 2.0, ya que implica la menor cantidad de sobrecarga. Puede usar IID_IStreamDocFile para las propiedades que contienen datos almacenados en almacenamiento estructurado disponible a través de la interfaz [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) . 
  
Para obtener más información acerca de cómo usar **OpenProperty** con datos adjuntos, vea la propiedad **PR_ATTACH_DATA_OBJ** y [Abrir un archivo adjunto](opening-an-attachment.md).
  
No use el puntero **IStream** que reciben para llamar al método su [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) o [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) a menos que utilice una cero variable de tamaño o posición. Además, no se basan en el valor del parámetro de salida _plibNewPosition_ devuelto de la llamada **Seek** . 
  
Si se llama **OpenProperty** para tener acceso a una propiedad con la interfaz **IStream** , use sólo esa interfaz para realizar cambios en él. No intente actualizar la propiedad con cualquiera de las otras [IMAPIProp: IUnknown](imapipropiunknown.md) métodos, como **SetProps** o [IMAPIProp::DeleteProps](imapiprop-deleteprops.md). 
  
No intente abrir una propiedad con **OpenProperty** más de una vez. Los resultados son undefined porque pueden variar de un proveedor a otro. 
  
Si necesita modificar la propiedad que se va a abrir, establecer la marca MAPI_MODIFY. Si no está seguro de si el objeto es compatible con la propiedad pero cree que debería, establezca los indicadores MAPI_CREATE y MAPI_MODIFY. Siempre que se establezca MAPI_CREATE, también se debe establecer MAPI_MODIFY.
  
Usted es responsable de refundición el puntero de interfaz devuelto en el parámetro _lppUnk_ a uno que sea apropiado para la interfaz especificada en el parámetro _lpiid_ . También debe usar el puntero devuelto para llamar al método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) cuando haya terminado con él. 
  
En ocasiones, establecer los marcadores en el parámetro _ulFlags indicado_ no es suficiente para indicar el tipo de acceso a la propiedad que es necesario. Puede colocar datos adicionales, como indicadores, en el parámetro _ulInterfaceOptions_ . Estos datos son dependientes de la interfaz. Algunas interfaces (como **IStream**) usarla y otros no lo hacen. Por ejemplo, cuando se abre una propiedad que se debe modificar con **IStream**, establecer la marca STGM_WRITE en el parámetro _ulInterfaceOptions_ además de MAPI_MODIFY. Cuando se abre una tabla mediante la interfaz [IMAPITable](imapitableiunknown.md) , puede establecer _ulInterfaceOptions_ en MAPI_UNICODE para indicar si las columnas de la tabla que tienen propiedades de cadena deben estar en formato Unicode. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI usa el método **IMAPIProp::OpenProperty** para recuperar una interfaz de secuencia de texto de gran tamaño y propiedades binarias.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
- [Abrir datos adjuntos](opening-an-attachment.md)

