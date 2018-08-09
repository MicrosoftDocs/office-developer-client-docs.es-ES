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
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817633"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Hace referencia a**: Outlook 
  
Recupera una secuencia que se utilizará para guardar el mensaje actual.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Parámetros

 _pulFlags_
  
> [out] Puntero a una máscara de bits de indicadores que controla cómo se debe guardar el texto del mensaje. Se puede establecer la marca siguiente:
    
MAPI_UNICODE. 
  
> El texto del mensaje se guarda en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el texto se guarda en formato ANSI.
    
 _pulFormat_
  
> [out] Puntero a una máscara de bits de indicadores que controla el formato del texto guardado. Se pueden establecer los siguientes indicadores:
    
SAVE_FORMAT_RICHTEXT 
  
> El texto del mensaje es que se guarde como texto con formato en el formato de texto enriquecido (RTF). 
    
SAVE_FORMAT_TEXT 
  
> El texto del mensaje es que se guarde como texto sin formato. 
    
 _ppstm_
  
> [out] Puntero a un puntero a la secuencia que va a contener el mensaje guardado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La secuencia se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIViewContext::GetSaveStream** para recuperar una secuencia de un objeto que implementa la interfaz **IStream** para admitir la administración del verbo Guardar como en el Visor de formulario. El método [IMAPIForm::DoVerb](imapiform-doverb.md) , que se implementa en el servidor de formulario y llamado por el Visor de formulario para invocar un verbo, no debe devolver hasta que el mensaje se convierte en el formato de texto adecuado y se coloca en la secuencia adecuada totalmente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

No se puede escribir en la secuencia indicada por _ppstm_ antes de llamar a **GetSaveStream**. Cuando se devuelve **GetSaveStream** , no restablezca la posición del puntero de búsqueda. Este puntero debe permanecer al final del texto del mensaje guardado. 
  
## <a name="see-also"></a>Vea también



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

