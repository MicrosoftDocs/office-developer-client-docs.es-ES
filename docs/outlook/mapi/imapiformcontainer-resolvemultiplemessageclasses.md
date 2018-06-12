---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817288"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Se aplica a**: Outlook 
  
Se resuelve un grupo de clases de mensajes en sus formularios en un contenedor de formulario y devuelve una matriz de formulario objetos de información para los formularios.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Sintaxis

 _pMsgClassArray_
  
> [entrada] Un puntero a una matriz que contiene los nombres de las clases de mensaje para resolver. Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se resuelven las clases de mensaje. Se puede establecer la marca siguiente:
    
MAPIFORM_EXACTMATCH 
  
> Se deben resolver sólo cadenas de clase de mensaje que son una coincidencia exacta.
    
 _ppfrminfoarray_
  
> [out] Un puntero a un puntero a una matriz de objetos de información del formulario. Si una aplicación cliente pasa NULL en el parámetro _pMsgClassArray_ , el parámetro _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios en el contenedor. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llaman al método **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver un grupo de clases de mensajes a los formularios dentro de un contenedor de formulario. La matriz de objetos de información de formulario devueltos en el parámetro _ppfrminfoarray_ aún más proporciona acceso a cada una de las propiedades de los formularios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver un grupo de clases de mensajes a los formularios, pase una matriz de nombres de clase de mensaje que se va a resolver. Para forzar la resolución para ser exactos (es decir, para evitar la resolución a una clase de la clase de mensaje base), el indicador MAPIFORM_EXACTMATCH se puede pasar en el parámetro _ulFlags_ . 
  
Si una clase de mensaje no se puede resolver a un formulario, se devuelve NULL para esa clase de mensaje en la matriz de información de formulario. Por lo tanto, incluso si el método devuelve S_OK, no se supone que se han resueltos correctamente todas las clases de mensaje. En su lugar, compruebe los valores en la matriz devuelta.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI usa el método **IMAPIFormContainer::ResolveMultipleMessageClasses** para buscar un formulario que está asociado a un conjunto de clases de mensajes.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

