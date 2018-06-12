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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 649046aa48f293caa5bd71cc670481b5c205459a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820645"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="41d85-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="41d85-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="41d85-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41d85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41d85-105">Define una función de devolución de llamada invocada por el Asistente para perfiles para permitir que un proveedor de servicios reaccionar a los eventos de usuario cuando se va a mostrar páginas o las hojas de propiedades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="41d85-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41d85-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="41d85-106">Header file:</span></span>  <br/> |<span data-ttu-id="41d85-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="41d85-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="41d85-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="41d85-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="41d85-109">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="41d85-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="41d85-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="41d85-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="41d85-111">Asistente para el perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="41d85-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="41d85-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41d85-112">Parameters</span></span>

<span data-ttu-id="41d85-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="41d85-113">_hDlg_</span></span>
  
> <span data-ttu-id="41d85-114">[entrada] Identificador de ventana para el cuadro de diálogo Asistente para el perfil.</span><span class="sxs-lookup"><span data-stu-id="41d85-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="41d85-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="41d85-115">_wMsgID_</span></span>
  
> <span data-ttu-id="41d85-116">[entrada] El mensaje de ventana que va a procesar.</span><span class="sxs-lookup"><span data-stu-id="41d85-116">[in] The window message to be processed.</span></span> <span data-ttu-id="41d85-117">Además de los mensajes de ventana regular esperados por un cuadro de diálogo modal, se pueden recibir los mensajes siguientes:</span><span class="sxs-lookup"><span data-stu-id="41d85-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="41d85-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="41d85-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="41d85-119">Ha completado el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="41d85-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="41d85-120">El proveedor de servicios debe hacer todos los limpieza necesaria, como cancelar la asignación de alguna dinámicamente asignados a la memoria.</span><span class="sxs-lookup"><span data-stu-id="41d85-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="41d85-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="41d85-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="41d85-122">Se ha seleccionado uno de los controles del proveedor, o ha hecho clic en el botón **siguiente** o **Atrás** .</span><span class="sxs-lookup"><span data-stu-id="41d85-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="41d85-123">El valor en el parámetro _wParam_ indica cuál de estos eventos de usuario se ha producido.</span><span class="sxs-lookup"><span data-stu-id="41d85-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="41d85-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="41d85-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="41d85-125">El usuario ha movido a otra página de propiedades, para el que se debe inicializar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41d85-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="41d85-126">El proveedor debe inicializar los controles que ha agregado el Asistente para perfiles en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41d85-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="41d85-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="41d85-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="41d85-128">El número de páginas que se debe mostrar el proveedor que solicita el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="41d85-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="41d85-129">El proveedor debe devolver el número de páginas en lugar de TRUE o FALSE.</span><span class="sxs-lookup"><span data-stu-id="41d85-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="41d85-130">Por ejemplo, use la siguiente instrucción return para indicar que deben tres páginas para que se muestre:</span><span class="sxs-lookup"><span data-stu-id="41d85-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="41d85-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="41d85-131">_wParam_</span></span>
  
> <span data-ttu-id="41d85-132">[entrada] Un parámetro de 32 bits asociado con los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="41d85-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="41d85-133">El mensaje especificado en el parámetro _wMsgID_ dependen de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="41d85-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="41d85-134">Además de los valores esperados con los mensajes de ventana normal para un cuadro de diálogo modal, se pueden recibir los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="41d85-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="41d85-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="41d85-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="41d85-136">Cuando _wMsgID_ contiene WM_COMMAND, el usuario ha hecho clic en el botón **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="41d85-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="41d85-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="41d85-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="41d85-138">Cuando _wMsgID_ contiene WM_COMMAND, el usuario ha hecho clic en el botón **Atrás** .</span><span class="sxs-lookup"><span data-stu-id="41d85-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="41d85-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="41d85-139">_lParam_</span></span>
  
> <span data-ttu-id="41d85-140">[entrada] Un parámetro de 32 bits asociado con los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="41d85-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="41d85-141">El mensaje especificado en el parámetro _wMsgID_ dependen de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="41d85-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41d85-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41d85-142">Return value</span></span>

<span data-ttu-id="41d85-143">El valor devuelto por una función de **SERVICEWIZARDDLGPROC** en función depende en el mensaje de ventana recibido.</span><span class="sxs-lookup"><span data-stu-id="41d85-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="41d85-144">Tenga en cuenta que las excepcionales devuelven el valor para el mensaje WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="41d85-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="41d85-145">Los valores devueltos normales son:</span><span class="sxs-lookup"><span data-stu-id="41d85-145">The normal return values are:</span></span> 
  
