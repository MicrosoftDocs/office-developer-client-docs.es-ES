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
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319813"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero a una interfaz que se puede usar para tener acceso a una propiedad.
  
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
  
> [entrada] La etiqueta de propiedad de la propiedad a la que se va a tener acceso. Tanto el identificador como el tipo deben incluirse en la etiqueta de propiedad.
    
 _lpiid_
  
> [entrada] Puntero al identificador de la interfaz que se usará para tener acceso a la propiedad. El _parámetro lpiid_ no debe ser **nulo.**
    
 _ulInterfaceOptions_
  
> [entrada] Datos relacionados con la interfaz identificada por el _parámetro lpiid._ 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el acceso a la propiedad. Se pueden establecer las siguientes marcas:
    
MAPI_CREATE 
  
> Si la propiedad no existe, debe crearse. Si la propiedad existe, se debe descartar el valor actual de la propiedad. Cuando un autor de la MAPI_CREATE establece la marca de MAPI_MODIFY, también debe establecerla.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenProperty** vuelva correctamente, posiblemente antes de que el objeto esté totalmente disponible para el autor de la llamada. Si el objeto no está disponible, realizar una llamada a objeto posterior puede generar un error. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY se requiere en estas situaciones:
    
  - Al abrir una propiedad de secuencia, **como IID_IStream**, para modificarla.
    
  - Al abrir un archivo adjunto de mensaje incrustado, [como PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) abierto **con IID_IMessage**, para modificarlo.
    
 _lppUnk_
  
> [salida] Puntero a la interfaz solicitada que se usará para el acceso a propiedades.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El puntero de interfaz solicitado se devolvió correctamente.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz solicitada no es compatible con esta propiedad.
    
MAPI_E_NO_ACCESS 
  
> El autor de la llamada no tiene permisos suficientes para acceder a la propiedad.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no puede proporcionar acceso a esta propiedad a través de la interfaz solicitada.
    
MAPI_E_NOT_FOUND 
  
> La propiedad solicitada no existe y MAPI_CREATE no se estableció en el _parámetro ulFlags._ 
    
MAPI_E_INVALID_PARAMETER 
  
> El tipo de propiedad de la etiqueta se establece en PT_UNSPECIFIED.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIProp::OpenProperty** proporciona acceso a una propiedad a través de una interfaz determinada. **OpenProperty** es una alternativa a los [métodos IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps.](imapiprop-setprops.md) Cuando se **produce un error en GetProps** o **SetProps** porque la propiedad es demasiado grande o demasiado compleja, llame **a OpenProperty**. **OpenProperty** se usa normalmente para tener acceso a propiedades de tipo PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para obtener acceso a los datos adjuntos de los **mensajes,** abra la propiedad PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) con un identificador de interfaz diferente, según el tipo de datos adjuntos. En la tabla siguiente se describe cómo llamar **a OpenProperty para** los distintos tipos de datos adjuntos: 
  
|**Tipo de datos adjuntos**|**Identificador de interfaz que se usará**|
|:-----|:-----|
|Binario  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Mensaje  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** es una derivada de la [interfaz IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que se basa en un archivo compuesto OLE 2.0. **IStreamDocfile** es la mejor opción para obtener acceso a datos adjuntos ole 2.0 porque implica la menor cantidad de sobrecarga. Puede usar el IID_IStreamDocFile para las propiedades que contienen datos almacenados en almacenamiento estructurado disponible a través de la [interfaz IStorage.](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) 
  
Para obtener más información acerca de cómo usar **OpenProperty** con datos adjuntos, vea la propiedad **PR_ATTACH_DATA_OBJ** y [Abrir datos adjuntos.](opening-an-attachment.md)
  
No use el puntero **IStream** que recibe para llamar a su [método Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) o [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) a menos que use una variable de posición cero o tamaño. Además, no confíe en el valor del parámetro de salida _plibNewPosition_ devuelto desde la **llamada Seek.** 
  
Si llamas **a OpenProperty para** obtener acceso a una propiedad con la interfaz **IStream,** usa solo esa interfaz para realizar cambios en ella. No intente actualizar la propiedad con ninguno de los otros métodos [IMAPIProp : IUnknown,](imapipropiunknown.md) como **SetProps** o [IMAPIProp::D eleteProps](imapiprop-deleteprops.md). 
  
No intente abrir una propiedad con **OpenProperty** más de una vez. Los resultados no están definidos porque pueden variar de un proveedor a otro. 
  
Si necesita modificar la propiedad que se va a abrir, establezca MAPI_MODIFY marca. Si no está seguro de si el objeto admite la propiedad pero cree que debe hacerlo, establezca los MAPI_CREATE y MAPI_MODIFY marcas. Siempre MAPI_CREATE se establece, MAPI_MODIFY también debe establecerse.
  
Usted es responsable de volver a convertir el puntero de interfaz devuelto en el parámetro _lppUnk_ a uno adecuado para la interfaz especificada en el parámetro _lpiid._ También debe usar el puntero devuelto para llamar a su [método IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) cuando haya terminado con él. 
  
A veces, establecer las marcas en  _el parámetro ulFlags_ no es suficiente para indicar el tipo de acceso a la propiedad que es necesaria. Puedes colocar datos adicionales, como marcas, en el _parámetro ulInterfaceOptions._ Estos datos dependen de la interfaz. Algunas interfaces (como **IStream)** la usan y otras no. Por ejemplo, cuando abra una propiedad que se modificará con **IStream,** establezca la marca STGM_WRITE en el parámetro  _ulInterfaceOptions_ además de MAPI_MODIFY. Al abrir una tabla mediante la interfaz [IMAPITable,](imapitableiunknown.md) puede establecer  _ulInterfaceOptions_ en MAPI_UNICODE para indicar si las columnas de la tabla que contienen propiedades de cadena deben estar en formato Unicode. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI usa el **método IMAPIProp::OpenProperty** para recuperar una interfaz de secuencia para texto grande y propiedades binarias.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
- [Abrir datos adjuntos](opening-an-attachment.md)

