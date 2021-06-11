---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405089"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="8ccfc-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="8ccfc-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="8ccfc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ccfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ccfc-105">Instala un formulario en una biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="8ccfc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8ccfc-106">Parameters</span></span>

 <span data-ttu-id="8ccfc-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8ccfc-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8ccfc-108">[in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="8ccfc-109">El _parámetro ulUIParam_ se omite a menos que la aplicación cliente MAPI_DIALOG marca en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8ccfc-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8ccfc-110">El  _parámetro ulUIParam_ puede ser NULL si MAPI_DIALOG no se pasa.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="8ccfc-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8ccfc-111">_ulFlags_</span></span>
  
> <span data-ttu-id="8ccfc-112">[in] Máscara de bits de marcas que controla la instalación del formulario.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="8ccfc-113">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="8ccfc-113">The following flags can be set:</span></span>
    
<span data-ttu-id="8ccfc-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8ccfc-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8ccfc-115">Muestra un cuadro de diálogo para proporcionar información de progreso o solicitar al usuario más información.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="8ccfc-116">Si no se establece esta marca, no se muestra ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="8ccfc-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8ccfc-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8ccfc-118">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8ccfc-119">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="8ccfc-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="8ccfc-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="8ccfc-121">Si ya existe otro formulario que controla la clase de mensaje que controla este formulario, reemplace el formulario existente por este.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="8ccfc-122">Esta marca se omite si la MAPI_DIALOG también está presente.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="8ccfc-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="8ccfc-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="8ccfc-124">[in] Ruta de acceso al archivo de configuración del formulario.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ccfc-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ccfc-125">Return value</span></span>

<span data-ttu-id="8ccfc-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ccfc-126">S_OK</span></span> 
  
> <span data-ttu-id="8ccfc-127">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8ccfc-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="8ccfc-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="8ccfc-129">Se ha producido un error de implementación.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-129">An implementation error occurred.</span></span> <span data-ttu-id="8ccfc-130">Para obtener la [estructura MAPIERROR](mapierror.md) asociada al error, llame al método [IMAPIFormContainer::GetLastError.](imapiformcontainer-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="8ccfc-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="8ccfc-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="8ccfc-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="8ccfc-132">El usuario canceló la instalación del formulario, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="8ccfc-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8ccfc-133">Notes to implementers</span></span>

<span data-ttu-id="8ccfc-134">Los proveedores de bibliotecas de formularios deben rellenar una estructura **MAPIERROR** y devolver MAPI_E_EXTENDED_ERROR si se produce alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="8ccfc-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="8ccfc-135">No se encuentra el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="8ccfc-136">El archivo de configuración no es legible.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="8ccfc-137">El archivo de configuración no es válido.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="8ccfc-138">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8ccfc-138">Notes to callers</span></span>

<span data-ttu-id="8ccfc-139">Las aplicaciones cliente llaman **al método IMAPIFormContainer::InstallForm** para instalar un formulario en un contenedor de formulario específico.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="8ccfc-140">El  _parámetro szCfgPathName_ debe contener la ruta de acceso de un archivo de configuración de formulario (es decir, un archivo con la extensión .cfg que describe el formulario y su implementación).</span><span class="sxs-lookup"><span data-stu-id="8ccfc-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="8ccfc-141">Las marcas del parámetro  _ulFlags_ especifican lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8ccfc-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="8ccfc-142">Si se MAPI_DIALOG marca, se muestra una interfaz de usuario, lo que permite al usuario que está instalando el formulario especificar detalles de instalación.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="8ccfc-143">Si se MAPIFORM_INSTALL_OVERWRITEONCONFLICT marca, cualquier formulario anterior para la misma clase de mensaje se reemplaza por el formulario que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="8ccfc-144">De lo contrario, la instalación del formulario se combina con la descripción del formulario actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="8ccfc-145">Si MAPI_DIALOG se establece, MAPIFORM_INSTALL_OVERWRITEONCONFLICT se omite.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="8ccfc-146">La ausencia de MAPIFORM_INSTALL_OVERWRITEONCONFLICT en el conjunto de marcas significa que se realizará una combinación.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="8ccfc-147">Se instalarán todas las plataformas nuevas del archivo .cfg que no estén presentes actualmente en la descripción del formulario y no se producirán otros cambios.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="8ccfc-148">Si se MAPI_UNICODE marca, la ruta de acceso del archivo de configuración del formulario es una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="8ccfc-149">Los clientes deben llamar a [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** devuelve MAPI_E_EXTENDED_ERROR y deben comprobar la estructura [MAPIERROR](mapierror.md) devuelta para determinar la condición que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8ccfc-150">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8ccfc-150">MFCMAPI reference</span></span>

<span data-ttu-id="8ccfc-151">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8ccfc-152">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8ccfc-152">**File**</span></span>|<span data-ttu-id="8ccfc-153">**Función**</span><span class="sxs-lookup"><span data-stu-id="8ccfc-153">**Function**</span></span>|<span data-ttu-id="8ccfc-154">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="8ccfc-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8ccfc-155">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8ccfc-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="8ccfc-156">CFormContainerDlg::OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="8ccfc-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="8ccfc-157">MFCMAPI usa el **método IMAPIFormContainer::InstallForm** para instalar un formulario en un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ccfc-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ccfc-158">See also</span></span>



[<span data-ttu-id="8ccfc-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8ccfc-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8ccfc-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ccfc-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="8ccfc-161">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="8ccfc-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

