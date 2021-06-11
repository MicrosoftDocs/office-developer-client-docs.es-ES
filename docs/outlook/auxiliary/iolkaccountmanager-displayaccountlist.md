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
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="c52c2-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="c52c2-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="c52c2-104">Muestra el cuadro **de diálogo Configuración** cuenta o Agregar **nueva** cuenta.</span><span class="sxs-lookup"><span data-stu-id="c52c2-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c52c2-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="c52c2-105">Quick info</span></span>

<span data-ttu-id="c52c2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="c52c2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="c52c2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="c52c2-107">Parameters</span></span>

<span data-ttu-id="c52c2-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="c52c2-108">_hwnd_</span></span>
  
> <span data-ttu-id="c52c2-109">[in] El identificador de la ventana en la que se muestra el cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="c52c2-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="c52c2-110">Puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="c52c2-110">May be zero.</span></span>
    
<span data-ttu-id="c52c2-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="c52c2-111">_dwFlags_</span></span>
  
> <span data-ttu-id="c52c2-112">[in] Marcas para modificar el comportamiento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="c52c2-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="c52c2-113">**ACCTUI_NO_WARNING:** no muestre la advertencia de que los cambios no tendrán efecto hasta que Outlook se reinicie.</span><span class="sxs-lookup"><span data-stu-id="c52c2-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="c52c2-114">Solo se aplica si la aplicación se ejecuta en proceso con Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="c52c2-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="c52c2-115">**ACCTUI_SHOW_DATA_TAB:** mostrar el **cuadro de diálogo Configuración** cuenta con la **pestaña** Datos seleccionada.</span><span class="sxs-lookup"><span data-stu-id="c52c2-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="c52c2-116">Solo es válido **si ACCTUI_SHOW_ACCTWIZARD** no está establecido.</span><span class="sxs-lookup"><span data-stu-id="c52c2-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="c52c2-117">**ACCTUI_SHOW_ACCTWIZARD:** muestra el **cuadro de diálogo** Agregar nueva cuenta.</span><span class="sxs-lookup"><span data-stu-id="c52c2-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="c52c2-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="c52c2-118">_wszTitle_</span></span>
  
> <span data-ttu-id="c52c2-119">[in] Este parámetro no se usa y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="c52c2-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="c52c2-120">_cCategories_</span></span>
  
> <span data-ttu-id="c52c2-121">[in] Este parámetro no se usa y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="c52c2-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="c52c2-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="c52c2-123">[in] Este parámetro no se usa y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="c52c2-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="c52c2-124">_pclsidType_</span></span>
  
> <span data-ttu-id="c52c2-125">[in] Este parámetro no se usa y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c52c2-126">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c52c2-126">Return values</span></span>

|<span data-ttu-id="c52c2-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="c52c2-127">**HRESULT**</span></span>|<span data-ttu-id="c52c2-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="c52c2-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c52c2-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="c52c2-129">S_OK</span></span>  <br/> |<span data-ttu-id="c52c2-130">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c52c2-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="c52c2-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="c52c2-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="c52c2-132">No se pudo crear el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c52c2-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="c52c2-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c52c2-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c52c2-134">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="c52c2-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="c52c2-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c52c2-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="c52c2-136">El **cuadro de diálogo Agregar nueva** cuenta devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="c52c2-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="c52c2-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c52c2-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="c52c2-138">El  _parámetro cCategories_,  _rgclsidCategories_ o  _pclsidType_ no es NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="c52c2-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c52c2-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="c52c2-140">El **cuadro de Configuración** de diálogo Cuenta devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="c52c2-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c52c2-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c52c2-141">Remarks</span></span>

<span data-ttu-id="c52c2-142">Los  _parámetros cCategories_,  _rgclsidCategories_ y  _pclsidType_ no se usan en este momento y deben ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="c52c2-143">_wszTitle_ no se usa y también debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c52c2-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

