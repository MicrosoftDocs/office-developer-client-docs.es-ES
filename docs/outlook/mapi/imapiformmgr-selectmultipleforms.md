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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420314"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Presenta un cuadro de diálogo que permite al usuario seleccionar varios formularios y devuelve una matriz de objetos de información de formulario que describen dichos formularios.
  
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
  
> [in] Identificador de la ventana principal del cuadro de diálogo mostrado. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla el tipo de las cadenas pasadas. Se puede establecer la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
 _pszTitle_
  
> [in] Puntero a una cadena que contiene el título del cuadro de diálogo. Si el  _parámetro pszTitle_ es NULL, el proveedor de biblioteca de formularios que proporciona los formularios proporciona un título predeterminado. 
    
 _pfld_
  
> [in] Puntero a la carpeta desde la que se seleccionan los formularios. Si el  _parámetro pfld_ es NULL, los formularios se seleccionan desde el contenedor de formularios local, personal u organización. 
    
 _pfrminfoarray_
  
> [in] Puntero a una matriz de objetos de información de formulario que están preseleccionados para el usuario.
    
 _ppfrminfoarray_
  
> [salida] Puntero a un puntero a la matriz devuelta de objetos de información de formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realiza correctamente y devuelve el valor o los valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** del cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormMgr::SelectMultipleForms** para presentar primero un cuadro de diálogo que permite al usuario seleccionar varios formularios y, a continuación, recuperar una matriz de objetos de información de formulario que describen los formularios seleccionados. El **cuadro de diálogo SelectMultipleForms** muestra todos los formularios, independientemente de si están ocultos (es decir, si sus propiedades ocultas están o no claras). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si un visor de formulario pasa la marca MAPI_UNICODE en el  _parámetro ulFlags,_ todas las cadenas son Unicode. Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa. 
  
## <a name="see-also"></a>Vea también



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

