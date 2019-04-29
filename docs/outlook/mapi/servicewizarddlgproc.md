---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432383"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="c565d-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="c565d-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="c565d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c565d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c565d-105">Define una función de devolución de llamada invocada por el Asistente para perfiles para permitir a un proveedor de servicios reaccionar a los eventos de usuario cuando se muestran las páginas o las hojas de propiedades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c565d-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c565d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c565d-106">Header file:</span></span>  <br/> |<span data-ttu-id="c565d-107">Mapiwz. h</span><span class="sxs-lookup"><span data-stu-id="c565d-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="c565d-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="c565d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c565d-109">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c565d-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="c565d-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="c565d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c565d-111">Asistente para perfiles MAPI</span><span class="sxs-lookup"><span data-stu-id="c565d-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="c565d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="c565d-112">Parameters</span></span>

<span data-ttu-id="c565d-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="c565d-113">_hDlg_</span></span>
  
> <span data-ttu-id="c565d-114">a Identificador de ventana para el cuadro de diálogo Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="c565d-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="c565d-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="c565d-115">_wMsgID_</span></span>
  
> <span data-ttu-id="c565d-116">a Mensaje de ventana que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="c565d-116">[in] The window message to be processed.</span></span> <span data-ttu-id="c565d-117">Además de los mensajes de ventana normales que espera un cuadro de diálogo modal, se pueden recibir los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="c565d-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="c565d-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="c565d-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="c565d-119">El Asistente de perfil se ha completado.</span><span class="sxs-lookup"><span data-stu-id="c565d-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="c565d-120">El proveedor de servicios debe realizar todas las tareas de limpieza necesarias, como cancelar la asignación de memoria asignada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="c565d-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="c565d-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="c565d-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="c565d-122">Se ha seleccionado uno de los controles del proveedor o se ha hace clic en el botón **siguiente** o **atrás** .</span><span class="sxs-lookup"><span data-stu-id="c565d-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="c565d-123">El valor del parámetro _wParam_ indica cuál de estos eventos de usuario se ha producido.</span><span class="sxs-lookup"><span data-stu-id="c565d-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="c565d-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="c565d-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="c565d-125">El usuario se ha movido a otra página de propiedades, para la que debe inicializarse el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c565d-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="c565d-126">El proveedor debe inicializar los controles que el Asistente para perfiles haya agregado al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c565d-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="c565d-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="c565d-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="c565d-128">El Asistente para perfiles solicita el número de páginas que el proveedor tiene que mostrar.</span><span class="sxs-lookup"><span data-stu-id="c565d-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="c565d-129">El proveedor debe devolver el número de páginas en lugar de verdadero o falso.</span><span class="sxs-lookup"><span data-stu-id="c565d-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="c565d-130">Por ejemplo, use la siguiente instrucción return para indicar que deben mostrarse tres páginas:</span><span class="sxs-lookup"><span data-stu-id="c565d-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="c565d-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="c565d-131">_wParam_</span></span>
  
> <span data-ttu-id="c565d-132">a Un parámetro de 32 bits asociado con los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="c565d-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="c565d-133">Los valores posibles dependen del mensaje especificado en el parámetro _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="c565d-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="c565d-134">Además de los valores que se esperan con los mensajes de ventana normales para un cuadro de diálogo modal, se pueden recibir los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c565d-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="c565d-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="c565d-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="c565d-136">Cuando _wMsgID_ contiene WM_COMMAND, el usuario hizo clic en el botón **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="c565d-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="c565d-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="c565d-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="c565d-138">Cuando _wMsgID_ contiene WM_COMMAND, el usuario ha realizado clic en el botón **atrás** .</span><span class="sxs-lookup"><span data-stu-id="c565d-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="c565d-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="c565d-139">_lParam_</span></span>
  
> <span data-ttu-id="c565d-140">a Un parámetro de 32 bits asociado con los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="c565d-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="c565d-141">Los valores posibles dependen del mensaje especificado en el parámetro _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="c565d-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c565d-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c565d-142">Return value</span></span>

