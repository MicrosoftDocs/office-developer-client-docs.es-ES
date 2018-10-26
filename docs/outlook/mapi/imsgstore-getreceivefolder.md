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
ms.openlocfilehash: a8cd211cc16b620ac47357271070e0b45b867bea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579945"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Obtiene la carpeta que se estableció como el destino para los mensajes entrantes de una clase de mensaje especificado o como el valor predeterminado de recepción carpeta para el almacén de mensajes.
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Parámetros

 _lpszMessageClass_
  
> [entrada] Un puntero a una clase de mensaje que está asociada con una carpeta de recepción. Si el parámetro _lpszMessageClass_ se establece en NULL o una cadena vacía, **GetReceiveFolder** devuelve el valor predeterminado recibir carpeta para el almacén de mensajes. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas en el pasado y devueltos. Se puede establecer la marca siguiente:
    
MAPI_UNICODE 
  
> La cadena de la clase de mensaje está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., la cadena de la clase de mensaje está en formato ANSI.
    
 _lpcbEntryID_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un puntero a un puntero al identificador de entrada para el solicitado recibir carpeta.
    
 _lppszExplicitClass_
  
> [out] Un puntero a un puntero a la clase de mensaje que se establezca explícitamente como su carpeta la carpeta indicada por _lppEntryID_de recepción. Esta clase de mensaje debe ser la misma que la clase en el parámetro _lpszMessageClass_ , o una clase de la clase base. Paso de NULL indica que la carpeta indicada por _lppEntryID_ es el valor predeterminado recibir carpeta para el almacén de mensajes. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La carpeta de recepción se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::GetReceiveFolder** Obtiene el identificador de entrada de una carpeta de recepción, una carpeta designada para recibir los mensajes entrantes de una clase de mensaje en particular. Los autores de llamadas pueden especificar una clase de mensaje o NULL en el parámetro _lpszMessageClass_ . Si _lpszMessageClass_ es NULL, **GetReceiveFolder** devuelve los siguientes valores: 
  
- En _lppszExplicitClass_, el nombre de la clase base inicial de la clase de mensaje que apunta _lpszMessageClass_ que establecer explícitamente una carpeta de recepción. 
    
- En _lppEntryID_, el identificador de entrada de la carpeta de recepción de la clase base indicada por el parámetro _lppszExplicitClass_ . 
    
Por ejemplo, supongamos que la carpeta de recepción de la clase de mensaje IPM **. Nota** se ha establecido para la entrada de identificador de la Bandeja de entrada y **GetReceiveFolder** se denomina con el contenido de _lpszMessageClass_ establecido en **IPM. Note.Phone**. Si **IPM. Note.Phone** no haya explícita recibe conjunto de carpetas, **GetReceiveFolder** devuelve el identificador de entrada de la Bandeja de entrada de _lppEntryID_ y **IPM. Nota** en _lppszExplicitClass_.
  
Si el cliente llama a **GetReceiveFolder** para una clase de mensaje y no ha establecido una carpeta de recepción para esa clase de mensaje, _lppszExplicitClass_ es una cadena de longitud cero, una cadena en formato Unicode o una cadena en formato ANSI dependiendo de si el cliente establecer el indicador MAPI_UNICODE en el parámetro _ulFlags indicado_ . 
  
Un valor predeterminado recibir carpeta, obtenido por pasando NULL en el parámetro _lpszMessageClass_ , siempre existe para cada almacén de mensajes. 
  
Un cliente debe llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) cuando se realiza con el identificador de entrada que se devuelven en _lppEntryID_ para liberar la memoria que contiene ese identificador de entrada. También debe llamar **MAPIFreeBuffer** cuando se hace con la cadena de la clase de mensaje devuelta en _lppszExplicitClass_ para liberar la memoria que contiene dicha cadena. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI usa el método **IMsgStore::GetReceiveFolder** para buscar la carpeta Bandeja de entrada.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

