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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321701"
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
  
> a Identificador de la ventana primaria del indicador de progreso que se muestra mientras se abre el formulario. El parámetro _ulUIParam_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ . 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se abre el formulario. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar el estado o solicitar información al usuario. Si no se establece esta marca, no se muestra ninguna interfaz de usuario.
    
MAPIFORM_EXACTMATCH 
  
> Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.
    
 _lpszMessageClass_
  
> a Un puntero a una cadena que da nombre a la clase de mensaje del mensaje que se va a cargar. Si se pasa NULL en el parámetro _lpszMessageClass_ , la clase de mensaje se determina a partir del mensaje al que señala el parámetro _PMSG_ . 
    
 _ulMessageStatus_
  
> a Una máscara de bits de marcas definidas por el cliente o por el proveedor que se copian de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje que proporciona información sobre el estado del mensaje. El parámetro _ulMessageStatus_ debe establecerse si _LPSZMESSAGECLASS_ no es null; de lo contrario, se omite _ulMessageStatus_ . 
    
 _ulMessageFlags_
  
> a Un puntero a una máscara de máscara de marcas copiada de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje que indica el estado actual del mensaje. El parámetro _ulMessageFlags_ debe establecerse si _LPSZMESSAGECLASS_ no es null; de lo contrario, se omite _ulMessageFlags_ . 
    
 _pFolderFocus_
  
> a Un puntero a la carpeta que contiene directamente el mensaje. El parámetro _pFolderFocus_ puede ser null si no existe una carpeta de este tipo (por ejemplo, si el mensaje está incrustado en otro mensaje). 
    
 _pMessageSite_
  
> a Un puntero al sitio del mensaje del mensaje.
    
 _PMSG_
  
> a Un puntero al mensaje.
    
 _pViewContext_
  
> a Un puntero al contexto de la vista para el mensaje. El parámetro _pViewContext_ puede ser null. 
    
 _riid_
  
> a Identificador de interfaz (IID) de la interfaz que se va a usar para el objeto de formulario devuelto. El parámetro _riid_ no debe ser nulo. 
    
 _ppvObj_
  
> contempla Un puntero a un puntero a la interfaz devuelta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> El formulario no es compatible con la interfaz solicitada.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje pasada en _lpszMessageClass_ no coincide con la clase de mensaje de ningún formulario de la biblioteca de formularios. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: LoadForm** para abrir un formulario de un mensaje existente. **LoadForm** abre el objeto Form, carga el mensaje en el objeto de formulario, configura el contexto de vista apropiado, si es necesario, y devuelve la interfaz solicitada para el objeto de formulario. 
  
El parámetro _pFolderFocus_ apunta a la carpeta que contiene el mensaje. Si el mensaje está incrustado en otro mensaje, _pFolderFocus_ debe ser null. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si se pasa NULL en _lpszMessageClass_, la implementación obtiene la clase de mensaje, el estado y las marcas del mensaje del **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** y **PR_MESSAGE_FLAGS **propiedades. Si se proporciona una cadena de clase de mensaje en _lpszMessageClass_, la implementación debe usar los valores de _ulMessageStatus_ y _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa el método **IMAPIFormMgr:: LoadForm** para cargar un formulario antes de mostrarlo.  <br/> |
   
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

