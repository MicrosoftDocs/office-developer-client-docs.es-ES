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
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577929"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Presenta un cuadro de diálogo que permite al usuario seleccionar un contenedor de formulario y devuelve una interfaz para el objeto de contenedor seleccionado por el usuario.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del cuadro de diálogo que se muestra. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se selecciona la biblioteca de formularios (es decir, cómo el contenedor de formulario está seleccionado). Se pueden establecer los siguientes indicadores:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Selección se puede realizar desde todos los contenedores. Éste es el tipo de selección de forma predeterminada. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Selección puede realizarse sólo de los contenedores de la carpeta.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Selección puede realizarse sólo de los contenedores que no estén asociados con las carpetas.
    
 _lppfcnt_
  
> [out] Un puntero a un puntero a la interfaz devuelta. Esta interfaz es para el objeto de contenedor que se ha seleccionado por el usuario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Visores de formulario normalmente llama al método de **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario en el que está instalado un formulario. **SelectFormContainer** no se puede usar para seleccionar el contenedor de forma local, que tiene el valor HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI usa el método **IMAPIFormMgr::SelectFormContainer** para seleccionar un contenedor de formulario antes de representar su contenido.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

