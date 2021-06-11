---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416653"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Descarga un formulario para su apertura.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Identificador de la ventana principal del indicador de progreso que se muestra mientras se descarga el formulario. El _parámetro ulUIParam_ se omite a menos que MAPI_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se descarga el formulario. Se puede establecer la siguiente marca:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar estado o solicitar al usuario más información. Si no se establece esta marca, no se muestra ninguna interfaz de usuario.
    
 _pfrmiInfo_
  
> [in] Puntero a un objeto de información de formulario para el formulario que se va a descargar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::P repareForm** para descargar un formulario de un contenedor de formularios para su apertura. La mayoría de los visores de formulario no necesitan llamar a **PrepareForm**, porque los métodos [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) e [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) llaman a **PrepareForm**, si es necesario. 
  
Puede usar **PrepareForm para** obtener las bibliotecas de vínculos dinámicos (DLL) y otros archivos asociados con un formulario para modificarlas. Si el formulario modificado se vuelve a cargar en el contenedor del formulario, debe volver a instalarse. 
  
## <a name="see-also"></a>Vea también



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

