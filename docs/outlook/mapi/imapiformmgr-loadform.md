---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418788"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia un formulario para abrir un mensaje existente.
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal del indicador de progreso que se muestra mientras se abre el formulario. El _parámetro ulUIParam_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el formulario. Se pueden establecer las siguientes marcas:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar estado o solicitar al usuario más información. Si no se establece esta marca, no se muestra ninguna interfaz de usuario.
    
MAPIFORM_EXACTMATCH 
  
> Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.
    
 _lpszMessageClass_
  
> [in] Puntero a una cadena que nombra la clase de mensaje del mensaje que se va a cargar. Si se pasa NULL en el parámetro _lpszMessageClass,_ la clase de mensaje se determina a partir del mensaje al que apunta el _parámetro pmsg._ 
    
 _ulMessageStatus_
  
> [in] Máscara de bits de marcas definidas por el cliente o definidas por el proveedor copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje que proporciona información sobre el estado del mensaje. El _parámetro ulMessageStatus_ debe establecerse _si lpszMessageClass_ no es NULL; de lo contrario, se omite _ulMessageStatus._ 
    
 _ulMessageFlags_
  
> [in] Puntero a una máscara de bits de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje que indica el estado actual del mensaje. El _parámetro ulMessageFlags_ debe establecerse si _lpszMessageClass_ no es NULL; de lo contrario, se omite _ulMessageFlags._ 
    
 _pFolderFocus_
  
> [in] Puntero a la carpeta que contiene directamente el mensaje. El  _parámetro pFolderFocus_ puede ser NULL si dicha carpeta no existe (por ejemplo, si el mensaje está incrustado en otro mensaje). 
    
 _pMessageSite_
  
> [in] Puntero al sitio del mensaje.
    
 _pmsg_
  
> [in] Puntero al mensaje.
    
 _pViewContext_
  
> [in] Puntero al contexto de vista del mensaje. El  _parámetro pViewContext_ puede ser NULL. 
    
 _riid_
  
> [in] Identificador de interfaz (IID) de la interfaz que se usará para el objeto de formulario devuelto. El  _parámetro riid_ no debe ser NULL. 
    
 _ppvObj_
  
> [salida] Puntero a un puntero a la interfaz devuelta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> El formulario no admite la interfaz solicitada.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje pasada  _en lpszMessageClass_ no coincide con la clase de mensaje para ningún formulario de la biblioteca de formularios. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman **al método IMAPIFormMgr::LoadForm** para abrir un formulario para un mensaje existente. **LoadForm** abre el objeto de formulario, carga el mensaje en el objeto de formulario, configura el contexto de vista adecuado, si es necesario, y devuelve la interfaz solicitada para el objeto de formulario. 
  
El  _parámetro pFolderFocus_ apunta a la carpeta que contiene el mensaje. Si el mensaje está incrustado en otro mensaje,  _pFolderFocus_ debe ser NULL. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si se pasa NULL en  _lpszMessageClass_, la implementación obtiene la clase de mensaje, el estado y las marcas del mensaje de las propiedades **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md) **),** PR_MSG_STATUS y **PR_MESSAGE_FLAGS** mensaje. Si se proporciona una cadena de clase de mensaje en  _lpszMessageClass_, la implementación debe usar los valores  _de ulMessageStatus_ y  _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa el **método IMAPIFormMgr::LoadForm** para cargar un formulario antes de mostrarlo.  <br/> |
   
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

