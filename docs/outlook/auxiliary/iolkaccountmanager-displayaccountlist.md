---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Muestra el cuadro de diálogo Configuración de la cuenta o agregar una nueva cuenta.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415036"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Muestra el cuadro de diálogo Configuración de la **cuenta** o **Agregar una nueva cuenta** . 
  
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
  
> a Identificador de la ventana a la que es modal el cuadro de diálogo mostrado. Puede ser cero.
    
_dwFlags_
  
> a Marcas para modificar el comportamiento de la visualización. 
    
   - **ACCTUI_NO_WARNING**: no muestre la advertencia de que los cambios no tendrán efecto hasta que se reinicie Outlook. Solo se aplica si la aplicación se está ejecutando en proceso con Outlook. exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— muestra el cuadro de diálogo Configuración de la **cuenta** con la ficha **datos** seleccionada. Solo es válido si no se establece **ACCTUI_SHOW_ACCTWIZARD** . 
    
   - **ACCTUI_SHOW_ACCTWIZARD**: muestra el cuadro de diálogo **Agregar nueva cuenta** . 
    
_wszTitle_
  
> a Este parámetro no se usa y debe ser NULL.
    
_cCategories_
  
> a Este parámetro no se usa y debe ser NULL. 
    
_rgclsidCategories_
  
> a Este parámetro no se usa y debe ser NULL.
    
_pclsidType_
  
> a Este parámetro no se usa y debe ser NULL.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada se realizó correctamente.  <br/> |
|E_ACCT_UI_BUSY  <br/> |No se pudo crear el cuadro de diálogo.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |El cuadro de diálogo **Agregar nueva cuenta** devolvió un error.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |El parámetro _cCategories_, _rgclsidCategories_o _pclsidType_ no es NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |El cuadro de diálogo Configuración de la **cuenta** devolvió un error.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los parámetros _cCategories_, _rgclsidCategories_y _pclsidType_ no se usan en este momento y deben ser nulos.  _wszTitle_ no se usa y también debe ser null. 
  