<span data-ttu-id="c565d-143">El valor devuelto por una función basada en **SERVICEWIZARDDLGPROC** depende del mensaje de ventana recibido.</span><span class="sxs-lookup"><span data-stu-id="c565d-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="c565d-144">Tenga en cuenta en concreto el valor devuelto excepcional para el mensaje WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="c565d-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="c565d-145">Los valores normales devueltos son:</span><span class="sxs-lookup"><span data-stu-id="c565d-145">The normal return values are:</span></span> 
  
<span data-ttu-id="c565d-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="c565d-146">TRUE</span></span> 
  
> <span data-ttu-id="c565d-147">El proveedor de servicios ha procesado el mensaje de ventana recibido.</span><span class="sxs-lookup"><span data-stu-id="c565d-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="c565d-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="c565d-148">FALSE</span></span> 
  
> <span data-ttu-id="c565d-149">El proveedor de servicios no ha procesado el mensaje de ventana recibido.</span><span class="sxs-lookup"><span data-stu-id="c565d-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c565d-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c565d-150">Remarks</span></span>

<span data-ttu-id="c565d-151">Cuando el usuario se mueve de una página de propiedades a otra, el proveedor es responsable de ocultar los controles de la página antigua y de mostrar los controles de la página siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="c565d-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="c565d-152">Cuando el usuario hace clic en el botón **siguiente** , se llama a la función basada en **SERVICEWIZARDDLGPROC** con el mensaje WM_COMMAND y WIZ_NEXT en el parámetro _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="c565d-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="c565d-153">Los pasos siguientes describen lo que ocurre entre el momento en que el usuario hace clic en **siguiente** y la hora en que se representan las páginas de configuración del primer proveedor.</span><span class="sxs-lookup"><span data-stu-id="c565d-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="c565d-154">El Asistente para perfiles oculta los controles que se encuentran en la ventana.</span><span class="sxs-lookup"><span data-stu-id="c565d-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="c565d-155">El Asistente para perfiles agrega los controles ocultos del proveedor a la página.</span><span class="sxs-lookup"><span data-stu-id="c565d-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="c565d-156">El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviando el mensaje WM_INITDIALOG, para que el proveedor pueda inicializar los controles.</span><span class="sxs-lookup"><span data-stu-id="c565d-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="c565d-157">El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviando el mensaje WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="c565d-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="c565d-158">El proveedor devuelve el número de páginas que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="c565d-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="c565d-159">El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviando el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="c565d-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="c565d-160">En este punto, el proveedor devuelve FALSE {error} o revela sus controles y devuelve TRUE {Success}.</span><span class="sxs-lookup"><span data-stu-id="c565d-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="c565d-161">Si el Asistente para perfiles pasa en ID_NEXT, se muestra la primera página del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c565d-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="c565d-162">Si se pasa ID_PREV, se muestra la última página.</span><span class="sxs-lookup"><span data-stu-id="c565d-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="c565d-163">El Asistente para perfiles llama a la función **SERVICEWIZARDDLGPROC** del proveedor, enviando el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV (según el botón en el que el usuario hizo clic).</span><span class="sxs-lookup"><span data-stu-id="c565d-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="c565d-164">El proveedor es responsable de mostrar u ocultar sus controles y escribir sus datos en el **IMAPIProp** que se pasa al Asistente para perfiles para recorrer su secuencia de páginas.</span><span class="sxs-lookup"><span data-stu-id="c565d-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="c565d-165">El proveedor debe devolver TRUE si se ha mostrado correctamente la página siguiente o anterior, y FALSE si no se puede mostrar la página siguiente ni la anterior.</span><span class="sxs-lookup"><span data-stu-id="c565d-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="c565d-166">El proveedor debe estar al tanto de la versión fuera de su secuencia de páginas y responder de manera adecuada ocultando sus controles y escribiendo sus datos en el perfil.</span><span class="sxs-lookup"><span data-stu-id="c565d-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="c565d-167">Si los pasos del usuario se encuentran fuera del intervalo de páginas del proveedor, el Asistente para perfiles elimina los controles ocultos del proveedor del cuadro de diálogo y llama al siguiente proveedor o muestra la página siguiente si ese era el último proveedor.</span><span class="sxs-lookup"><span data-stu-id="c565d-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

