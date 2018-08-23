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
ms.openlocfilehash: e740e86fc25307457119aabf6e2aa0c42a9d69b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568227"
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

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje nuevo. Identificadores de interfaz válido incluyen IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer y IID_IMAPIFolder. Pasando NULL hace que el proveedor de almacenamiento de mensajes devolver la interfaz de mensaje estándar, [IMessage: IMAPIProp](imessageimapiprop.md). 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se crea el mensaje. Se pueden establecer los siguientes indicadores:
    
ITEMPROC_FORCE
  
> Indica al almacén de carpetas personales (PST) que el mensaje es apto para reglas de procesamiento antes de que el almacén notifica a cualquier cliente de escucha de la llegada del nuevo mensaje. Las reglas de procesamiento sólo se aplica a los nuevos mensajes que se crean en un servidor que no es un servidor de Exchange de Microsoft, debido a que Exchange Server procesa las reglas para los mensajes en el servidor. Por lo tanto, el proveedor o cliente que crea el mensaje debe pasar esta marca en combinación con el almacenamiento de un mensaje con [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) con NON_EMS_XP_SAVE, que indica que el servidor no es un servidor de Exchange. 
    
MAPI_ASSOCIATED 
  
> El mensaje que se va a crear se debe incluir en la tabla de contenido asociadas en lugar de la tabla de contenido estándar. Los mensajes asociados están ocultos de interacción del usuario.
    
MAPI_DEFERRED_ERRORS 
  
> Se permite que **CreateMessage** correctamente incluso si no se ha completado la operación de creación. Esto implica que el nuevo mensaje es posible que no sean inmediatamente disponible para el autor de la llamada. 
    
 _lppMessage_
  
> [out] Un puntero a un puntero al mensaje recién creado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se ha creado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::CreateMessage** crea un nuevo mensaje con contenido genérico o asociado y le asigna un identificador de entrada. El identificador de entrada consta de un elemento que representa el proveedor de almacén de mensajes y un elemento que representa el mensaje individual. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede elegir si va a establecer todas las propiedades del mensaje se requiere en **CreateMessage** o en el método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje. No es necesario que estas propiedades esté disponible hasta que se ha producido una operación de guardar correcta. 
  
Para obtener más información acerca de cómo trabajar con información asociada, vea [Las tablas de información de Folder-Associated](folder-associated-information-tables.md) y [Las tablas de contenido](contents-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Algunos proveedores de almacén de mensajes permiten el identificador de entrada del nuevo mensaje para que estén disponibles inmediatamente después de **CreateMessage** devuelve; otros proveedores de almacenes de mensaje retrasar su disponibilidad hasta que se guarda el mensaje. Debido a que no todos los proveedores de almacén de mensajes generan un identificador de entrada para un nuevo mensaje de hasta que se ha llamado (método **IMAPIProp::SaveChanges** ) del mensaje, es posible que no se puede obtener acceso al identificador de entrada cuando **CreateMessage** devuelve. Además, el nuevo mensaje es posible que no se incluyan en la tabla de contenido de la carpeta hasta que se produce la operación de guardar. 
  
Esperar el identificador de entrada asignado al mensaje nuevo para ser únicos no sólo en el almacén de mensajes actual, pero es más probable que a través de todos los almacenes de mensajes que están abiertos al mismo tiempo. Una excepción a esta regla se produce cuando aparecen varias entradas para un almacén de mensajes en el perfil. Esto hace que el almacén de mensajes que se va a abrir varias veces y los identificadores de entrada que se va a duplicar. 
  
Para crear un mensaje saliente, llamar al método **IMAPIFolder::CreateMessage** de la carpeta Bandeja de salida. 
  
Si elimina una carpeta que contiene un mensaje nuevo antes de que el mensaje se guarda, los resultados son no definidos.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolder::OnNewMessage  <br/> |MFCMAPI usa el método **IMAPIFolder::CreateMessage** para crear y guardar un mensaje nuevo.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

