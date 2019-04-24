---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321675"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe dicho formulario.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana principal del cuadro de diálogo que se muestra. 
    
 _ulFlags_
  
> a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _pszTitle_
  
> a Un puntero a una cadena que contiene el título del cuadro de diálogo. Si el parámetro _pszTitle_ es null, el proveedor de la biblioteca de formularios proporciona un título predeterminado. 
    
 _pfld_
  
> a Puntero a la carpeta desde la que se va a seleccionar el formulario. Si el parámetro _pfld_ es null, el formulario puede seleccionarse desde el contenedor de formulario local, personal o de la organización. 
    
 _ppfrminfoReturned_
  
> contempla Un puntero a un puntero al objeto de información del formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: SelectForm** para presentar primero un cuadro de diálogo que permite al usuario seleccionar un formulario y, a continuación, recuperar un objeto de información de formulario que describe el formulario seleccionado. El cuadro de diálogo restringe al usuario que seleccione un solo formulario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El cuadro de diálogo **SelectForm** muestra sólo los formularios que no están ocultos (es decir, los formularios que tienen sus propiedades ocultas en blanco). Si un visor de formularios pasa la marca MAPI_UNICODE en el parámetro _ulFlags_ , todas las cadenas son Unicode. Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSelectForm  <br/> |MFCMAPI usa el método **IMAPIFormMgr:: SelectForm** para seleccionar un formulario y enviar información sobre el formulario a uno o más registros.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

