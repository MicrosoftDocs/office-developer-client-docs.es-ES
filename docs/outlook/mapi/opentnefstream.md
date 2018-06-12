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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818450"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Se aplica a**: Outlook 
  
Llamado por un proveedor de transporte para iniciar una sesión de formato de encapsulación neutro de transporte (TNEF) MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
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

## <a name="parameters"></a>Sintaxis

_lpvSupport_
  
> [entrada] Pasa un objeto de soporte técnico o pasa en NULL. 
    
_lpStream_
  
> [entrada] Puntero a una interfaz **IStream** OLE de almacenamiento secuencia objeto proporcionar un origen o destino para un mensaje de secuencia TNEF. 
    
_lpszStreamName_
  
> [entrada] Puntero en el nombre de la secuencia de datos que utiliza el objeto TNEF. Si el autor de la llamada ha establecido el indicador TNEF_ENCODE (parámetro _ulFlags_ ) en su llamada a **OpenTnefStream**, el parámetro _lpszName_ debe especificar un puntero no nulo a una cadena no nula formada por los caracteres que se considere válidos para asignar nombres a un archivo. MAPI no admite nombres de cadena, incluidos los caracteres "[", "]", o ":", incluso si el sistema de archivos permite su uso. El tamaño de la cadena que se pasa para _lpszName_ no debe superar el valor de MAX_PATH, la longitud máxima de una cadena que contiene un nombre de ruta de acceso. 
    
_ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para indicar el modo de la función. Se pueden establecer los siguientes indicadores:
    
TNEF_BEST_DATA 
  
> Todas las propiedades posibles se asignan a sus atributos de nivel inferior, pero cuando hay una posible pérdida de datos debido a la conversión a un atributo de nivel inferior, la propiedad también se codifica en la encapsulaciones. Tenga en cuenta que esto hará que la duplicación de información en la secuencia TNEF. TNEF_BEST_DATA es el valor predeterminado si no se especifiquen ningún otros modos. 
    
TNEF_COMPATIBILITY 
  
> Proporciona compatibilidad con versiones anteriores con el cliente de más antiguos a las aplicaciones. Secuencias TNEF codificadas con esta marca va a asignar todas las propiedades posibles en su atributo de nivel inferior correspondiente. Este modo también hace que el valor predeterminado de algunas propiedades que necesitan los clientes de nivel inferior. 
    
  > [!CAUTION]
  > Esta marca está obsoleta y no debe usarse. 
  
TNEF_DECODE 
  
> Se abre el objeto TNEF en la secuencia indicada con acceso de solo lectura. El proveedor de transporte debe establecer esta marca si desea que la función para inicializar el objeto de descodificación subsiguientes.
    
TNEF_ENCODE 
  
> Se abre el objeto TNEF en la secuencia indicada para el permiso de lectura y escritura. El proveedor de transporte debe establecer esta marca si desea que la función para inicializar el objeto de codificación subsiguientes.
    
TNEF_PURE 
  
> Codifica todas las propiedades en los bloques de encapsulación de MAPI. Por lo tanto, un archivo TNEF "puro" consistirá, en la mayoría, attMAPIProps, attAttachment, attRenddata y attRecipTable. Este modo es ideal para su uso cuando no hay compatibilidad con versiones anteriores se requiere.
    
_lpMessage_
  
> [entrada] Puntero a un objeto de mensaje como un destino para un mensaje descodificado con datos adjuntos o un origen de un mensaje codificado con datos adjuntos. Las propiedades de un mensaje codificado pueden sobrescribir las propiedades de un mensaje de destino.
    
_wKey_
  
> [entrada] Una clave de búsqueda que utiliza el objeto TNEF para que coincida con los datos adjuntos a las etiquetas de texto insertados en el texto del mensaje. Este valor debe ser relativamente único a través de los mensajes.
    
_lppTNEF_
  
> [out] Puntero al nuevo objeto TNEF.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Un objeto TNEF creado por la función **OpenTnefStream** más adelante, llama al método OLE **IUnknown:: AddRef** para agregar referencias para el objeto de soporte, el objeto stream y el objeto de mensaje. El proveedor de transporte puede liberar las referencias para todos los tres objetos con una sola llamada al método OLE **IUnknown:: Release** en el objeto TNEF. 
  
**OpenTnefStream** asigna e inicializa una interfaz de **ITnef** del objeto TNEF para el proveedor usar en **una interfaz de mensaje MAPI** de codificación en un mensaje de secuencia TNEF. Como alternativa, la función puede configurar el objeto para el proveedor de uso de las llamadas subsiguientes a [ITnef::ExtractProps](itnef-extractprops.md) para descodificar un mensaje de secuencia TNEF en un mensaje MAPI. Para liberar el objeto TNEF y cerrar la sesión, el proveedor de transporte debe llamar al método **IUnknown:: Release** heredado en el objeto. 
  
Esta función es el punto de entrada original para el acceso de TNEF y ha sido reemplazada por [OpenTnefStreamEx](opentnefstreamex.md) , pero aún se usa para la compatibilidad para aquellos ya está usando la codificación TNEF. 
  
## <a name="see-also"></a>Ver también

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

