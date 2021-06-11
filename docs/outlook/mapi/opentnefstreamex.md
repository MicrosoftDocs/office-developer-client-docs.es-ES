---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406244"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto Transport-Neutral Encapsulation Format (TNEF) que se puede usar para codificar o descodificar un objeto de mensaje en un flujo de datos TNEF para usarlo en transportes o puertas de enlace y almacenes de mensajes. Este es el punto de entrada para el acceso TNEF. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Tnef.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de transporte  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Parameters

_lpvSupport_
  
> [in] Pasa un objeto de soporte técnico o pasa null. Si es NULL,  _el parámetro lpAddressBook_ debe ser distinto de null. 
    
_lpStream_
  
> [in] Puntero a un objeto de secuencia de almacenamiento, como una interfaz OLE **IStream,** que proporciona un origen o destino para un mensaje de secuencia TNEF. 
    
_lpszStreamName_
  
> [in] Puntero al nombre de la secuencia de datos que usa el objeto TNEF. Si el autor de la llamada ha establecido la marca de TNEF_ENCODE ( _parámetro ulFlags)_ en su llamada a **OpenTnefStream**, el parámetro  _lpszName_ debe especificar un puntero que no sea nulo a una cadena que no sea nula y que consista en cualquier carácter que se considere válido para asignar un nombre a un archivo. MAPI no permite nombres de cadena, incluidos los caracteres "[", "]" o ., incluso si el sistema de archivos permite su uso. El tamaño de la cadena pasada para el parámetro  _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso. 
    
_ulFlags_
  
> [in] Máscara de bits de las marcas usadas para indicar el modo de la función. Se pueden establecer las siguientes marcas:
    
TNEF_BEST_DATA 
  
> Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en las encapsulaciones. Tenga en cuenta que esto provocará la duplicación de información en la secuencia TNEF. TNEF_BEST_DATA es el valor predeterminado si no se especifica ningún otro modo. 
    
TNEF_COMPATIBILITY 
  
> Proporciona compatibilidad con versiones anteriores con aplicaciones cliente anteriores. Las secuencias TNEF codificadas con esta marca asignarán todas las propiedades posibles a su atributo de nivel inferior correspondiente. Este modo también provoca la configuración predeterminada de algunas propiedades que requieren los clientes de nivel inferior. 
    
  > [!CAUTION]
  > Esta marca está obsoleta y no debe usarse. 
  
TNEF_DECODE 
  
> El objeto TNEF de la secuencia indicada se abre con acceso de solo lectura. El proveedor de transporte debe establecer esta marca si la función va a inicializar el objeto para la posterior decodificación.
    
TNEF_ENCODE 
  
> El objeto TNEF de la secuencia indicada se abre para el permiso de lectura y escritura. El proveedor de transporte debe establecer esta marca si la función es inicializar el objeto para la codificación posterior.
    
TNEF_PURE 
  
> Codifica todas las propiedades en los bloques de encapsulación MAPI. Por lo tanto, un archivo TNEF "puro" constará, como máximo, de los atributos attMAPIProps, attAttachment, attRenddata y attRecipTable. Este modo es ideal para su uso cuando no se requiere compatibilidad con versiones anteriores.
    
_lpMessage_
  
> [in] Puntero a un objeto de mensaje como destino de un mensaje descodificado con datos adjuntos o un origen para un mensaje codificado con datos adjuntos. Las propiedades de un mensaje codificado pueden sobrescribir todas las propiedades de un mensaje de destino.
    
_wKeyVal_
  
> [in] Clave de búsqueda que el objeto TNEF usa para hacer coincidir datos adjuntos con las etiquetas de texto insertadas en el texto del mensaje. Este valor debe ser relativamente único en todos los mensajes. 
    
_lpAddressBook_
  
> [in] Puntero a un objeto de libreta de direcciones usado para obtener información de direccionamiento para los identificadores de entrada. 
    
_lppTNEF_
  
> [salida] Puntero al nuevo objeto TNEF.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La **función OpenTnefStreamEx** es el reemplazo recomendado para [OpenTnefStream](opentnefstream.md), el punto de entrada original para el acceso TNEF. 
  
Más adelante, un objeto TNEF creado por la función **OpenTnefStreamEx** llama al método OLE **IUnknown::AddRef** para agregar referencias al objeto de compatibilidad, al objeto stream y al objeto message. El proveedor de transporte puede liberar las referencias de los tres objetos con una sola llamada al método OLE **IUnknown::Release** en el objeto TNEF. 
  
**OpenTnefStreamEx** asigna e inicializa un objeto TNEF para que el proveedor lo use al codificar un mensaje MAPI en un mensaje de secuencia TNEF. Como alternativa, esta función puede configurar el objeto para que el proveedor lo use en llamadas posteriores a [ITnef::ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI. Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown::Release** heredado en el objeto. 
  
El valor base del  _parámetro wKeyVal_ no debe ser cero y no debe ser el mismo para cada llamada a **OpenTnefStreamEx**. En su lugar, use números aleatorios según la hora del sistema del generador de números aleatorios de la biblioteca en tiempo de ejecución.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI usa el **método OpenTnefStreamEx** para abrir una secuencia en el archivo TNEF para que se puedan extraer propiedades.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

