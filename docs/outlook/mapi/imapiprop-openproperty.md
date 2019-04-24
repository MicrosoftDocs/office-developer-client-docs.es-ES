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

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> a Etiqueta de propiedad de la propiedad a la que se va a tener acceso. El identificador y el tipo deben incluirse en la etiqueta de propiedad.
    
 _lpiid_
  
> a Puntero al identificador de la interfaz que se va a usar para obtener acceso a la propiedad. El parámetro _lpiid_ no debe ser **nulo**.
    
 _ulInterfaceOptions_
  
> a Datos relacionados con la interfaz identificada por el parámetro _lpiid_ . 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla el acceso a la propiedad. Se pueden establecer los siguientes indicadores:
    
MAPI_CREATE 
  
> Si la propiedad no existe, se debe crear. Si la propiedad existe, se debe descartar el valor actual de la propiedad. Cuando un autor de llamada establece la marca MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProperty** vuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el autor de la llamada. Si el objeto no está disponible, la realización de una llamada de objeto subsiguiente puede generar un error. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY es necesario en estas situaciones:
    
  - Al abrir una propiedad de flujo, como **IID_IStream**, para modificarla.
    
  - Al abrir datos adjuntos de un mensaje incrustado, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) abierto con **IID_IMessage**, para modificarlo.
    
 _lppUnk_
  
> contempla Puntero a la interfaz solicitada que se va a utilizar para el acceso a la propiedad.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El puntero de interfaz solicitado se ha devuelto correctamente.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz solicitada no es compatible con esta propiedad.
    
MAPI_E_NO_ACCESS 
  
> El autor de la llamada no tiene suficientes permisos para obtener acceso a la propiedad.
    
MAPI_E_NO_SUPPORT 
  
> El objeto no puede proporcionar acceso a esta propiedad a través de la interfaz solicitada.
    
MAPI_E_NOT_FOUND 
  
> La propiedad solicitada no existe y MAPI_CREATE no se estableció en el parámetro _ulFlags_ . 
    
MAPI_E_INVALID_PARAMETER 
  
> El tipo de propiedad de la etiqueta se establece en PT_UNSPECIFIED.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIProp:: OpenProperty** proporciona acceso a una propiedad a través de una interfaz determinada. **OpenProperty** es una alternativa a los métodos [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPIProp:: SetProps](imapiprop-setprops.md) . Cuando se produce un error en **GetProps** o **SetProps** porque la propiedad es demasiado grande o demasiado compleja, llame a **OpenProperty**. **OpenProperty** se usa normalmente para obtener acceso a las propiedades de tipo PT Object. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para tener acceso a los datos adjuntos de los mensajes, abra la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) con un identificador de interfaz diferente, según el tipo de datos adjuntos. En la tabla siguiente se describe cómo llamar a **OpenProperty** para los distintos tipos de datos adjuntos: 
  
|**Tipo de datos adjuntos**|**Identificador de interfaz que se va a usar**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Mensaje  <br/> |IID_IMessage  <br/> |
|OLE 2,0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** es un derivado de la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que se basa en un archivo compuesto OLE 2,0. **IStreamDocfile** es la mejor opción para obtener acceso a los datos adjuntos de OLE 2,0 porque implica la menor cantidad de sobrecarga. Puede usar IID_IStreamDocFile para las propiedades que contienen datos almacenados en el almacenamiento estructurado disponible a través de la interfaz [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) . 
  
Para obtener más información acerca de cómo usar **OpenProperty** con datos adjuntos, vea la propiedad **PR_ATTACH_DATA_OBJ** y [abrir datos](opening-an-attachment.md)adjuntos.
  
No use el puntero **IStream** que reciba para llamar a su método [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) o [setSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) a menos que use una variable de tamaño o de posición cero. Además, no confíe en el valor del parámetro de salida _plibNewPosition_ devuelto desde la llamada a **Seek** . 
  
Si llama a **OpenProperty** para tener acceso a una propiedad con la interfaz **IStream** , use sólo esa interfaz para realizar cambios. No intente actualizar la propiedad con ninguno de los otros métodos [IMAPIProp: IUnknown](imapipropiunknown.md) , como **SetProps** o [IMAPIProp::D eleteprops](imapiprop-deleteprops.md). 
  
No intente abrir una propiedad con **OpenProperty** más de una vez. Los resultados no están definidos porque pueden variar de un proveedor a un proveedor. 
  
Si necesita modificar la propiedad que se va a abrir, establezca la marca MAPI_MODIFY. Si no está seguro de si el objeto admite la propiedad pero cree que debería, establezca las marcas MAPI_CREATE y MAPI_MODIFY. Siempre que se establece MAPI_CREATE, se debe establecer MAPI_MODIFY.
  
Usted es responsable de reconvertir el puntero de interfaz devuelto en el parámetro _lppUnk_ en uno que sea adecuado para la interfaz especificada en el parámetro _lpiid_ . También debe usar el puntero devuelto para llamar a su método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) cuando haya terminado. 
  
A veces, la configuración de las marcas en el parámetro _ulFlags_ no es suficiente para indicar el tipo de acceso a la propiedad que se requiere. Puede colocar datos adicionales, como indicadores, en el parámetro _ulInterfaceOptions_ . Estos datos dependen de la interfaz. Algunas interfaces (como **IStream**) la usan y otras no. Por ejemplo, al abrir una propiedad que se va a modificar con **IStream**, establezca la marca STGM_WRITE en el parámetro _ULINTERFACEOPTIONS_ además de MAPI_MODIFY. Al abrir una tabla mediante la interfaz [IMAPITable](imapitableiunknown.md) , puede establecer _ulInterfaceOptions_ en MAPI_UNICODE para indicar si las columnas de la tabla que contienen propiedades de cadena deben estar en formato Unicode. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|StreamEditor. cpp  <br/> |CStreamEditor:: ReadTextStreamFromProperty  <br/> |MFCMAPI usa el método **IMAPIProp:: OpenProperty** para recuperar una interfaz de secuencia para las propiedades binarias y de texto de gran tamaño.  <br/> |
   
## <a name="see-also"></a>Vea también

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
- [Apertura de datos adJuntos](opening-an-attachment.md)

