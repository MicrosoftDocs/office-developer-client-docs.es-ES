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
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="42fbf-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="42fbf-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="42fbf-104">Muestra el cuadro de diálogo de la **Configuración de la cuenta** o **Agregar una nueva cuenta** .</span><span class="sxs-lookup"><span data-stu-id="42fbf-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="42fbf-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="42fbf-105">Quick info</span></span>

<span data-ttu-id="42fbf-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="42fbf-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="42fbf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42fbf-107">Parameters</span></span>

<span data-ttu-id="42fbf-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="42fbf-108">_hwnd_</span></span>
  
> <span data-ttu-id="42fbf-109">[entrada] El identificador de la ventana a la que el cuadro de diálogo mostrado es modal.</span><span class="sxs-lookup"><span data-stu-id="42fbf-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="42fbf-110">Puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="42fbf-110">May be zero.</span></span>
    
<span data-ttu-id="42fbf-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="42fbf-111">_dwFlags_</span></span>
  
> <span data-ttu-id="42fbf-112">[entrada] Marcas para modificar el comportamiento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="42fbf-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="42fbf-113">**ACCTUI_NO_WARNING**: no mostrar la advertencia de que los cambios no tendrán efecto hasta que se reinicie Outlook.</span><span class="sxs-lookup"><span data-stu-id="42fbf-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="42fbf-114">Se aplica sólo si la aplicación se está ejecutando en proceso con Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="42fbf-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="42fbf-115">**ACCTUI_SHOW_DATA_TAB**: mostrar el cuadro de diálogo **Configuración de la cuenta** con la ficha de **datos** seleccionada.</span><span class="sxs-lookup"><span data-stu-id="42fbf-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="42fbf-116">Válido sólo si no se ha establecido **ACCTUI_SHOW_ACCTWIZARD** .</span><span class="sxs-lookup"><span data-stu-id="42fbf-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="42fbf-117">**ACCTUI_SHOW_ACCTWIZARD**: mostrar el cuadro de diálogo **Agregar una nueva cuenta** .</span><span class="sxs-lookup"><span data-stu-id="42fbf-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="42fbf-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="42fbf-118">_wszTitle_</span></span>
  
> <span data-ttu-id="42fbf-119">[entrada] Este parámetro no se utiliza y debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="42fbf-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="42fbf-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="42fbf-120">_cCategories_</span></span>
  
> <span data-ttu-id="42fbf-121">[entrada] Este parámetro no se utiliza y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="42fbf-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="42fbf-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="42fbf-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="42fbf-123">[entrada] Este parámetro no se utiliza y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="42fbf-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="42fbf-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="42fbf-124">_pclsidType_</span></span>
  
> <span data-ttu-id="42fbf-125">[entrada] Este parámetro no se utiliza y debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="42fbf-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="42fbf-126">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="42fbf-126">Return values</span></span>

|<span data-ttu-id="42fbf-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="42fbf-127">**HRESULT**</span></span>|<span data-ttu-id="42fbf-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="42fbf-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42fbf-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="42fbf-129">S_OK</span></span>  <br/> |<span data-ttu-id="42fbf-130">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="42fbf-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="42fbf-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="42fbf-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="42fbf-132">No se pudo crear el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42fbf-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="42fbf-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="42fbf-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="42fbf-134">No se ha inicializado el Administrador de cuentas para su uso.</span><span class="sxs-lookup"><span data-stu-id="42fbf-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="42fbf-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="42fbf-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="42fbf-136">El cuadro de diálogo **Agregar una nueva cuenta** devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="42fbf-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="42fbf-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="42fbf-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="42fbf-138">El parámetro _cCategories_, _rgclsidCategories_o _pclsidType_ no es NULL.</span><span class="sxs-lookup"><span data-stu-id="42fbf-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="42fbf-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="42fbf-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="42fbf-140">El cuadro de diálogo **Configuración de la cuenta** devolvió un error.</span><span class="sxs-lookup"><span data-stu-id="42fbf-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42fbf-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42fbf-141">Remarks</span></span>

<span data-ttu-id="42fbf-142">Los parámetros _cCategories_, _rgclsidCategories_y _pclsidType_ no se usan en este momento y deben ser NULL.</span><span class="sxs-lookup"><span data-stu-id="42fbf-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="42fbf-143">_wszTitle_ no se utiliza y también debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="42fbf-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

