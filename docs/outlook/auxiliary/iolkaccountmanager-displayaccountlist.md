---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Muestra el cuadro de diálogo Configuración cuenta o Agregar nueva cuenta.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415036"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Muestra el cuadro **de diálogo Configuración** cuenta o Agregar **nueva** cuenta. 
  
## <a name="quick-info"></a>Información rápida

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>Parameters

_hwnd_
  
> [in] El identificador de la ventana en la que se muestra el cuadro de diálogo modal. Puede ser cero.
    
_dwFlags_
  
> [in] Marcas para modificar el comportamiento de la presentación. 
    
   - **ACCTUI_NO_WARNING:** no muestre la advertencia de que los cambios no tendrán efecto hasta que Outlook se reinicie. Solo se aplica si la aplicación se ejecuta en proceso con Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB:** mostrar el **cuadro de diálogo Configuración** cuenta con la **pestaña** Datos seleccionada. Solo es válido **si ACCTUI_SHOW_ACCTWIZARD** no está establecido. 
    
   - **ACCTUI_SHOW_ACCTWIZARD:** muestra el **cuadro de diálogo** Agregar nueva cuenta. 
    
_wszTitle_
  
> [in] Este parámetro no se usa y debe ser NULL.
    
_cCategories_
  
> [in] Este parámetro no se usa y debe ser NULL. 
    
_rgclsidCategories_
  
> [in] Este parámetro no se usa y debe ser NULL.
    
_pclsidType_
  
> [in] Este parámetro no se usa y debe ser NULL.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada se ha realizado correctamente.  <br/> |
|E_ACCT_UI_BUSY  <br/> |No se pudo crear el cuadro de diálogo.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |El **cuadro de diálogo Agregar nueva** cuenta devolvió un error.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |El  _parámetro cCategories_,  _rgclsidCategories_ o  _pclsidType_ no es NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |El **cuadro de Configuración** de diálogo Cuenta devuelve un error.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los  _parámetros cCategories_,  _rgclsidCategories_ y  _pclsidType_ no se usan en este momento y deben ser NULL.  _wszTitle_ no se usa y también debe ser NULL. 
  

