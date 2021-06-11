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
  
Crea un mensaje nuevo.
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al nuevo mensaje. Los identificadores de interfaz válidos IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder. Si se pasa NULL, el proveedor del almacén de mensajes devuelve la interfaz de mensaje estándar, [IMessage : IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se crea el mensaje. Se pueden establecer las siguientes marcas:
    
ITEMPROC_FORCE
  
> Indica al almacén de carpetas personales (PST) que el mensaje es apto para el procesamiento de reglas antes de que el almacén notime a cualquier cliente de escucha la llegada del nuevo mensaje. El procesamiento de reglas solo se aplica a los mensajes nuevos que se crean en un servidor que no es un Microsoft Exchange Server, ya que Exchange Server procesa reglas para los mensajes en el servidor. Por lo tanto, el proveedor o cliente que crea el mensaje debe pasar esta marca en combinación con guardar un mensaje con [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) mediante NON_EMS_XP_SAVE, lo que indica que el servidor no es un Exchange Server. 
    
MAPI_ASSOCIATED 
  
> El mensaje que se va a crear debe incluirse en la tabla de contenido asociada en lugar de en la tabla de contenido estándar. Los mensajes asociados se ocultan de la interacción del usuario.
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage** puede realizarse correctamente incluso si la operación de creación no se ha completado por completo. Esto implica que es posible que el nuevo mensaje no esté disponible inmediatamente para el autor de la llamada. 
    
 _lppMessage_
  
> [salida] Puntero a un puntero al mensaje recién creado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::CreateMessage** crea un nuevo mensaje con contenido genérico o asociado y asigna un identificador de entrada. El identificador de entrada consta de una parte que representa el proveedor del almacén de mensajes y una parte que representa el mensaje individual. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede elegir si desea establecer todas las propiedades de mensaje necesarias en **CreateMessage** o en el método [IMAPIProp::SaveChanges del](imapiprop-savechanges.md) mensaje. No es necesario que estas propiedades estén disponibles hasta que se haya producido un guardado correcto. 
  
Para obtener más información acerca de cómo trabajar con información asociada, vea Tablas de [información](folder-associated-information-tables.md) asociadas a carpetas y [tablas de contenido.](contents-tables.md) 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Algunos proveedores de almacenes de mensajes permiten que el identificador de entrada del nuevo mensaje esté disponible inmediatamente después de que **CreateMessage** devuelva; otros proveedores de almacén de mensajes retrasan su disponibilidad hasta que se guarda el mensaje. Dado que no todos los proveedores de almacén de mensajes generan un identificador de entrada para un mensaje nuevo hasta que haya llamado al método **IMAPIProp::SaveChanges** del mensaje, es posible que no pueda tener acceso al identificador de entrada cuando **createMessage** devuelva. Además, es posible que el nuevo mensaje no se incluya en la tabla de contenido de la carpeta hasta que se produzca el guardado. 
  
Espere que el identificador de entrada asignado al nuevo mensaje sea único no solo en el almacén de mensajes actual, sino que lo más probable es que en todos los almacenes de mensajes que están abiertos al mismo tiempo. Una excepción a esta regla se produce cuando aparecen varias entradas para un almacén de mensajes en el perfil. Esto hace que el almacén de mensajes se abra varias veces y que se dupliquen los identificadores de entrada. 
  
Para crear un mensaje saliente, llame al método **IMAPIFolder::CreateMessage** de la carpeta De salida. 
  
Si elimina una carpeta que contiene un nuevo mensaje antes de guardar el mensaje, los resultados no están definidos.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI usa el **método IMAPIFolder::CreateMessage** para crear y guardar un mensaje nuevo.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

