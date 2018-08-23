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
ms.openlocfilehash: 3cd84e4ddb6d722d9f3de11d65b100d86e69ecae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571818"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una clase de mensaje se resuelve en su formulario dentro de un contenedor de formulario y devuelve un objeto de información de formulario para ese formulario.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Parámetros

 _szMsgClass_
  
> [entrada] Una cadena que da nombre a la clase de mensaje que se resuelve.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se resuelve la clase de mensaje. Se puede establecer la marca siguiente:
    
MAPIFORM_EXACTMATCH 
  
> Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.
    
 _pFolderFocus_
  
> [entrada] Un puntero a la carpeta que contiene el mensaje que se resuelve. El parámetro _pFolderFocus_ puede ser NULL. 
    
 _ppResult_
  
> [out] Un puntero a un puntero a un objeto de información de formulario devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje que se pasa en el parámetro _szMsgClass_ no coincide con la clase de mensaje para cualquier formulario en la biblioteca de formularios. 
    
## <a name="remarks"></a>Comentarios

Visores de formulario llaman al método **IMAPIFormMgr::ResolveMessageClass** para resolver una clase de mensaje para su formulario dentro de un contenedor de formulario. El objeto de información de formulario devuelto en el parámetro _ppResult_ aún más proporciona acceso a las propiedades del formulario que tiene la clase de mensaje determinado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver una clase de mensaje a un formulario, se pasa un visor de formulario en el nombre de la clase de mensaje para que se resuelvan, como " `IPM.HelpDesk.Software`". Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando un formulario que coincide exactamente server no está disponible), el indicador MAPIFORM_EXACTMATCH se puede pasar en el parámetro _ulFlags indicado_ . Si el parámetro _pFolderFocus_ es NULL, el proceso de resolución de la clase de mensaje no busca en un contenedor de carpeta. 
  
El orden de los contenedores que desea buscado depende de la implementación del proveedor de la biblioteca de formulario. El proveedor de biblioteca del formulario predeterminado busca en primer lugar el contenedor local y, a continuación, el contenedor de la carpeta de la carpeta en el pasado, el contenedor de formularios personal y, por último, el contenedor de la organización.
  
Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.
  
Se devuelve el identificador de clase para la clase de mensaje resuelto como parte del objeto de información de formulario. Un visor de formulario no debe trabajar en la suposición de que existe el identificador de clase en la biblioteca OLE hasta después de que el Visor de formulario ha llamado al método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) o el método [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

