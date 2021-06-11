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
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321640"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una [interfaz IMAPIFormContainer](imapiformcontaineriunknown.md) para un contenedor de formulario específico. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameters

 _hfrmreg_
  
> [in] Enumeración HFRMREG que indica la biblioteca de formularios que se va a abrir (es decir, el contenedor de formularios que se va a abrir). Una enumeración HFRMREG es una enumeración específica de un proveedor de biblioteca de formularios. Entre los valores posibles de HFRMREG se incluyen los siguientes:
    
HFRMREG_DEFAULT 
  
> Un contenedor de formulario cómodo.
    
HFRMREG_FOLDER 
  
> Un contenedor de carpetas. 
    
HFRMREG_PERSONAL 
  
> Contenedor del almacén de mensajes predeterminado. 
    
HFRMREG_LOCAL 
  
> Un contenedor de formulario local. 
    
 _lpunk_
  
> [in] Puntero al objeto para el que se abre la interfaz. El  _parámetro lpunk_ debe ser **null** a menos que el valor del parámetro  _hfrmreg_ requiera un puntero de objeto. 
    
 _lppfcnt_
  
> [salida] Puntero a un puntero al objeto contenedor de formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_INTERFACE 
  
> El objeto señalado por  _lpunk_ no admite la interfaz necesaria. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::OpenFormContainer** para abrir una **interfaz IMAPIFormContainer** para un contenedor de formulario específico. A continuación, esta interfaz se puede usar para instalar formularios en un contenedor de formularios y quitar los formularios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el valor de _hfrmreg_ es HFRMREG_FOLDER, el identificador de interfaz usado en _lpunk_ debe ser distinto de **null** y debe permitir llamadas del método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) a una [interfaz IMAPIFolder.](imapifolderimapicontainer.md) 
  
Para abrir el contenedor de formulario local, debe usar una llamada al método **OpenFormContainer** o a la [función MAPIOpenLocalFormContainer;](mapiopenlocalformcontainer.md) no puede usar el [método IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir al usuario seleccionar el contenedor del formulario local. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI usa el método **IMAPIFormMgr::OpenFormContainer** para recuperar un contenedor de formulario para que se pueda representar el contenido del contenedor.  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI usa el método **IMAPIFormMgr::OpenFormContainer** para recuperar un contenedor de formulario para una carpeta de modo que se pueda representar el contenido del contenedor.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

