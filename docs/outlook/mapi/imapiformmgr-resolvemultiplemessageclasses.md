---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571699"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se resuelve un grupo de clases de mensajes en sus formularios dentro de un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parámetros

 _pMsgClasses_
  
> [entrada] Un puntero a una matriz que contiene los nombres de las clases de mensaje para resolver.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se resuelven las clases de mensaje. Se puede establecer la marca siguiente:
    
MAPIFORM_EXACTMATCH 
  
> Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.
    
MAPIFORM_LOCALONLY
  
> No incluya los formularios en caché.
    
 _pFolderFocus_
  
> [entrada] Un puntero a la carpeta que contiene el formulario se resuelve cuya clase de mensaje. El parámetro _pFolderFocus_ puede ser NULL. 
    
 _ppfrminfoarray_
  
> [out] Un puntero a un puntero a una matriz de objetos de información del formulario. Si un visor de formulario pasa NULL en el parámetro _pMsgClasses_ , el parámetro _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios en el contenedor. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llaman al método **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver un grupo de clases de mensajes a los formularios dentro de un contenedor de formulario. La matriz de objetos de información de formulario devueltos en _ppfrminfoarray_ aún más proporciona acceso a cada una de las propiedades de los formularios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver un grupo de clases de mensajes a los formularios, un visor de formulario se pasa en una matriz de nombres de clase de mensaje que se va a resolver. Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase base de la clase de mensaje cuando un formulario que coincide exactamente server no está disponible) se puede pasar el indicador MAPIFORM_EXACTMATCH en el parámetro _ulFlags indicado_ . 
  
Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.
  
Si una clase de mensaje no se puede resolver a un formulario, se devuelve NULL para esa clase de mensaje en la matriz de información de formulario. Por lo tanto, incluso si el método devuelve S_OK, visores de formulario no deben trabajar en la suposición de que se han resueltos correctamente todas las clases de mensaje. En su lugar, los visores de formulario deben comprobar los valores de la matriz devuelta.
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

