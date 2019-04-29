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
# <a name="imapiformmgrselectform"></a><span data-ttu-id="9975d-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="9975d-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="9975d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9975d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9975d-105">Muestra un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe dicho formulario.</span><span class="sxs-lookup"><span data-stu-id="9975d-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="9975d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9975d-106">Parameters</span></span>

 <span data-ttu-id="9975d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9975d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="9975d-108">a Identificador de la ventana principal del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="9975d-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="9975d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9975d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9975d-110">a Una máscara de bits de marcadores que controla el tipo de las cadenas pasadas.</span><span class="sxs-lookup"><span data-stu-id="9975d-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="9975d-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="9975d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9975d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9975d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9975d-113">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9975d-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9975d-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9975d-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9975d-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="9975d-115">_pszTitle_</span></span>
  
> <span data-ttu-id="9975d-116">a Un puntero a una cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9975d-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="9975d-117">Si el parámetro _pszTitle_ es null, el proveedor de la biblioteca de formularios proporciona un título predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9975d-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="9975d-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="9975d-118">_pfld_</span></span>
  
> <span data-ttu-id="9975d-119">a Puntero a la carpeta desde la que se va a seleccionar el formulario.</span><span class="sxs-lookup"><span data-stu-id="9975d-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="9975d-120">Si el parámetro _pfld_ es null, el formulario puede seleccionarse desde el contenedor de formulario local, personal o de la organización.</span><span class="sxs-lookup"><span data-stu-id="9975d-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="9975d-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="9975d-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="9975d-122">contempla Un puntero a un puntero al objeto de información del formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="9975d-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9975d-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9975d-123">Return value</span></span>

<span data-ttu-id="9975d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="9975d-124">S_OK</span></span> 
  
> <span data-ttu-id="9975d-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="9975d-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9975d-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9975d-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9975d-127">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="9975d-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9975d-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9975d-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9975d-129">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9975d-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9975d-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9975d-130">Remarks</span></span>

<span data-ttu-id="9975d-131">Los visores de formularios llaman al método **IMAPIFormMgr:: SelectForm** para presentar primero un cuadro de diálogo que permite al usuario seleccionar un formulario y, a continuación, recuperar un objeto de información de formulario que describe el formulario seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9975d-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="9975d-132">El cuadro de diálogo restringe al usuario que seleccione un solo formulario.</span><span class="sxs-lookup"><span data-stu-id="9975d-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9975d-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9975d-133">Notes to callers</span></span>

<span data-ttu-id="9975d-134">El cuadro de diálogo **SelectForm** muestra sólo los formularios que no están ocultos (es decir, los formularios que tienen sus propiedades ocultas en blanco).</span><span class="sxs-lookup"><span data-stu-id="9975d-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="9975d-135">Si un visor de formularios pasa la marca MAPI_UNICODE en el parámetro _ulFlags_ , todas las cadenas son Unicode.</span><span class="sxs-lookup"><span data-stu-id="9975d-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="9975d-136">Los proveedores de bibliotecas de formularios que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9975d-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9975d-137">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9975d-137">MFCMAPI reference</span></span>

<span data-ttu-id="9975d-138">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9975d-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9975d-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="9975d-139">**File**</span></span>|<span data-ttu-id="9975d-140">**Función**</span><span class="sxs-lookup"><span data-stu-id="9975d-140">**Function**</span></span>|<span data-ttu-id="9975d-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9975d-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9975d-142">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="9975d-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="9975d-143">CFolderDlg:: OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="9975d-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="9975d-144">MFCMAPI usa el método **IMAPIFormMgr:: SelectForm** para seleccionar un formulario y enviar información sobre el formulario a uno o más registros.</span><span class="sxs-lookup"><span data-stu-id="9975d-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9975d-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="9975d-145">See also</span></span>



[<span data-ttu-id="9975d-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9975d-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="9975d-147">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="9975d-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

