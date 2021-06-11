---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430682"
---
# <a name="wizardentry"></a><span data-ttu-id="beeeb-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="beeeb-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="beeeb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="beeeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="beeeb-105">Define una función de punto de entrada del proveedor de servicios a la que llama el Asistente para perfiles para recuperar suficiente información para mostrar las hojas de propiedades de configuración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="beeeb-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="beeeb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="beeeb-106">Header file:</span></span>  <br/> |<span data-ttu-id="beeeb-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="beeeb-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="beeeb-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="beeeb-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="beeeb-109">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="beeeb-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="beeeb-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="beeeb-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="beeeb-111">Asistente para perfiles MAPI</span><span class="sxs-lookup"><span data-stu-id="beeeb-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="beeeb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="beeeb-112">Parameters</span></span>

 <span data-ttu-id="beeeb-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="beeeb-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="beeeb-114">[in] Identificador de instancia del DLL del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="beeeb-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="beeeb-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="beeeb-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="beeeb-116">[salida] Puntero a una cadena que contiene el nombre completo del recurso de cuadro de diálogo que debe mostrar el Asistente para perfiles durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="beeeb-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="beeeb-117">El tamaño máximo de la cadena, incluido el terminador NULL, es de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="beeeb-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="beeeb-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="beeeb-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="beeeb-119">[salida] Puntero a un procedimiento Windows cuadro de diálogo estándar al que llamará el Asistente para perfiles para notificar al proveedor de varios eventos.</span><span class="sxs-lookup"><span data-stu-id="beeeb-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="beeeb-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="beeeb-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="beeeb-121">[in] Puntero a una implementación de interfaz de propiedad que proporciona acceso a las propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="beeeb-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="beeeb-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="beeeb-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="beeeb-123">[in] Puntero al objeto de compatibilidad MAPI aplicable a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="beeeb-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="beeeb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beeeb-124">Return value</span></span>

<span data-ttu-id="beeeb-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="beeeb-125">S_OK</span></span> 
  
> <span data-ttu-id="beeeb-126">La función **WIZARDENTRY** del proveedor de servicios se llamó correctamente.</span><span class="sxs-lookup"><span data-stu-id="beeeb-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="beeeb-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="beeeb-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="beeeb-128">Un error de origen inesperado o desconocido impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="beeeb-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="beeeb-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="beeeb-129">Remarks</span></span>

<span data-ttu-id="beeeb-130">El Asistente para perfiles llama a **la función basada en WIZARDENTRY** cuando está listo para mostrar la interfaz de usuario de configuración del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="beeeb-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="beeeb-131">Cuando el Asistente para perfiles haya terminado de configurar todos los proveedores, escribe las propiedades de configuración en el perfil llamando a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="beeeb-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="beeeb-132">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="beeeb-132">Notes to implementers</span></span>

<span data-ttu-id="beeeb-133">El nombre de la **función basada en WIZARDENTRY** debe colocarse en la WIZARD_ENTRY_NAME en MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="beeeb-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="beeeb-134">El nombre del recurso es el del recurso de cuadro de diálogo que se representará en el panel del Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="beeeb-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="beeeb-135">El recurso que se pasa atrás debe contener todas las páginas de un único recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="beeeb-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="beeeb-136">Cuando el Asistente para perfiles recibe este recurso, omite el estilo de cuadro de diálogo, pero no los estilos de control, y crea todos los controles como secundarios de la página Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="beeeb-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="beeeb-137">Todos los controles están ocultos inicialmente.</span><span class="sxs-lookup"><span data-stu-id="beeeb-137">All controls are initially hidden.</span></span> <span data-ttu-id="beeeb-138">Los proveedores deben asegurarse de que las coordenadas de sus controles estén basadas en cero o cero y que no superen un ancho máximo de 200 unidades de diálogo y un alto máximo de 150 unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="beeeb-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="beeeb-139">Los identificadores de control inferiores a 400 están reservados para el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="beeeb-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="beeeb-140">El Asistente para perfiles muestra el título del proveedor en texto en negrita encima de la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="beeeb-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="beeeb-141">El proveedor debe conservar el puntero de interfaz de propiedad proporcionado en el parámetro  _lpMAPIProp_ para su referencia futura.</span><span class="sxs-lookup"><span data-stu-id="beeeb-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="beeeb-142">El Asistente para perfiles trata solo el conjunto más básico de propiedades y el proveedor puede usar la implementación de la interfaz de propiedades para incluir propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="beeeb-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="beeeb-143">Durante la configuración, los proveedores deben agregar sus propiedades de configuración al objeto que implementa la interfaz de propiedades.</span><span class="sxs-lookup"><span data-stu-id="beeeb-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="beeeb-144">Una vez configurados todos los proveedores, el Asistente para perfiles agrega estas propiedades al perfil.</span><span class="sxs-lookup"><span data-stu-id="beeeb-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="beeeb-145">Para obtener más información sobre cómo usar esta función, vea [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="beeeb-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

