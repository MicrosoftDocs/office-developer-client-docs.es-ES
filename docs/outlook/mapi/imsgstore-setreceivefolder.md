---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4e2d4f76fe436fd18b439bbbb558b1169094b438
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589465"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Establece una carpeta como destino de los mensajes entrantes de una clase de mensaje en particular.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpszMessageClass_
  
> [entrada] Un puntero a la clase de mensaje es que se asociará con la nueva carpeta de recepción. Si el parámetro _lpszMessageClass_ se establece en NULL o una cadena vacía, **SetReceiveFolder** conjuntos de carpeta para el almacén de mensajes de recepción la predeterminada. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo del texto en las cadenas que se pasan en. Se puede establecer la marca siguiente:
    
MAPI_UNICODE 
  
> La cadena de la clase de mensaje está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la cadena de la clase de mensaje está en formato ANSI.
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada de la carpeta que se va a establecer como la carpeta de recepción. Si el parámetro _lpEntryID_ se establece en NULL, **SetReceiveFolder** reemplaza la recepción de la actual carpeta con predeterminado del almacén de mensajes. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Una carpeta de recepción se ha establecido correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::SetReceiveFolder** establece o cambia la carpeta de recepción para una clase de mensaje en particular. Con **SetReceiveFolder**, un cliente puede, mediante llamadas sucesivas, especificar una diferentes recibir carpeta para cada clase de mensaje definido o especificar que los mensajes entrantes para todas las clases de mensaje varios van a la misma carpeta. Por ejemplo, un cliente puede tener su propia clase de mensajes entran en su propia carpeta. Una aplicación de fax puede designar una carpeta en la que el proveedor de almacenamiento coloca los faxes entrantes y otra carpeta en la que el proveedor coloca los faxes salientes.
  
Si se produce un error durante la llamada a **SetReceiveFolder**, la configuración de la carpeta de recepción permanece inalterada. 
  
Si cambia de **SetReceiveFolder** la configuración de la carpeta de recepción con _lpEntryID_ establecido en NULL, que indica que se debe establecer la carpeta de recepción predeterminada, **SetReceiveFolder** devuelve S_OK incluso si se ha producido ningún valor existente para el indicado clase de mensaje. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI usa el método **IMsgStore::SetReceiveFolder** para establecer una carpeta como la carpeta de recepción para una clase de mensaje en particular.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

