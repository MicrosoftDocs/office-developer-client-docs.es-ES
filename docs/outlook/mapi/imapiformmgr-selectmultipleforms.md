---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321598"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de objetos de información de formulario que describen esos formularios.
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana principal del cuadro de diálogo que se muestra. 
    
 _ulFlags_
  
> a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.
    
 _pszTitle_
  
> a Un puntero a una cadena que contiene el título del cuadro de diálogo. Si el parámetro _pszTitle_ es null, el proveedor de la biblioteca de formularios que proporciona los formularios proporciona un título predeterminado. 
    
 _pfld_
  
> a Puntero a la carpeta desde la que se van a seleccionar los formularios. Si el parámetro _pfld_ es null, los formularios se seleccionan desde el contenedor de formulario local, personal o de la organización. 
    
 _pfrminfoarray_
  
> a Un puntero a una matriz de objetos de información de formulario que están preseleccionadas para el usuario.
    
 _ppfrminfoarray_
  
> contempla Un puntero a un puntero a la matriz devuelta de objetos de información de formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr:: SelectMultipleForms** para presentar primero un cuadro de diálogo que permite al usuario seleccionar varios formularios y, a continuación, recuperar una matriz de objetos de información de formulario que describen los formularios seleccionados. El cuadro de diálogo **SelectMultipleForms** muestra todos los formularios, estén o no ocultos (es decir, si sus propiedades ocultas están claras o no). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si un visor de formularios pasa la marca MAPI_UNICODE en el parámetro _ulFlags_ , todas las cadenas son Unicode. Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE. 
  
## <a name="see-also"></a>Vea también



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

