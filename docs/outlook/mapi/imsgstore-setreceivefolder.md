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
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434091"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece una carpeta como destino para los mensajes entrantes de una clase de mensaje determinada.
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> [in] Puntero a la clase de mensaje que se va a asociar a la nueva carpeta de recepción. Si el  _parámetro lpszMessageClass_ se establece en NULL o una cadena vacía, **SetReceiveFolder** establece la carpeta de recepción predeterminada para el almacén de mensajes. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de texto de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> La cadena de clase de mensaje está en formato Unicode. Si la MAPI_UNICODE no está establecida, la cadena de clase de mensaje tiene el formato ANSI.
    
 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada de la carpeta para establecer como carpeta de recepción. Si el  _parámetro lpEntryID_ se establece en NULL, **SetReceiveFolder** reemplaza la carpeta de recepción actual por el valor predeterminado del almacén de mensajes. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se estableció correctamente una carpeta de recepción.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::SetReceiveFolder** establece o cambia la carpeta de recepción de una clase de mensaje determinada. Con **SetReceiveFolder,** un cliente puede, mediante llamadas sucesivas, especificar una carpeta de recepción diferente para cada clase de mensaje definida o especificar que los mensajes entrantes para varias clases de mensaje vayan a la misma carpeta. Por ejemplo, un cliente puede hacer que su propia clase de mensajes llegue a su propia carpeta. Una aplicación de fax puede designar una carpeta en la que el proveedor de almacenamiento coloca faxes entrantes y otra carpeta en la que el proveedor coloca faxes salientes.
  
Si se produce un error durante la llamada a **SetReceiveFolder,** la configuración de la carpeta de recepción permanece sin cambios. 
  
Si **SetReceiveFolder** cambia la configuración de la carpeta de recepción con  _lpEntryID_ establecido en NULL, lo que indica que se debe establecer la carpeta de recepción predeterminada, **SetReceiveFolder** devuelve S_OK incluso si no había ninguna configuración existente para la clase de mensaje indicada. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI usa el **método IMsgStore::SetReceiveFolder** para establecer una carpeta como carpeta de recepción para una clase de mensaje determinada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

