---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348779"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene la carpeta que se estableció como destino para los mensajes entrantes de una clase de mensaje especificada o como la carpeta de recepción predeterminada para el almacén de mensajes.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> a Un puntero a una clase de mensaje que está asociado a una carpeta de recepción. Si el parámetro _lpszMessageClass_ está establecido en null o una cadena vacía, **GetReceiveFolder** devuelve la carpeta de recepción predeterminada para el almacén de mensajes. 
    
 _ulFlags_
  
> a Máscara de bits de marcadores que controla el tipo de las cadenas que se han pasado y se han devuelto. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> La cadena de clase de mensaje está en formato Unicode. Si no se establece la marca MAPI_UNICODE, la cadena de clase de mensaje está en formato ANSI.
    
 _lpcbEntryID_
  
> contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> contempla Un puntero a un puntero al identificador de entrada de la carpeta de recepción solicitada.
    
 _lppszExplicitClass_
  
> contempla Un puntero a un puntero a la clase de mensaje que establece explícitamente como su carpeta de recepción la carpeta a la que apunta _lppEntryID_. Esta clase de mensaje debe ser la misma que la clase en el parámetro _lpszMessageClass_ o una clase base de dicha clase. Si se pasa NULL, indica que la carpeta a la que apunta _lppEntryID_ es la carpeta de recepción predeterminada para el almacén de mensajes. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta de recepción se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: GetReceiveFolder** obtiene el identificador de entrada de una carpeta de recepción, una carpeta designada para recibir los mensajes entrantes de una clase de mensaje determinada. Los autores de llamadas pueden especificar una clase de mensaje o NULL en el parámetro _lpszMessageClass_ . Si _lpszMessageClass_ es null, **GetReceiveFolder** devuelve los siguientes valores: 
  
- En _lppszExplicitClass_, el nombre de la primera clase base de la clase de mensaje a la que apunta _lpszMessageClass_ que hace que se establezca explícitamente una carpeta de recepción. 
    
- En _lppEntryID_, el identificador de entrada de la carpeta de recepción para la clase base apuntado por el parámetro _lppszExplicitClass_ . 
    
Por ejemplo, supongamos que la carpeta de recepción de la clase de mensaje **IPM. Note** se ha establecido en el identificador de entrada de la bandeja de entrada y se llama a **GetReceiveFolder** con el contenido de _lpszMessageClass_ establecido en **IPM. Note. Phone**. Si se trata de **IPM. Note. Phone** no tiene un conjunto de carpetas de recepción explícito, **GetReceiveFolder** devuelve el identificador de entrada de la bandeja de entrada en _lppEntryID_ e **IPM. Nota** en _lppszExplicitClass_.
  
Si el cliente llama a **GetReceiveFolder** para una clase de mensaje y no ha establecido una carpeta de recepción para la clase de mensaje, _lppszExplicitClass_ es una cadena de longitud cero, una cadena en formato Unicode o una cadena en formato ANSI, en función de si el el cliente estableció la marca MAPI_UNICODE en el parámetro _ulFlags_ . 
  
Siempre existe una carpeta de recepción predeterminada, obtenida pasando un valor NULL en el parámetro _lpszMessageClass_ , para cada almacén de mensajes. 
  
Un cliente debe llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando se realiza con el identificador de entrada devuelto en _lppEntryID_ para liberar la memoria que contiene el identificador de entrada. También debe llamar a **MAPIFreeBuffer** cuando se ha realizado con la cadena de clase de mensaje devuelta en _lppszExplicitClass_ para liberar la memoria que contiene esa cadena. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetInbox  <br/> |MFCMAPI usa el método **IMsgStore:: GetReceiveFolder** para localizar la carpeta Bandeja de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

