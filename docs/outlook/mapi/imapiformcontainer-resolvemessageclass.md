---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817283"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Hace referencia a**: Outlook 
  
Una clase de mensaje se resuelve en su formulario en un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parámetros

 _szMessageClass_
  
> [entrada] Una cadena que da nombre a la clase de mensaje que se resuelve. Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se resuelve la clase de mensaje. Se puede establecer la marca siguiente:
    
MAPIFORM_EXACTMATCH 
  
> Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.
    
 _ppforminfo_
  
> [out] Un puntero a un puntero al objeto de información de formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje que se pasa en el parámetro _szMessageClass_ no coincide con la clase de mensaje para cualquier formulario en el contenedor de formulario. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llaman al método **IMAPIFormContainer::ResolveMessageClass** para resolver una clase de mensaje a un formulario dentro de un contenedor de formulario. El objeto de información de formulario devuelto en el parámetro _ppforminfo_ aún más proporciona acceso a las propiedades del formulario con la clase de mensaje determinado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver una clase de mensaje a un formulario, pase el nombre de la clase de mensaje que se va a resolver (por ejemplo, `IPM.HelpDesk.Software`). Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase de la clase de mensaje base), el indicador MAPIFORM_EXACTMATCH se puede pasar en el parámetro _ulFlags_ . 
  
Se devuelve el identificador de clase para la clase de mensaje resuelto como parte del objeto de información de formulario. No se supone que existe el identificador de clase en la biblioteca OLE hasta después de llamar a los métodos [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) o [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI utiliza el método **IMAPIFormContainer::ResolveMessageClass** para localizar un formulario que está asociado a una clase de mensaje.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

