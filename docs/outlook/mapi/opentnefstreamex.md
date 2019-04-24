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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348576"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto de formato de encapsulación neutro para el transporte (TNEF) que se puede usar para codificar o descodificar un objeto de mensaje en una secuencia de datos TNEF para su uso mediante transportes o puertas de enlace y almacenes de mensajes. Es el punto de entrada para el acceso TNEF. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF. h  <br/> |
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
  
> a Pasa un objeto de soporte o pasa NULL. Si es NULL, el parámetro _lpAddressBook_ no debe ser null. 
    
_lpStream_
  
> a Puntero a un objeto de secuencia de almacenamiento, como una interfaz OLE **IStream** , que proporciona un origen o un destino para un mensaje de transmisión TNEF. 
    
_lpszStreamName_
  
> a Puntero al nombre de la secuencia de datos que usa el objeto TNEF. Si el autor de la llamada ha establecido el indicador TNEF_ENCODE ( _ulFlags_ ) en su llamada a **OpenTnefStream**, el parámetro _lpszName_ debe especificar un puntero que no sea nulo a una cadena que no sea NULL y que consista en cualquier carácter que se considere válido para el nombre de un archivo. MAPI no permite nombres de cadena que incluyan los caracteres "[", "]" o ":", incluso si el sistema de archivos permite su uso. El tamaño de la cadena que se pasa para el parámetro _lpszName_ no debe superar el valor de MAX_PATH, es decir, la longitud máxima de una cadena que contiene un nombre de ruta de acceso. 
    
_ulFlags_
  
> a Máscara de las marcas usadas para indicar el modo de la función. Se pueden establecer los siguientes indicadores:
    
TNEF_BEST_DATA 
  
> Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en las encapsulaciones. Tenga en cuenta que esto hará que se duplique la información del flujo TNEF. TNEF_BEST_DATA es el valor predeterminado si no se especifican otros modos. 
    
TNEF_COMPATIBILITY 
  
> Proporciona compatibilidad con versiones anteriores con aplicaciones cliente más antiguas. Las secuencias TNEF codificadas con este indicador asignarán todas las propiedades posibles al atributo de bajo nivel correspondiente. Este modo también hace que el valor predeterminado de algunas propiedades que los clientes de nivel inferior requieran. 
    
  > [!CAUTION]
  > Esta marca está obsoleta y no debe usarse. 
  
TNEF_DECODE 
  
> El objeto TNEF en la secuencia indicada se abre con acceso de solo lectura. El proveedor de transporte debe establecer esta marca si la función es inicializar el objeto para la descodificación subsiguiente.
    
TNEF_ENCODE 
  
> El objeto TNEF en la secuencia indicada se abre para permiso de lectura y escritura. El proveedor de transporte debe establecer esta marca si la función es inicializar el objeto para la codificación subsiguiente.
    
TNEF_PURE 
  
> Codifica todas las propiedades en los bloques de encapsulación MAPI. Por lo tanto, un archivo TNEF "puro" constará de, como máximo, los atributos attMAPIProps, attAttachment, attRenddata y attRecipTable. Este modo es ideal para su uso cuando no se requiere compatibilidad con versiones anteriores.
    
_lpMessage_
  
> a Puntero a un objeto de mensaje como destino para un mensaje descodificado con datos adjuntos o un origen para un mensaje codificado con datos adjuntos. Las propiedades de un mensaje codificado pueden sobrescribir cualquier propiedad de un mensaje de destino.
    
_wKeyVal_
  
> a Clave de búsqueda que el objeto TNEF utiliza para hacer coincidir los datos adjuntos con las etiquetas de texto insertadas en el texto del mensaje. Este valor debe ser relativamente único en todos los mensajes. 
    
_lpAddressBook_
  
> a Puntero a un objeto de la libreta de direcciones usado para obtener información de dirección para los identificadores de entrada. 
    
_lppTNEF_
  
> contempla Puntero al nuevo objeto TNEF.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La función **OpenTnefStreamEx** es el reemplazo recomendado para [OpenTnefStream](opentnefstream.md), el punto de entrada original de acceso TNEF. 
  
Posteriormente, un objeto TNEF creado por la función **OpenTnefStreamEx** llama al método OLE **IUnknown:: AddRef** para agregar referencias para el objeto support, el objeto Stream y el objeto Message. El proveedor de transporte puede liberar las referencias de los tres objetos con una sola llamada al método OLE **IUnknown:: Release** en el objeto TNEF. 
  
**OpenTnefStreamEx** asigna e inicializa un objeto TNEF para que lo use el proveedor al codificar un mensaje MAPI en un mensaje de transmisión TNEF. Como alternativa, esta función puede configurar el objeto que el proveedor debe usar en las llamadas posteriores a [ITnef:: ExtractProps](itnef-extractprops.md) para descodificar un mensaje de transmisión TNEF en un mensaje MAPI. Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown:: Release** heredado en el objeto. 
  
El valor base para el parámetro _wKeyVal_ no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**. En su lugar, use números aleatorios basados en la hora del sistema desde el generador de números aleatorios de la biblioteca en tiempo de ejecución.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Archivo. cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI usa el método **OpenTnefStreamEx** para abrir una secuencia en el archivo TNEF para que se puedan extraer propiedades.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

