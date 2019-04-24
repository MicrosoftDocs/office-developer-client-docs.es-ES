---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348737"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una interfaz de secuencia en el texto de un mensaje encapsulado.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> a Un puntero al mensaje con el que está asociada la secuencia. No es necesario que este mensaje sea el mismo mensaje que se pasa en la llamada a la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre la interfaz de la secuencia. Se pueden establecer los siguientes indicadores:
    
MAPI_CREATE 
  
> Si una propiedad no existe en el mensaje actual, se debe crear. Si la propiedad existe, los datos actuales de la propiedad deben reemplazarse por los datos de la secuencia formato de encapsulación neutro para el transporte (TNEF). Cuando una implementación establece la marca MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. La interfaz predeterminada es de sólo lectura. MAPI_MODIFY debe establecerse siempre que se establezca MAPI_CREATE.
    
 _lppStream_
  
> contempla Un puntero a un puntero a un objeto Stream que contiene el texto de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) del mensaje encapsulado pasado y que admite la interfaz [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: OpenTaggedBody** para abrir una interfaz de secuencia en el texto de un mensaje encapsulado (es decir, en un objeto TNEF). 
  
Como parte de su procesamiento, **OpenTaggedBody** inserta o analiza etiquetas de datos adjuntos que indican la posición de los datos adjuntos u objetos OLE en el texto del mensaje. Las etiquetas de datos adjuntos tienen el siguiente formato: 
  
 **[[** _nombre del archivo adjunto_ **:** _n_ **en** _el nombre del contenedor de datos adjuntos_ **]]**
  
 _nombre de datos_ adjuntos describe el objeto Attachment;  _n_ es un número que identifica los datos adjuntos que forman parte de una secuencia, incrementando desde el valor pasado en el parámetro _lpKey_ de la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) ; y el _nombre del contenedor de datos_ adjuntos describe el componente físico en el que reside el objeto Attachment. 
  
 **OpenTaggedBody** lee el texto del mensaje e inserta una etiqueta de datos adjuntos donde un objeto Attachment aparecía originalmente en el texto. No se cambia el texto del mensaje original. 
  
Cuando un mensaje que tiene etiquetas se pasa a una secuencia, se quitan las etiquetas y los objetos de datos adjuntos se reubican en la posición de las etiquetas en la secuencia.
  
## <a name="see-also"></a>Vea también



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónica PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

