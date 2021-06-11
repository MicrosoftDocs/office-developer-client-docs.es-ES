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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435351"
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
  
> [in] Puntero a una clase de mensaje asociada a una carpeta de recepción. Si el  _parámetro lpszMessageClass_ se establece en NULL o una cadena vacía, **GetReceiveFolder** devuelve la carpeta de recepción predeterminada para el almacén de mensajes. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de las cadenas pasadas y devueltas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> La cadena de clase de mensaje está en formato Unicode. Si la MAPI_UNICODE no está establecida, la cadena de clase de mensaje tiene el formato ANSI.
    
 _lpcbEntryID_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._ 
    
 _lppEntryID_
  
> [salida] Puntero a un puntero al identificador de entrada de la carpeta de recepción solicitada.
    
 _lppszExplicitClass_
  
> [salida] Puntero a un puntero a la clase de mensaje que establece explícitamente como carpeta de recepción la carpeta a la que  _apunta lppEntryID_. Esta clase de mensaje debe ser la misma que la clase del parámetro  _lpszMessageClass_ o una clase base de esa clase. Pasar NULL indica que la carpeta a la que  _apunta lppEntryID_ es la carpeta de recepción predeterminada para el almacén de mensajes. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta de recepción se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::GetReceiveFolder** obtiene el identificador de entrada de una carpeta de recepción, una carpeta designada para recibir mensajes entrantes de una clase de mensaje determinada. Los autores de llamadas pueden especificar una clase de mensaje o NULL en el _parámetro lpszMessageClass._ Si  _lpszMessageClass_ es NULL, **GetReceiveFolder** devuelve los siguientes valores: 
  
- En  _lppszExplicitClass_, el nombre de la primera clase base de la clase de mensaje apuntada por  _lpszMessageClass_ que establece explícitamente una carpeta de recepción. 
    
- En _lppEntryID_, el identificador de entrada de la carpeta de recepción de la clase base a la que apunta el _parámetro lppszExplicitClass._ 
    
Por ejemplo, supongamos que la carpeta de recepción de la clase de mensaje **IPM. La** nota se ha establecido en el identificador de entrada de la Bandeja de entrada y se llama a **GetReceiveFolder** con el contenido de _lpszMessageClass_ establecido en **IPM. Nota. Teléfono**. Si **es IPM. Nota. Teléfono** no tiene un conjunto explícito de carpetas de recepción, **GetReceiveFolder** devuelve el identificador de entrada de la Bandeja de entrada en _lppEntryID_ e **IPM. Nota** en _lppszExplicitClass_.
  
Si el cliente llama a **GetReceiveFolder** para una clase de mensaje y no ha establecido una carpeta de recepción para esa clase de mensaje, _lppszExplicitClass_ es una cadena de longitud cero, una cadena en formato Unicode o una cadena en formato ANSI en función de si el cliente establece la marca MAPI_UNICODE en el _parámetro ulFlags._ 
  
Una carpeta de recepción predeterminada, obtenida pasando NULL en el parámetro  _lpszMessageClass,_ siempre existe para cada almacén de mensajes. 
  
Un cliente debe llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando se realiza con el identificador de entrada devuelto en  _lppEntryID_ para liberar la memoria que contiene ese identificador de entrada. También debe llamar a **MAPIFreeBuffer** cuando termine con la cadena de clase de mensaje devuelta en  _lppszExplicitClass_ para liberar la memoria que contiene esa cadena. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI usa el **método IMsgStore::GetReceiveFolder** para buscar la carpeta Bandeja de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

