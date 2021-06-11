---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408428"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera una secuencia que se usará para guardar el mensaje actual.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Parameters

 _pulFlags_
  
> [salida] Puntero a una máscara de bits de marcas que controla cómo se debe guardar el texto del mensaje. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> El texto del mensaje se guarda en formato Unicode. Si no MAPI_UNICODE marca, el texto se guarda en formato ANSI.
    
 _pulFormat_
  
> [salida] Puntero a una máscara de bits de marcas que controla el formato del texto guardado. Se pueden establecer las siguientes marcas:
    
SAVE_FORMAT_RICHTEXT 
  
> El texto del mensaje se guardará como texto con formato en el formato de texto enriquecido (RTF). 
    
SAVE_FORMAT_TEXT 
  
> El texto del mensaje se guardará como texto sin formato. 
    
 _ppstm_
  
> [salida] Puntero a un puntero a la secuencia que contendrá el mensaje guardado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La secuencia se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos Form llaman al método **IMAPIViewContext::GetSaveStream** para recuperar una secuencia de un objeto que implementa la interfaz **IStream** para admitir el control del verbo Guardar como en el visor de formularios. El método [IMAPIForm::D oVerb,](imapiform-doverb.md) que se implementa en el servidor de formularios y al que llama el visor de formularios para invocar un verbo, no debe devolverse hasta que el mensaje se convierta completamente en el formato de texto adecuado y se coloque en la secuencia adecuada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No escriba en la secuencia a la que apunta  _ppstm antes_ de llamar a **GetSaveStream**. Cuando **getSaveStream** devuelve, no restablezca la posición del puntero de búsqueda. Este puntero debe permanecer al final del texto del mensaje guardado. 
  
## <a name="see-also"></a>Vea también



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

