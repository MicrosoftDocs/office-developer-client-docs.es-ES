---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ed3f793e4353cf78949a9df3a17dd3997a573f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817306"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Hace referencia a**: Outlook 
  
Se abre un formulario para crear un nuevo mensaje en función de la clase de mensaje del formulario.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal para el indicador de progreso que se muestra mientras se abre el formulario. El parámetro _ulUIParam_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el formulario. Se puede establecer la marca siguiente:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar el estado o solicite al usuario para obtener más información. Si no se establece este marcador, no se muestra ninguna interfaz de usuario.
    
 _pfrminfoToActivate_
  
> [entrada] Un puntero al objeto de información de formulario que se usa para abrir el formulario.
    
 _refiidToAsk_
  
> [entrada] Un puntero para el identificador de interfaz (IID) para la interfaz que se devolverá para el objeto de formulario que se creó. El parámetro _refiidToAsk_ no debe ser NULL. 
    
 _ppvObj_
  
> [out] Un puntero a un puntero a la interfaz devuelta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> No se admite la interfaz solicitada por el objeto de formulario.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormMgr::CreateForm** para abrir un formulario para crear un nuevo mensaje en función de la clase de mensaje del formulario. **CreateForm** abre el formulario mediante la creación de una instancia del servidor de formulario para ese formulario tal como se describe en el objeto de información de formulario determinado. Si es necesario, **CreateForm** llama al método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) para descargar el código de servidor del formulario en el disco del usuario. 
  
El parámetro _pfrminfoToActivate_ debe apuntar a un objeto de información de formulario que se ha resuelto correctamente. 
  
Después de que se ha abierto el formulario, el Visor de formulario llamada debe configurar un mensaje mediante la interfaz de [IPersistMessage](ipersistmessageiunknown.md) y, opcionalmente, puede configurar un contexto de vista para el formulario. Para obtener más información, vea [iniciar un servidor de formulario](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa el método **IMAPIFormMgr::CreateForm** para crear un formulario antes de mostrarla.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Iniciar un servidor de formulario](launching-a-form-server.md)

