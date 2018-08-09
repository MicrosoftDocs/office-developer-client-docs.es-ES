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
ms.openlocfilehash: 52fd844954f41d5d09b5e78f7c23ff6f7469bb43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818458"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Hace referencia a**: Outlook 
  
Crea un objeto de formato de encapsulación neutro para el transporte (TNEF) que se puede usar para codificar o descodificar un objeto de mensaje en una secuencia de datos TNEF para su uso por los transportes o puertas de enlace y los almacenes de mensajes. Éste es el punto de entrada para el acceso de TNEF. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Parámetros

_lpvSupport_
  
> [entrada] Pasa un objeto de soporte técnico o pasa en NULL. Si es nulo, el parámetro _lpAddressBook_ debe ser distinto de null. 
    
_lpStream_
  
> [entrada] Puntero a un objeto stream de almacenamiento, como una interfaz **IStream** OLE, que proporciona un origen o destino para un mensaje de secuencia TNEF. 
    
_lpszStreamName_
  
> [entrada] Puntero en el nombre de la secuencia de datos que utiliza el objeto TNEF. Si el autor de la llamada ha establecido el indicador TNEF_ENCODE (parámetro _ulFlags_ ) en su llamada a **OpenTnefStream**, el parámetro _lpszName_ debe especificar un puntero no nulo a una cadena no nula formada por los caracteres que se considere válidos para asignar nombres a un archivo. MAPI no admite nombres de cadena, incluidos los caracteres "[", "]", o ":", incluso si el sistema de archivos permite su uso. El tamaño de la cadena que se pasa para el parámetro _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso. 
    
_ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para indicar el modo de la función. Se pueden establecer los siguientes indicadores:
    
TNEF_BEST_DATA 
  
> Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en la encapsulaciones. Tenga en cuenta que esto hará que la duplicación de información en la secuencia TNEF. TNEF_BEST_DATA es el valor predeterminado si no se especifiquen ningún otros modos. 
    
TNEF_COMPATIBILITY 
  
> Proporciona compatibilidad con versiones anteriores con aplicaciones de cliente anteriores. Secuencias TNEF codificadas con esta marca va a asignar todas las propiedades posibles en su atributo de nivel inferior correspondiente. Este modo también hace que el valor predeterminado de algunas propiedades que necesitan los clientes de nivel inferior. 
    
  > [!CAUTION]
  > Esta marca está obsoleta y no debe usarse. 
  
TNEF_DECODE 
  
> Se abre el objeto TNEF en la secuencia indicada con acceso de solo lectura. El proveedor de transporte debe establecer este indicador si la función es inicializar el objeto de descodificación subsiguientes.
    
TNEF_ENCODE 
  
> Se abre el objeto TNEF en la secuencia indicada para el permiso de lectura y escritura. El proveedor de transporte debe establecer este indicador si la función es inicializar el objeto de codificación subsiguientes.
    
TNEF_PURE 
  
> Codifica todas las propiedades en los bloques de encapsulación de MAPI. Por lo tanto, un archivo TNEF "puro" consistirá, como máximo, los atributos attMAPIProps, attAttachment, attRenddata y attRecipTable. Este modo es ideal para su uso cuando no hay compatibilidad con versiones anteriores se requiere.
    
_lpMessage_
  
> [entrada] Puntero a un objeto de mensaje como un destino para un mensaje descodificado con datos adjuntos o un origen de un mensaje codificado con datos adjuntos. Las propiedades de un mensaje de destino se pueden sobrescribir con las propiedades de un mensaje codificado.
    
_wKeyVal_
  
> [entrada] Una clave de búsqueda que utiliza el objeto TNEF para que coincida con los datos adjuntos a las etiquetas de texto insertados en el texto del mensaje. Este valor debe ser relativamente único a través de los mensajes. 
    
_lpAddressBook_
  
> [entrada] Puntero a un objeto de la libreta de direcciones utilizado para obtener información de los identificadores de entrada de direcciones. 
    
_lppTNEF_
  
> [out] Puntero al nuevo objeto TNEF.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La función **OpenTnefStreamEx** es la sustitución recomendada para [OpenTnefStream](opentnefstream.md), el punto de entrada original para el acceso de TNEF. 
  
Un objeto TNEF creado por la función **OpenTnefStreamEx** más adelante, llama al método OLE **IUnknown:: AddRef** para agregar referencias para el objeto de soporte, el objeto stream y el objeto de mensaje. El proveedor de transporte puede liberar las referencias para todos los tres objetos con una sola llamada al método OLE **IUnknown:: Release** en el objeto TNEF. 
  
**OpenTnefStreamEx** asigna e inicializa un objeto TNEF para el proveedor de uso en la codificación de un mensaje MAPI en un mensaje de secuencia TNEF. Como alternativa, esta función puede configurar el objeto para el proveedor de uso de las llamadas subsiguientes a [ITnef::ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI. Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown:: Release** heredado en el objeto. 
  
El valor de base para el parámetro _wKeyVal_ no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**. En su lugar, utilice números aleatorios según la hora del sistema desde el generador de números aleatorios de la biblioteca de tiempo de ejecución.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI usa el método **OpenTnefStreamEx** para abrir una secuencia en el archivo TNEF, por lo que se pueden extraer las propiedades.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

