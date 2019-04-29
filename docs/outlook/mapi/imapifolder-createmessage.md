---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412635"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un nuevo mensaje.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al nuevo mensaje. Los identificadores de interfaz válidos incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder. Si se pasa NULL, el proveedor de almacén de mensajes devolverá la interfaz de mensaje estándar, [IMessage: IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo se crea el mensaje. Se pueden establecer los siguientes indicadores:
    
ITEMPROC_FORCE
  
> Indica al almacén de carpetas personales (PST) que el mensaje es apto para el procesamiento de reglas antes de que el almacén notifique a los clientes de escuchas la llegada del nuevo mensaje. El procesamiento de reglas solo se aplica a los mensajes nuevos que se crean en un servidor que no es Microsoft Exchange Server, ya que Exchange Server procesa las reglas para los mensajes en el servidor. Por lo tanto, el proveedor o el cliente que crea el mensaje debe pasar esta marca en combinación con guardar un mensaje con [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md) con NON_EMS_XP_SAVE, que indica que el servidor no es un servidor de Exchange. 
    
MAPI_ASSOCIATED 
  
> El mensaje que se va a crear debe incluirse en la tabla de contenido asociada en lugar de la tabla de contenido estándar. Los mensajes asociados están ocultos para la interacción del usuario.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** puede tener éxito incluso si la operación de creación no se completó completamente. Esto implica que el nuevo mensaje puede que no esté disponible inmediatamente para el autor de la llamada. 
    
 _lppMessage_
  
> contempla Un puntero a un puntero al mensaje que se acaba de crear.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: CreateMessage** crea un nuevo mensaje con contenido genérico o asociado y asigna un identificador de entrada. El identificador de entrada consta de una parte que representa al proveedor de almacenamiento de mensajes y una parte que representa el mensaje individual. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede elegir si desea establecer todas las propiedades de mensaje necesarias en **CreateMessage** o en el método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje. No es necesario que estas propiedades estén disponibles hasta que se haya guardado correctamente. 
  
Para obtener más información sobre cómo trabajar con información asociada, vea tablas [de información asociada a carpetas](folder-associated-information-tables.md) y [tablas de contenido](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Algunos proveedores de almacenamiento de mensajes permiten que el identificador de entrada del nuevo mensaje esté disponible inmediatamente una vez devuelto **CreateMessage** ; otros proveedores de almacenamiento de mensajes retrasan su disponibilidad hasta que se guarda el mensaje. Como no todos los proveedores de almacenamiento de mensajes generan un identificador de entrada para un mensaje nuevo hasta que se llama al método **IMAPIProp:: SaveChanges** del mensaje, es posible que no pueda obtener acceso al identificador de entrada cuando **CreateMessage** devuelve. Además, es posible que el nuevo mensaje no se incluya en la tabla de contenido de la carpeta hasta que se guarde. 
  
Se espera que el identificador de entrada asignado al nuevo mensaje sea único y que sea único en el almacén de mensajes actual, pero lo más probable es que todos los almacenes de mensajes estén abiertos al mismo tiempo. Se produce una excepción a esta regla cuando en el perfil aparecen varias entradas para un almacén de mensajes. Esto hace que el almacén de mensajes se abra varias veces y que se dupliquen los identificadores de entrada. 
  
Para crear un mensaje saliente, llame al método **IMAPIFolder:: CreateMessage** de la carpeta Bandeja de salida. 
  
Si elimina una carpeta que contiene un mensaje nuevo antes de guardar el mensaje, los resultados quedan sin definir.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolder:: OnNewMessage  <br/> |MFCMAPI usa el método **IMAPIFolder:: CreateMessage** para crear y guardar un nuevo mensaje.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

