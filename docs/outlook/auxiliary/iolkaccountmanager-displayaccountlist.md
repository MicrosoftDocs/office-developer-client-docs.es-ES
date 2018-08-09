---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Muestra el cuadro de diálogo de la configuración de la cuenta o agregar una nueva cuenta.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816229"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Muestra el cuadro de diálogo de la **Configuración de la cuenta** o **Agregar una nueva cuenta** . 
  
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

## <a name="parameters"></a>Parámetros

_hwnd_
  
> [entrada] El identificador de la ventana a la que el cuadro de diálogo mostrado es modal. Puede ser cero.
    
_dwFlags_
  
> [entrada] Marcas para modificar el comportamiento de la presentación. 
    
   - **ACCTUI_NO_WARNING**: no mostrar la advertencia de que los cambios no tendrán efecto hasta que se reinicie Outlook. Se aplica sólo si la aplicación se está ejecutando en proceso con Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**: mostrar el cuadro de diálogo **Configuración de la cuenta** con la ficha de **datos** seleccionada. Válido sólo si no se ha establecido **ACCTUI_SHOW_ACCTWIZARD** . 
    
   - **ACCTUI_SHOW_ACCTWIZARD**: mostrar el cuadro de diálogo **Agregar una nueva cuenta** . 
    
_wszTitle_
  
> [entrada] Este parámetro no se utiliza y debe ser nulo.
    
_cCategories_
  
> [entrada] Este parámetro no se utiliza y debe ser NULL. 
    
_rgclsidCategories_
  
> [entrada] Este parámetro no se utiliza y debe ser NULL.
    
_pclsidType_
  
> [entrada] Este parámetro no se utiliza y debe ser NULL.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada tuvo éxito.  <br/> |
|E_ACCT_UI_BUSY  <br/> |No se pudo crear el cuadro de diálogo.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |El cuadro de diálogo **Agregar una nueva cuenta** devolvió un error.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |El parámetro _cCategories_, _rgclsidCategories_o _pclsidType_ no es NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |El cuadro de diálogo **Configuración de la cuenta** devolvió un error.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los parámetros _cCategories_, _rgclsidCategories_y _pclsidType_ no se usan en este momento y deben ser NULL.  _wszTitle_ no se utiliza y también debe ser nulo. 
  

