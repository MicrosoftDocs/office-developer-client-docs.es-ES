---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428595"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto contenedor seleccionado por el usuario.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal del cuadro de diálogo mostrado. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se selecciona la biblioteca de formularios (es decir, cómo se selecciona el contenedor de formularios). Se pueden establecer las siguientes marcas:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> La selección se puede realizar desde todos los contenedores. Este es el tipo de selección predeterminado. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> La selección solo se puede realizar desde contenedores de carpetas.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> La selección solo se puede realizar desde contenedores que no están asociados con carpetas.
    
 _lppfcnt_
  
> [salida] Puntero a un puntero a la interfaz devuelta. Esta interfaz es para el objeto contenedor seleccionado por el usuario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios normalmente llaman al método **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario en el que está instalado un formulario. **SelectFormContainer** no se puede usar para seleccionar el contenedor de formulario local, que tiene el valor HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI usa el **método IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario antes de representar su contenido.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

