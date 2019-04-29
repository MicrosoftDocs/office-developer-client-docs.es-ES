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
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428021"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Resuelve un grupo de clases de mensaje en sus formularios dentro de un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _pMsgClasses_
  
> a Un puntero a una matriz que contiene los nombres de las clases de mensaje que se van a resolver.
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se resuelven las clases de mensaje. Se puede establecer la siguiente marca:
    
MAPIFORM_EXACTMATCH 
  
> Solo se deben resolver las cadenas de clase de mensaje que sean una coincidencia exacta.
    
MAPIFORM_LOCALONLY
  
> No incluya formularios en caché.
    
 _pFolderFocus_
  
> a Un puntero a la carpeta que contiene el formulario cuya clase de mensaje se está resolviendo. El parámetro _pFolderFocus_ puede ser null. 
    
 _ppfrminfoarray_
  
> contempla Un puntero a un puntero a una matriz de objetos de información de formulario. Si un visor de formularios pasa NULL en el parámetro _pMsgClasses_ , el parámetro _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios del contenedor. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: ResolveMultipleMessageClasses** para resolver un grupo de clases de mensaje a los formularios dentro de un contenedor de formularios. La matriz de objetos de información de formulario devuelta en _ppfrminfoarray_ proporciona acceso a todas las propiedades de los formularios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver un grupo de clases de mensaje en formularios, un visor de formulario pasa una matriz de nombres de clase de mensaje que se van a resolver. Para forzar que la resolución sea exacta (es decir, para evitar la resolución en una clase base de la clase de mensaje cuando no hay disponible un servidor de formularios que coincida exactamente), se puede pasar la marca MAPIFORM_EXACTMATCH en el parámetro _ulFlags_ . 
  
Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.
  
Si una clase de mensaje no se puede resolver en un formulario, se devuelve NULL para dicha clase de mensaje en la matriz de información del formulario. Por lo tanto, incluso si el método devuelve S_OK, los visores de formularios no deberían trabajar en el supuesto de que todas las clases de mensaje se han resuelto correctamente. En su lugar, los visores de formulario deben comprobar los valores de la matriz devuelta.
  
## <a name="see-also"></a>Ver también



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

