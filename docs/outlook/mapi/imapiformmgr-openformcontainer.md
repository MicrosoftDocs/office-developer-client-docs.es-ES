---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bf3d9159dd1ed31fb93569218770f1015579339
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582927"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se abre una interfaz de [IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de forma específicos. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parámetros

 _hfrmreg_
  
> [entrada] Una enumeración HFRMREG que indica la biblioteca de formularios para abrir (es decir, el contenedor de formulario para abrir). Una enumeración HFRMREG es una enumeración que es específica de un proveedor de la biblioteca de formulario. Los valores posibles de HFRMREG incluyen lo siguiente:
    
HFRMREG_DEFAULT 
  
> Un contenedor conveniente formulario.
    
HFRMREG_FOLDER 
  
> Un contenedor de carpeta. 
    
HFRMREG_PERSONAL 
  
> El contenedor para el almacén de mensajes predeterminado. 
    
HFRMREG_LOCAL 
  
> Un contenedor de forma local. 
    
 _lpUnk_
  
> [entrada] Un puntero al objeto para el que se abre la interfaz. El parámetro _lpunk_ debe ser **null** a menos que el valor para el parámetro _hfrmreg_ requiere un puntero de objeto. 
    
 _lppfcnt_
  
> [out] Un puntero a un puntero al objeto de contenedor de formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> El objeto al que señala por _lpunk_ no es compatible con la interfaz necesaria. 
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormMgr::OpenFormContainer** para abrir una interfaz **IMAPIFormContainer** para un contenedor de forma específicos. A continuación, se puede usar esta interfaz para instalar formularios en y formularios de eliminación de un contenedor de formulario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el valor de _hfrmreg_ es HFRMREG_FOLDER, el identificador de interfaz que se usa en _lpunk_ debe ser distinto de **null** y debe permitir llamadas al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) a una interfaz [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Para abrir el contenedor de forma local, debe usar una llamada al método **OpenFormContainer** o la función [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; no puede usar el método [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir que el usuario seleccionar el contenedor de forma local. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI usa el método **IMAPIFormMgr::OpenFormContainer** para recuperar un contenedor de formulario por lo que se puede representar el contenido del contenedor.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI usa el método **IMAPIFormMgr::OpenFormContainer** para recuperar un contenedor de formulario para una carpeta, por lo que se puede representar el contenido del contenedor.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

