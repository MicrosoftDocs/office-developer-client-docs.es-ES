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
ms.openlocfilehash: 3c6242c9a926341908cb86645a8ea8586a9ca598
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586357"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="de7bd-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="de7bd-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="de7bd-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de7bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de7bd-105">Presenta un cuadro de diálogo que permite al usuario seleccionar un formulario y devuelve un objeto de información de formulario que describe ese formulario.</span><span class="sxs-lookup"><span data-stu-id="de7bd-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="de7bd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de7bd-106">Parameters</span></span>

 <span data-ttu-id="de7bd-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="de7bd-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="de7bd-108">[entrada] Identificador de la ventana principal del cuadro de diálogo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="de7bd-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="de7bd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de7bd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="de7bd-110">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas que se pasan en.</span><span class="sxs-lookup"><span data-stu-id="de7bd-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="de7bd-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="de7bd-111">The following flag can be set:</span></span>
    
<span data-ttu-id="de7bd-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="de7bd-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="de7bd-113">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="de7bd-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="de7bd-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="de7bd-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="de7bd-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="de7bd-115">_pszTitle_</span></span>
  
> <span data-ttu-id="de7bd-116">[entrada] Un puntero a una cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="de7bd-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="de7bd-117">Si el parámetro _pszTitle_ es NULL, el proveedor de la biblioteca de formularios proporciona un título predeterminado.</span><span class="sxs-lookup"><span data-stu-id="de7bd-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="de7bd-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="de7bd-118">_pfld_</span></span>
  
> <span data-ttu-id="de7bd-119">[entrada] Un puntero a la carpeta desde la que se va a seleccionar el formulario.</span><span class="sxs-lookup"><span data-stu-id="de7bd-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="de7bd-120">Si el parámetro _pfld_ es NULL, se puede seleccionar el formulario desde el contenedor de forma local, el personal o la organización.</span><span class="sxs-lookup"><span data-stu-id="de7bd-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="de7bd-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="de7bd-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="de7bd-122">[out] Un puntero a un puntero al objeto de información de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="de7bd-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de7bd-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de7bd-123">Return value</span></span>

<span data-ttu-id="de7bd-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="de7bd-124">S_OK</span></span> 
  
> <span data-ttu-id="de7bd-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="de7bd-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="de7bd-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="de7bd-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="de7bd-127">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="de7bd-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="de7bd-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="de7bd-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="de7bd-129">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="de7bd-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de7bd-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de7bd-130">Remarks</span></span>

<span data-ttu-id="de7bd-131">Visores de formulario llamar al método **IMAPIFormMgr::SelectForm** a presenta primero un cuadro de diálogo que permite al usuario seleccionar un formulario y, a continuación, para recuperar un objeto de información de formulario que describe el formulario seleccionado.</span><span class="sxs-lookup"><span data-stu-id="de7bd-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="de7bd-132">El cuadro de diálogo restringe el usuario para seleccionar un único formulario.</span><span class="sxs-lookup"><span data-stu-id="de7bd-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="de7bd-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="de7bd-133">Notes to callers</span></span>

<span data-ttu-id="de7bd-134">El cuadro de diálogo **SelectForm** muestra sólo los formularios que no están ocultos (es decir, desactive los formularios que tienen sus propiedades ocultos).</span><span class="sxs-lookup"><span data-stu-id="de7bd-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="de7bd-135">Si un visor de formulario, pasa el indicador MAPI_UNICODE el parámetro _ulFlags_ , todas las cadenas son cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="de7bd-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="de7bd-136">Proveedores de biblioteca de formulario que no admiten cadenas Unicode deben devolver MAPI_E_BAD_CHARWIDTH si se pasa MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="de7bd-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="de7bd-137">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="de7bd-137">MFCMAPI reference</span></span>

<span data-ttu-id="de7bd-138">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="de7bd-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="de7bd-139">**File**</span><span class="sxs-lookup"><span data-stu-id="de7bd-139">**File**</span></span>|<span data-ttu-id="de7bd-140">**Función**</span><span class="sxs-lookup"><span data-stu-id="de7bd-140">**Function**</span></span>|<span data-ttu-id="de7bd-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="de7bd-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de7bd-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="de7bd-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="de7bd-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="de7bd-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="de7bd-144">MFCMAPI usa el método **IMAPIFormMgr::SelectForm** para seleccionar un formulario y enviar información sobre el formulario a uno o más registros.</span><span class="sxs-lookup"><span data-stu-id="de7bd-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de7bd-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="de7bd-145">See also</span></span>



[<span data-ttu-id="de7bd-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de7bd-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="de7bd-147">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="de7bd-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

