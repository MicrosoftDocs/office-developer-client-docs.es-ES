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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423583"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Presenta un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe ese formulario.
  
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
  
> [in] Identificador de la ventana principal del cuadro de diálogo mostrado. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
 _pszTitle_
  
> [in] Puntero a una cadena que contiene el título del cuadro de diálogo. Si el  _parámetro pszTitle_ es NULL, el proveedor de biblioteca de formularios proporciona un título predeterminado. 
    
 _pfld_
  
> [in] Puntero a la carpeta desde la que se va a seleccionar el formulario. Si el  _parámetro pfld_ es NULL, el formulario se puede seleccionar desde el contenedor del formulario local, personal u organización. 
    
 _ppfrminfoReturned_
  
> [salida] Puntero a un puntero al objeto de información del formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** del cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::SelectForm** para presentar primero un cuadro de diálogo que permita al usuario seleccionar un formulario y, a continuación, recuperar un objeto de información de formulario que describa el formulario seleccionado. El cuadro de diálogo limita al usuario a seleccionar un solo formulario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

El **cuadro de diálogo Seleccionarformulario** muestra solo formularios que no están ocultos (es decir, formularios que tienen sus propiedades ocultas borradas). Si un visor de formulario pasa la marca MAPI_UNICODE en el  _parámetro ulFlags,_ todas las cadenas son Unicode. Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI usa el **método IMAPIFormMgr::SelectForm** para seleccionar un formulario y enviar información sobre el formulario a uno o varios registros.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

