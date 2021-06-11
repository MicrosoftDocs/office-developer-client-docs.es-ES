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
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419852"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre un formulario para crear un nuevo mensaje basado en la clase de mensaje del formulario.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal para el indicador de progreso que se muestra mientras se abre el formulario. El _parámetro ulUIParam_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el formulario. Se puede establecer la siguiente marca:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar estado o solicitar al usuario más información. Si no se establece esta marca, no se muestra ninguna interfaz de usuario.
    
 _pfrminfoToActivate_
  
> [in] Puntero al objeto de información del formulario que se usa para abrir el formulario.
    
 _refiidToAsk_
  
> [in] Puntero al identificador de interfaz (IID) para la interfaz que se devolverá para el objeto de formulario que se creó. El  _parámetro refiidToAsk_ no debe ser NULL. 
    
 _ppvObj_
  
> [salida] Puntero a un puntero a la interfaz devuelta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> La interfaz solicitada no es compatible con el objeto de formulario.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::CreateForm** para abrir un formulario para crear un nuevo mensaje basado en la clase de mensaje del formulario. **CreateForm** abre el formulario creando una instancia del servidor de formularios para ese formulario, tal como se describe en el objeto de información del formulario especificado. Si es necesario, **CreateForm** llama al método [IMAPIFormMgr::P repareForm para](imapiformmgr-prepareform.md) descargar el código del servidor de formulario en el disco del usuario. 
  
El  _parámetro pfrminfoToActivate_ debe apuntar a un objeto de información de formulario que se haya resuelto correctamente. 
  
Una vez abierto el formulario, el visor de formularios de llamada debe configurar un mensaje mediante la interfaz [IPersistMessage](ipersistmessageiunknown.md) y, opcionalmente, puede configurar un contexto de vista para el formulario. Para obtener más información, vea [Launching a Form Server](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa el **método IMAPIFormMgr::CreateForm** para crear un formulario antes de mostrarlo.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Iniciar un servidor de formularios](launching-a-form-server.md)

