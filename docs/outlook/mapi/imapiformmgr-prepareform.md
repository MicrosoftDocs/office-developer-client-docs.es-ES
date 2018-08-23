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
ms.openlocfilehash: 6e8ea7230ae86dee99cc4413715055fc53afa900
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579728"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Descargas de un formulario para abrirlo.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso que se muestra mientras se descarga el formulario. El parámetro _ulUIParam_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ . 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se descarga el formulario. Se puede establecer la marca siguiente:
    
MAPI_DIALOG 
  
> Muestra una interfaz de usuario para proporcionar el estado o solicite al usuario para obtener más información. Si no se establece este marcador, no se muestra ninguna interfaz de usuario.
    
 _pfrmiInfo_
  
> [entrada] Un puntero a un objeto de información de formulario para el formulario que se va a descargar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormMgr::PrepareForm** para descargar un formulario desde un contenedor de formulario para abrirlo. La mayoría de los visores de formulario no es necesario llamar a **PrepareForm**, debido a que la [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) y el [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) métodos llaman **PrepareForm**, si es necesario. 
  
Puede usar **PrepareForm** para obtener las bibliotecas de vínculos dinámicos (DLL) y otros archivos asociados con un formulario para modificarlos. Si se carga el formulario modificado en su contenedor de formulario, se debe volver a instalar. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

