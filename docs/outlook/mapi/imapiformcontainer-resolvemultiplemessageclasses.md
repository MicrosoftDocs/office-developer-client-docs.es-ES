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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412544"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Resuelve un grupo de clases de mensajes en sus formularios en un contenedor de formularios y devuelve una matriz de objetos de información de formulario para esos formularios.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parámetros

 _pMsgClassArray_
  
> [entrada] Puntero a una matriz que contiene los nombres de las clases de mensaje que se resolverán. Los nombres de clase de mensaje son siempre cadenas ANSI, nunca Unicode.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se resuelven las clases de mensaje. Se puede establecer la siguiente marca:
    
MAPIFORM_EXACTMATCH 
  
> Solo deben resolverse las cadenas de clase de mensaje que sean una coincidencia exacta.
    
 _ppfrminfoarray_
  
> [salida] Puntero a un puntero a una matriz de objetos de información de formulario. Si una aplicación cliente pasa NULL en el parámetro  _pMsgClassArray,_ el parámetro  _ppfrminfoarray_ contiene objetos de información de formulario para todos los formularios del contenedor. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman al método **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver un grupo de clases de mensajes en formularios dentro de un contenedor de formularios. La matriz de objetos de información de formulario devueltos en el  _parámetro ppfrminfoarray_ proporciona acceso adicional a cada una de las propiedades de los formularios. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para resolver un grupo de clases de mensajes en formularios, pase una matriz de nombres de clase de mensaje que se resolverán. Para forzar que la resolución sea exacta (es decir, para evitar la resolución a una clase base de la clase de mensaje), la marca MAPIFORM_EXACTMATCH puede pasarse en el _parámetro ulFlags._ 
  
Si una clase de mensaje no se puede resolver en un formulario, se devuelve NULL para esa clase de mensaje en la matriz de información del formulario. Por lo tanto, incluso si el método devuelve S_OK, no suponga que todas las clases de mensajes se han resuelto correctamente. En su lugar, compruebe los valores de la matriz devuelta.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI usa el **método IMAPIFormContainer::ResolveMultipleMessageClasses** para buscar un formulario asociado a un conjunto de clases de mensaje.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

