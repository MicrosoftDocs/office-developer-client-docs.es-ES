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
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408554"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Resuelve una clase de mensaje en su formulario en un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parameters

 _szMessageClass_
  
> [in] Cadena que nombra la clase de mensaje que se está resolviendo. Los nombres de clase de mensaje siempre son cadenas ANSI, nunca Unicode.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se resuelve la clase de mensaje. Se puede establecer la siguiente marca:
    
MAPIFORM_EXACTMATCH 
  
> Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.
    
 _ppforminfo_
  
> [salida] Puntero a un puntero al objeto de información del formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje pasada en  _el parámetro szMessageClass_ no coincide con la clase de mensaje para ningún formulario del contenedor de formularios. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman **al método IMAPIFormContainer::ResolveMessageClass** para resolver una clase de mensaje en un formulario dentro de un contenedor de formularios. El objeto de información del formulario devuelto en el  _parámetro ppforminfo_ proporciona acceso adicional a las propiedades del formulario con la clase de mensaje determinada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver una clase de mensaje en un formulario, pase el nombre de la clase de mensaje que se va a resolver (por ejemplo,  `IPM.HelpDesk.Software` ). Para forzar que la resolución sea exacta (es decir, para evitar la resolución a una clase base de la clase de mensaje), la marca MAPIFORM_EXACTMATCH se puede pasar en el _parámetro ulFlags._ 
  
El identificador de clase de la clase de mensaje resuelto se devuelve como parte del objeto de información del formulario. No suponga que el identificador de clase existe en la biblioteca OLE hasta después de llamar al método [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) o [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI usa el **método IMAPIFormContainer::ResolveMessageClass** para buscar un formulario asociado a una clase de mensaje.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

