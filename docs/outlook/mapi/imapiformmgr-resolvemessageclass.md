---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426397"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Resuelve una clase de mensaje en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Parameters

 _szMsgClass_
  
> [in] Cadena que nombra la clase de mensaje que se está resolviendo.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se resuelve la clase de mensaje. Se puede establecer la siguiente marca:
    
MAPIFORM_EXACTMATCH 
  
> Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.
    
 _pFolderFocus_
  
> [in] Puntero a la carpeta que contiene el mensaje que se está resolviendo. El  _parámetro pFolderFocus_ puede ser NULL. 
    
 _ppResult_
  
> [salida] Puntero a un puntero a un objeto de información de formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje pasada en  _el parámetro szMsgClass_ no coincide con la clase de mensaje para ningún formulario de la biblioteca de formularios. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::ResolveMessageClass** para resolver una clase de mensaje en su formulario dentro de un contenedor de formularios. El objeto de información del formulario devuelto en el  _parámetro ppResult_ proporciona acceso adicional a las propiedades del formulario que tiene la clase de mensaje determinada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver una clase de mensaje en un formulario, un visor de formulario pasa el nombre de la clase de mensaje que se va a resolver, como " `IPM.HelpDesk.Software` ". Para forzar que la resolución sea exacta (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando no hay disponible un servidor de formulario que coincida exactamente), se puede pasar la marca MAPIFORM_EXACTMATCH en el _parámetro ulFlags._ Si el  _parámetro pFolderFocus_ es NULL, el proceso de resolución de clase de mensaje no busca en un contenedor de carpetas. 
  
El orden de los contenedores buscados depende de la implementación del proveedor de biblioteca de formularios. El proveedor de biblioteca de formularios predeterminado busca primero el contenedor local, después el contenedor de carpetas para la carpeta pasada, el contenedor de formulario personal y, por último, el contenedor de la organización.
  
Los nombres de clase de mensaje siempre son cadenas ANSI, nunca Unicode.
  
El identificador de clase de la clase de mensaje resuelto se devuelve como parte del objeto de información del formulario. Un visor de formularios no debe funcionar en la suposición de que el identificador de clase existe en la biblioteca OLE hasta después de que el visor de formulario haya llamado al método [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) o al método [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="see-also"></a>Vea también



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