<span data-ttu-id="41d85-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="41d85-146">TRUE</span></span> 
  
> <span data-ttu-id="41d85-147">El proveedor de servicios ha procesado el mensaje de ventana recibidos.</span><span class="sxs-lookup"><span data-stu-id="41d85-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="41d85-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="41d85-148">FALSE</span></span> 
  
> <span data-ttu-id="41d85-149">El proveedor de servicios no procesó el mensaje de ventana recibidos.</span><span class="sxs-lookup"><span data-stu-id="41d85-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41d85-150">Notas</span><span class="sxs-lookup"><span data-stu-id="41d85-150">Remarks</span></span>

<span data-ttu-id="41d85-151">Cuando el usuario se mueve de una página de propiedades a otra, el proveedor es responsable de la ocultación de controles de la página anterior y que muestra los controles de la página siguiente o anterior.</span><span class="sxs-lookup"><span data-stu-id="41d85-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="41d85-152">Cuando el usuario hace clic en el botón **siguiente** , se llama a la función **SERVICEWIZARDDLGPROC** en función con el mensaje WM_COMMAND y WIZ_NEXT en el parámetro _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="41d85-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="41d85-153">Los pasos siguientes describen lo que se produce entre el momento en que el usuario hace clic en **siguiente** y la hora en que se presentan las páginas de configuración del proveedor en la primera.</span><span class="sxs-lookup"><span data-stu-id="41d85-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="41d85-154">El Asistente para perfiles oculta todos los controles que se encuentran en la ventana.</span><span class="sxs-lookup"><span data-stu-id="41d85-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="41d85-155">El Asistente para perfiles agrega los controles ocultos del proveedor a la página.</span><span class="sxs-lookup"><span data-stu-id="41d85-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="41d85-156">El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviar el mensaje WM_INITDIALOG, por lo que el proveedor puede inicializar los controles.</span><span class="sxs-lookup"><span data-stu-id="41d85-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="41d85-157">El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, envía el mensaje WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="41d85-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="41d85-158">El proveedor devuelve el número de páginas que se muestran.</span><span class="sxs-lookup"><span data-stu-id="41d85-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="41d85-159">El Asistente para perfiles llama a **SERVICEWIZARDDLGPROC**, enviar el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="41d85-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="41d85-160">En este momento, el proveedor ya sea devuelve FALSE {error} o revela sus controles y devuelve TRUE {éxito}.</span><span class="sxs-lookup"><span data-stu-id="41d85-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="41d85-161">Si el Asistente para perfiles pasa ID_NEXT, se muestra la primera página del proveedor.</span><span class="sxs-lookup"><span data-stu-id="41d85-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="41d85-162">Si se pasa ID_PREV, se muestra la última página.</span><span class="sxs-lookup"><span data-stu-id="41d85-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="41d85-163">El Asistente para perfiles llama (función) **SERVICEWIZARDDLGPROC** del proveedor, enviar el mensaje WM_COMMAND con el parámetro _wParam_ establecido en WIZ_NEXT o WIZ_PREV (dependiendo de qué botón hizo clic el usuario).</span><span class="sxs-lookup"><span data-stu-id="41d85-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="41d85-164">El proveedor es responsable de mostrar u ocultar sus controles y escribir sus datos en el **IMAPIProp** se pasa al asistente paso a paso a través de su secuencia de páginas de perfil.</span><span class="sxs-lookup"><span data-stu-id="41d85-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="41d85-165">El proveedor debe devolver TRUE si la página siguiente o anterior se mostró correctamente, y FALSE si ni la página siguiente ni anterior se pudieron mostrar.</span><span class="sxs-lookup"><span data-stu-id="41d85-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="41d85-166">El proveedor debe tener en cuenta cuando está pasando fuera de su secuencia de páginas y responder de forma adecuada ocultando sus controles y escribir sus datos en el perfil.</span><span class="sxs-lookup"><span data-stu-id="41d85-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="41d85-167">Si el usuario pasos fuera de intervalo del proveedor de páginas, el Asistente para perfiles elimina los controles ocultos del proveedor desde el cuadro de diálogo y llama al proveedor de siguiente o muestra su página siguiente si era el último proveedor.</span><span class="sxs-lookup"><span data-stu-id="41d85-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

