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
  
> [in] Puntero al mensaje al que está asociada la secuencia. No es necesario que este mensaje sea el mismo que se pasa en la llamada a la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx.](opentnefstreamex.md) 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre la interfaz de secuencia. Se pueden establecer las siguientes marcas:
    
MAPI_CREATE 
  
> Si una propiedad no existe en el mensaje actual, debe crearse. Si la propiedad existe, los datos actuales de la propiedad deben reemplazarse por los datos de la secuencia Transport-Neutral formato de encapsulación (TNEF). Cuando una implementación establece la MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. La interfaz predeterminada es de solo lectura. MAPI_MODIFY debe establecerse siempre que MAPI_CREATE se establezca.
    
 _lppStream_
  
> [salida] Puntero a un puntero a un objeto de secuencia que contiene el texto de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) del mensaje encapsulado pasado y que admite la [interfaz IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::OpenTaggedBody** para abrir una interfaz de secuencia en el texto de un mensaje encapsulado (es decir, en un objeto TNEF). 
  
Como parte de su procesamiento, **OpenTaggedBody** inserta o analiza etiquetas de datos adjuntos que indican la posición de los datos adjuntos u objetos OLE en el texto del mensaje. Las etiquetas de datos adjuntos tienen el siguiente formato: 
  
 **[[** _nombre de datos adjuntos_ **:** _n en_ **nombre** _del contenedor de datos adjuntos_ **]]**
  
 _el nombre de los_ datos adjuntos describe el objeto attachment;  _n_ es un número que identifica los datos adjuntos que forman parte de una secuencia, incrementándose desde el valor pasado en el parámetro  _lpKey_ de la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx;](opentnefstreamex.md) y  _el nombre del contenedor de_ datos adjuntos describe el componente físico donde reside el objeto de datos adjuntos. 
  
 **OpenTaggedBody** lee el texto del mensaje e inserta una etiqueta de datos adjuntos siempre que un objeto de datos adjuntos apareciera originalmente en el texto. No se cambia el texto del mensaje original. 
  
Cuando se pasa un mensaje con etiquetas a una secuencia, las etiquetas se quitan y los objetos adjuntos se reubican en la posición de las etiquetas en la secuencia.
  
## <a name="see-also"></a>Vea también



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónica PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

