---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348926"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llamado por un proveedor de transporte para iniciar una sesión de formato TNEF (Transport neutral Encapsulation Format) de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de transporte  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Parameters

_lpvSupport_
  
> a Pasa un objeto de soporte o pasa NULL. 
    
_lpStream_
  
> a Puntero a una interfaz OLE **IStream** del objeto de la secuencia de almacenamiento que proporciona un origen o un destino para un mensaje de transmisión TNEF. 
    
_lpszStreamName_
  
> a Puntero al nombre de la secuencia de datos que usa el objeto TNEF. Si el autor de la llamada ha establecido el indicador TNEF_ENCODE ( _ulFlags_ ) en su llamada a **OpenTnefStream**, el parámetro _lpszName_ debe especificar un puntero que no sea nulo a una cadena que no sea NULL y que consista en cualquier carácter que se considere válido para el nombre de un archivo. MAPI no permite nombres de cadena que incluyan los caracteres "[", "]" o ":", incluso si el sistema de archivos permite su uso. El tamaño de la cadena pasada para _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso. 
    
_ulFlags_
  
> a Máscara de las marcas usadas para indicar el modo de la función. Se pueden establecer los siguientes indicadores:
    
TNEF_BEST_DATA 
  
> Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en las encapsulaciones. Tenga en cuenta que esto hará que se duplique la información del flujo TNEF. TNEF_BEST_DATA es el valor predeterminado si no se especifican otros modos. 
    
TNEF_COMPATIBILITY 
  
> Proporciona compatibilidad con versiones anteriores con las aplicaciones cliente más antiguas. Las secuencias TNEF codificadas con este indicador asignarán todas las propiedades posibles al atributo de bajo nivel correspondiente. Este modo también hace que el valor predeterminado de algunas propiedades que los clientes de nivel inferior requieran. 
    
  > [!CAUTION]
  > Esta marca está obsoleta y no debe usarse. 
  
TNEF_DECODE 
  
> El objeto TNEF en la secuencia indicada se abre con acceso de solo lectura. El proveedor de transporte debe establecer esta marca si desea que la función inicialice el objeto para su posterior descodificación.
    
TNEF_ENCODE 
  
> El objeto TNEF en la secuencia indicada se abre para permiso de lectura y escritura. El proveedor de transporte debe establecer esta marca si desea que la función inicialice el objeto para la codificación subsiguiente.
    
TNEF_PURE 
  
> Codifica todas las propiedades en los bloques de encapsulación MAPI. Por lo tanto, un archivo TNEF "puro" constará de, como máximo, attMAPIProps, attAttachment, attRenddata y attRecipTable. Este modo es ideal para su uso cuando no se requiere compatibilidad con versiones anteriores.
    
_lpMessage_
  
> a Puntero a un objeto de mensaje como destino para un mensaje descodificado con datos adjuntos o un origen para un mensaje codificado con datos adjuntos. Las propiedades de un mensaje codificado podrían sobrescribir cualquier propiedad de un mensaje de destino.
    
_wKey_
  
> a Clave de búsqueda que el objeto TNEF utiliza para hacer coincidir los datos adjuntos con las etiquetas de texto insertadas en el texto del mensaje. Este valor debe ser relativamente único en todos los mensajes.
    
_lppTNEF_
  
> contempla Puntero al nuevo objeto TNEF.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Posteriormente, un objeto TNEF creado por la función **OpenTnefStream** llama al método OLE **IUnknown:: AddRef** para agregar referencias para el objeto support, el objeto Stream y el objeto Message. El proveedor de transporte puede liberar las referencias de los tres objetos con una sola llamada al método OLE **IUnknown:: Release** en el objeto TNEF. 
  
**OpenTnefStream** asigna e inicializa una interfaz **ITNEF** de objeto TNEF para que el proveedor la utilice al codificar una interfaz de mensaje de MAPI **IMessage** en un mensaje de transmisión TNEF. Como alternativa, la función puede configurar el objeto para que lo use el proveedor en las llamadas posteriores a [ITnef:: ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI. Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown:: Release** heredado en el objeto. 
  
Esta función es el punto de entrada original para el acceso TNEF y ha sido reemplazado por [OpenTnefStreamEx](opentnefstreamex.md) pero todavía se usa para la compatibilidad con los usuarios que ya usan TNEF. 
  
## <a name="see-also"></a>Vea también

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

