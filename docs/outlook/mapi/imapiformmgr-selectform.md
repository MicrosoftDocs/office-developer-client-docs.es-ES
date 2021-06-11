---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423583"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="97938-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="97938-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="97938-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97938-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97938-105">Presenta un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe ese formulario.</span><span class="sxs-lookup"><span data-stu-id="97938-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="97938-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="97938-106">Parameters</span></span>

 <span data-ttu-id="97938-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="97938-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="97938-108">[in] Identificador de la ventana principal del cuadro de diálogo mostrado.</span><span class="sxs-lookup"><span data-stu-id="97938-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="97938-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="97938-109">_ulFlags_</span></span>
  
> <span data-ttu-id="97938-110">[in] Máscara de bits de marcas que controla el tipo de las cadenas pasadas.</span><span class="sxs-lookup"><span data-stu-id="97938-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="97938-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="97938-111">The following flag can be set:</span></span>
    
<span data-ttu-id="97938-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="97938-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="97938-113">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="97938-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="97938-114">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="97938-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="97938-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="97938-115">_pszTitle_</span></span>
  
> <span data-ttu-id="97938-116">[in] Puntero a una cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="97938-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="97938-117">Si el  _parámetro pszTitle_ es NULL, el proveedor de biblioteca de formularios proporciona un título predeterminado.</span><span class="sxs-lookup"><span data-stu-id="97938-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="97938-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="97938-118">_pfld_</span></span>
  
> <span data-ttu-id="97938-119">[in] Puntero a la carpeta desde la que se va a seleccionar el formulario.</span><span class="sxs-lookup"><span data-stu-id="97938-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="97938-120">Si el  _parámetro pfld_ es NULL, el formulario se puede seleccionar desde el contenedor del formulario local, personal u organización.</span><span class="sxs-lookup"><span data-stu-id="97938-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="97938-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="97938-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="97938-122">[salida] Puntero a un puntero al objeto de información del formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="97938-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="97938-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97938-123">Return value</span></span>

<span data-ttu-id="97938-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="97938-124">S_OK</span></span> 
  
> <span data-ttu-id="97938-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="97938-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="97938-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="97938-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="97938-127">La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="97938-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="97938-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="97938-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="97938-129">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="97938-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="97938-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97938-130">Remarks</span></span>

<span data-ttu-id="97938-131">Los visores de formularios llaman al método **IMAPIFormMgr::SelectForm** para presentar primero un cuadro de diálogo que permita al usuario seleccionar un formulario y, a continuación, recuperar un objeto de información de formulario que describa el formulario seleccionado.</span><span class="sxs-lookup"><span data-stu-id="97938-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="97938-132">El cuadro de diálogo limita al usuario a seleccionar un solo formulario.</span><span class="sxs-lookup"><span data-stu-id="97938-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="97938-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="97938-133">Notes to callers</span></span>

<span data-ttu-id="97938-134">El **cuadro de diálogo Seleccionarformulario** muestra solo formularios que no están ocultos (es decir, formularios que tienen sus propiedades ocultas borradas).</span><span class="sxs-lookup"><span data-stu-id="97938-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="97938-135">Si un visor de formulario pasa la marca MAPI_UNICODE en el  _parámetro ulFlags,_ todas las cadenas son Unicode.</span><span class="sxs-lookup"><span data-stu-id="97938-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="97938-136">Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE se pasa.</span><span class="sxs-lookup"><span data-stu-id="97938-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="97938-137">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="97938-137">MFCMAPI reference</span></span>

<span data-ttu-id="97938-138">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="97938-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="97938-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="97938-139">**File**</span></span>|<span data-ttu-id="97938-140">**Función**</span><span class="sxs-lookup"><span data-stu-id="97938-140">**Function**</span></span>|<span data-ttu-id="97938-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="97938-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="97938-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="97938-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="97938-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="97938-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="97938-144">MFCMAPI usa el **método IMAPIFormMgr::SelectForm** para seleccionar un formulario y enviar información sobre el formulario a uno o varios registros.</span><span class="sxs-lookup"><span data-stu-id="97938-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97938-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="97938-145">See also</span></span>



[<span data-ttu-id="97938-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97938-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="97938-147">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="97938-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

