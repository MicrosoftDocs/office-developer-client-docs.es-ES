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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321612"
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
  
> a Una cadena que asigna un nombre a la clase de mensaje que se está resolviendo.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se resuelve la clase de mensaje. Se puede establecer la siguiente marca:
    
MAPIFORM_EXACTMATCH 
  
> Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.
    
 _pFolderFocus_
  
> a Un puntero a la carpeta que contiene el mensaje que se está resolviendo. El parámetro _pFolderFocus_ puede ser null. 
    
 _ppResult_
  
> contempla Un puntero a un puntero a un objeto devuelto de información de formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje pasada en el parámetro _szMsgClass_ no coincide con la clase de mensaje de ningún formulario de la biblioteca de formularios. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: ResolveMessageClass** para resolver una clase de mensaje para su formulario dentro de un contenedor de formularios. El objeto de información de formulario devuelto en el parámetro _ppResult_ proporciona más acceso a las propiedades del formulario que tiene la clase de mensaje determinada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver una clase de mensaje en un formulario, un visor de formulario pasa el nombre de la clase de mensaje que se va a resolver `IPM.HelpDesk.Software`, como "". Para forzar que la resolución sea exacta (es decir, para evitar la resolución en una clase base de la clase de mensaje cuando no está disponible un servidor de formularios que coincida exactamente), se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags_ . Si el parámetro _pFolderFocus_ es null, el proceso de resolución de la clase de mensaje no busca en un contenedor de carpetas. 
  
El orden de los contenedores buscados depende de la implementación del proveedor de la biblioteca de formularios. El proveedor de bibliotecas de formularios predeterminado busca primero en el contenedor local, luego en el contenedor de carpetas de la carpeta pasada, en el contenedor de formularios personales y, por último, en el contenedor de la organización.
  
Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.
  
El identificador de clase de la clase de mensaje resuelta se devuelve como parte del objeto de información de formulario. Un visor de formularios no debe trabajar en caso de que el identificador de clase exista en la biblioteca OLE hasta que el visor de formulario haya llamado al método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) o al método [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) . 
  
## <a name="see-also"></a>Vea también



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

