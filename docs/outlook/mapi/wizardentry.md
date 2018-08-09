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
ms.openlocfilehash: 2c307d18c5b62e5190aa10632a47a3f16b80e81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820980"
---
# <a name="wizardentry"></a><span data-ttu-id="84247-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="84247-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="84247-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84247-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84247-105">Define una función de punto de entrada de proveedor de servicio que el Asistente para perfiles llama para recuperar suficiente información como para mostrar las hojas de propiedades de configuración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="84247-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84247-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="84247-106">Header file:</span></span>  <br/> |<span data-ttu-id="84247-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="84247-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="84247-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="84247-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="84247-109">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="84247-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="84247-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="84247-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="84247-111">Asistente para el perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="84247-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="84247-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84247-112">Parameters</span></span>

 <span data-ttu-id="84247-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="84247-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="84247-114">[entrada] Identificador de instancia del archivo DLL del proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="84247-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="84247-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="84247-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="84247-116">[out] Puntero a una cadena que contiene el nombre completo del recurso de cuadro de diálogo que debe mostrar el Asistente para perfiles durante la configuración.</span><span class="sxs-lookup"><span data-stu-id="84247-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="84247-117">El tamaño máximo de la cadena, incluido el terminador NULL, es de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="84247-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="84247-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="84247-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="84247-119">[out] Puntero a un procedimiento de cuadros de diálogo de Windows estándar que se llamará por el Asistente para perfiles para notificar el proveedor de varios eventos.</span><span class="sxs-lookup"><span data-stu-id="84247-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="84247-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="84247-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="84247-121">[entrada] Puntero a una implementación de la interfaz de propiedad que proporciona acceso a las propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="84247-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="84247-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="84247-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="84247-123">[entrada] Puntero al objeto de compatibilidad con MAPI aplicable a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="84247-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84247-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84247-124">Return value</span></span>

<span data-ttu-id="84247-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="84247-125">S_OK</span></span> 
  
> <span data-ttu-id="84247-126">Función **WIZARDENTRY** del proveedor de servicio se ha llamado correctamente.</span><span class="sxs-lookup"><span data-stu-id="84247-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="84247-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="84247-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="84247-128">Un error de origen desconocido o inesperado no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="84247-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84247-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84247-129">Remarks</span></span>

<span data-ttu-id="84247-130">El Asistente para perfiles llama a la función **WIZARDENTRY** en función cuando está listo para mostrar la interfaz de usuario de configuración del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="84247-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="84247-131">Cuando el Asistente para perfiles haya terminado de configurar todos los proveedores, escribe las propiedades de configuración para el perfil mediante una llamada a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="84247-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="84247-132">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="84247-132">Notes to implementers</span></span>

<span data-ttu-id="84247-133">El nombre de la función **WIZARDENTRY** según se debe colocar en la entrada WIZARD_ENTRY_NAME en MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="84247-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="84247-134">El nombre del recurso es que del recurso de diálogo que se representará en el panel del Asistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="84247-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="84247-135">El recurso que se pasa hacia atrás debe contener todas las páginas de un recurso de cuadro de diálogo único.</span><span class="sxs-lookup"><span data-stu-id="84247-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="84247-136">Cuando el Asistente para perfiles recibe este recurso, pasa por alto el estilo del cuadro de diálogo, pero no los estilos de control y todos los controles se crea como elementos secundarios de la página del Asistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="84247-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="84247-137">Todos los controles inicialmente están ocultos.</span><span class="sxs-lookup"><span data-stu-id="84247-137">All controls are initially hidden.</span></span> <span data-ttu-id="84247-138">Deben realizar los proveedores de asegurarse de que las coordenadas de sus controles sean cero o basado en cero, y que no superen un ancho máximo de 200 unidades de cuadro de diálogo y una altura máxima de 150 unidades de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="84247-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="84247-139">Identificadores de control debajo de 400 están reservados para el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="84247-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="84247-140">El Asistente para perfiles muestra el título del proveedor en texto en negrita por encima de la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="84247-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="84247-141">El puntero de interfaz de propiedad proporcionado en el parámetro _lpMAPIProp_ se debe conservar por el proveedor para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="84247-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="84247-142">El Asistente para perfiles se ocupa sólo el conjunto más básico de propiedades y el proveedor puede utilizar la implementación de la interfaz de la propiedad para incluir propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="84247-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="84247-143">Durante la configuración, los proveedores deben agregar sus propiedades de configuración para el objeto que implementa la interfaz (propiedad).</span><span class="sxs-lookup"><span data-stu-id="84247-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="84247-144">Después de que se han configurado todos los proveedores, el Asistente para perfiles agrega estas propiedades para el perfil.</span><span class="sxs-lookup"><span data-stu-id="84247-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="84247-145">Para obtener más información acerca de cómo usar esta función, vea [Compatibilidad con configuración del servicio de mensajes](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="84247-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

