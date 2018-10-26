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
ms.openlocfilehash: 3e758acfa1cf0c11be666dd730d9bf589d2e9d77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586217"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso que se muestra mientras se abre el formulario. El parámetro _ulUIParam_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el formulario. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar el estado o solicite al usuario para obtener más información. Si no se establece este marcador, no se muestra ninguna interfaz de usuario.
    
MAPIFORM_EXACTMATCH 
  
> Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.
    
 _lpszMessageClass_
  
> [entrada] Un puntero a una cadena que da nombre a la clase de mensaje del mensaje que se va a cargar. Si se pasa NULL en el parámetro _lpszMessageClass_ , se determina la clase de mensaje del mensaje indicada por el parámetro _pmsg_ . 
    
 _ulMessageStatus_
  
> [entrada] Una máscara de bits de definidas por el cliente o definidas por el proveedor de indicadores que se copió desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje que proporciona información sobre el estado del mensaje. El parámetro _ulMessageStatus_ debe establecerse si _lpszMessageClass_ no es NULL; de lo contrario, se omite _ulMessageStatus_ . 
    
 _ulMessageFlags_
  
> [entrada] Un puntero a una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje que indica el estado actual del mensaje. El parámetro _ulMessageFlags_ debe establecerse si _lpszMessageClass_ no es NULL; de lo contrario, se omite _ulMessageFlags_ . 
    
 _pFolderFocus_
  
> [entrada] Un puntero a la carpeta que contiene directamente el mensaje. El parámetro _pFolderFocus_ puede ser NULL si no existe como una carpeta (por ejemplo, si el mensaje está incrustado en otro mensaje). 
    
 _pMessageSite_
  
> [entrada] Un puntero al sitio de mensaje del mensaje.
    
 _pMsg_
  
> [entrada] Un puntero al mensaje.
    
 _pViewContext_
  
> [entrada] Un puntero al contexto de vista para el mensaje. El parámetro _pViewContext_ puede ser NULL. 
    
 _riid_
  
> [entrada] El identificador de interfaz (IID) de la interfaz que se usará para el objeto de formulario devuelto. El parámetro _riid_ no debe ser NULL. 
    
 _ppvObj_
  
> [out] Un puntero a un puntero a la interfaz devuelta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> El formulario no es compatible con la interfaz solicitada.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje que se pasó _lpszMessageClass_ no coincide con la clase de mensaje para cualquier formulario en la biblioteca de formularios. 
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormMgr::LoadForm** para abrir un formulario para un mensaje existente. **LoadForm** abre el objeto de formulario, se carga el mensaje en el objeto de formulario, se configura el contexto de vista apropiada, si es necesario y se devuelve la interfaz solicitada para el objeto de formulario. 
  
El parámetro _pFolderFocus_ apunta a la carpeta que contiene el mensaje. Si el mensaje está incrustado en otro mensaje, _pFolderFocus_ debe ser nulo. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si se pasa NULL en _lpszMessageClass_, la implementación obtiene la clase de mensaje del mensaje, estado y los indicadores desde el mensaje **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** y **PR_MESSAGE_FLAGS **propiedades. Si se proporciona una cadena de la clase de mensaje en _lpszMessageClass_, la implementación debe usar los valores de _ulMessageStatus_ y _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa el método **IMAPIFormMgr::LoadForm** para cargar un formulario antes de mostrarla.  <br/> |
   
## <a name="see-also"></a>Vea también



[Propiedad canónico PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propiedad canónico PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónico PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

