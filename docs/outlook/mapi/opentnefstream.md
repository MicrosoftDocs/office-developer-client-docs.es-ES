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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423961"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Llamado por un proveedor de transporte para iniciar una sesión de formato de encapsulamiento neutro de transporte (TNEF) MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Tnef.h  <br/> |
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

## <a name="parameters"></a>Parámetros

_lpvSupport_
  
> [entrada] Pasa un objeto de compatibilidad o pasa NULL. 
    
_lpStream_
  
> [entrada] Puntero a una interfaz OLE **IStream** de objeto de secuencia de almacenamiento que proporciona un origen o destino para un mensaje de secuencia TNEF. 
    
_lpszStreamName_
  
> [entrada] Puntero al nombre de la secuencia de datos que usa el objeto TNEF. Si el autor de la llamada ha establecido la marca TNEF_ENCODE ( _parámetro ulFlags)_ en su llamada a **OpenTnefStream**, el parámetro  _lpszName_ debe especificar un puntero que no sea nulo a una cadena que no sea nula y que conste de cualquier carácter que se considere válido para nombrar un archivo. MAPI no permite nombres de cadena, incluidos los caracteres "[", "]" o ":", incluso si el sistema de archivos permite su uso. El tamaño de la cadena pasada para  _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso. 
    
_ulFlags_
  
> [entrada] Máscara de bits de marcas usadas para indicar el modo de la función. Se pueden establecer las siguientes marcas:
    
TNEF_BEST_DATA 
  
> Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en las encapsulaciones. Tenga en cuenta que esto provocará la duplicación de información en la secuencia TNEF. TNEF_BEST_DATA es el valor predeterminado si no se especifican otros modos. 
    
TNEF_COMPATIBILITY 
  
> Proporciona compatibilidad con versiones anteriores con las aplicaciones cliente anteriores. Las secuencias TNEF codificadas con esta marca asignarán todas las propiedades posibles a su atributo de nivel inferior correspondiente. Este modo también provoca la configuración predeterminada de algunas propiedades que requieren los clientes de nivel inferior. 
    
  > [!CAUTION]
  > Esta marca está obsoleta y no debe usarse. 
  
TNEF_DECODE 
  
> El objeto TNEF de la secuencia indicada se abre con acceso de solo lectura. El proveedor de transporte debe establecer esta marca si desea que la función inicialice el objeto para la posterior decodificación.
    
TNEF_ENCODE 
  
> El objeto TNEF de la secuencia indicada se abre para el permiso de lectura y escritura. El proveedor de transporte debe establecer esta marca si desea que la función inicialice el objeto para la codificación posterior.
    
TNEF_PURE 
  
> Codifica todas las propiedades en los bloques de encapsulación MAPI. Por lo tanto, un archivo TNEF "puro" constará, como máximo, de attMAPIProps, attAttachment, attRenddata y attRecipTable. Este modo es ideal para su uso cuando no se requiere compatibilidad con versiones anteriores.
    
_lpMessage_
  
> [entrada] Puntero a un objeto de mensaje como destino de un mensaje descodificado con datos adjuntos o un origen de un mensaje codificado con datos adjuntos. Las propiedades de un mensaje codificado pueden sobrescribir las propiedades de un mensaje de destino.
    
_wKey_
  
> [entrada] Clave de búsqueda que el objeto TNEF usa para hacer coincidir los datos adjuntos con las etiquetas de texto insertadas en el texto del mensaje. Este valor debe ser relativamente único en todos los mensajes.
    
_lppTNEF_
  
> [salida] Puntero al nuevo objeto TNEF.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Un objeto TNEF creado por la función **OpenTnefStream** más adelante llama al método OLE **IUnknown::AddRef** para agregar referencias para el objeto de compatibilidad, el objeto de secuencia y el objeto de mensaje. El proveedor de transporte puede liberar las referencias de los tres objetos con una sola llamada al método OLE **IUnknown::Release** en el objeto TNEF. 
  
**OpenTnefStream** asigna e inicializa una interfaz **ITnef** de objeto TNEF para que el proveedor la use en la codificación de una interfaz **IMessage** de mensaje MAPI en un mensaje de secuencia TNEF. Como alternativa, la función puede configurar el objeto para que el proveedor lo use en llamadas posteriores a [ITnef::ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI. Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **heredado IUnknown::Release** en el objeto. 
  
Esta función es el punto de entrada original para el acceso TNEF y se ha reemplazado por [OpenTnefStreamEx,](opentnefstreamex.md) pero se sigue usando para la compatibilidad con aquellos que ya usan TNEF. 
  
## <a name="see-also"></a>Consulte también

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

