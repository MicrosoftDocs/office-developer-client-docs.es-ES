---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578629"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="adb98-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="adb98-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="adb98-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adb98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adb98-105">Agrega un proveedor de servicios para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="adb98-105">Adds a service provider to the message service.</span></span> 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="adb98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="adb98-106">Parameters</span></span>

 <span data-ttu-id="adb98-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="adb98-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="adb98-108">[entrada] Un puntero en el nombre del proveedor que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="adb98-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="adb98-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="adb98-109">_cValues_</span></span>
  
> <span data-ttu-id="adb98-110">[entrada] El recuento de valores de la propiedad indicada por el parámetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="adb98-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="adb98-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="adb98-111">_lpProps_</span></span>
  
> <span data-ttu-id="adb98-112">[entrada] Un puntero a una matriz de valor de propiedad que se describe las propiedades del proveedor que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="adb98-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="adb98-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="adb98-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="adb98-114">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="adb98-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="adb98-115">Si se establece la marca MAPI_DIALOG en el parámetro _ulFlags_ , se usa el parámetro _ulUIParam_ .</span><span class="sxs-lookup"><span data-stu-id="adb98-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="adb98-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="adb98-116">_ulFlags_</span></span>
  
> <span data-ttu-id="adb98-117">[entrada] Una máscara de bits de indicadores que controla la adición de proveedor.</span><span class="sxs-lookup"><span data-stu-id="adb98-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="adb98-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="adb98-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="adb98-119">MAPI_DIALOG: Muestra un cuadro de diálogo para solicitar información de configuración.</span><span class="sxs-lookup"><span data-stu-id="adb98-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="adb98-120">MAPI_UNICODE.: Las propiedades de cadena y el nombre del proveedor están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="adb98-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="adb98-121">Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="adb98-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="adb98-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="adb98-122">_lpUID_</span></span>
  
> <span data-ttu-id="adb98-123">[out] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa el proveedor que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="adb98-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="adb98-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="adb98-124">Return value</span></span>

<span data-ttu-id="adb98-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="adb98-125">S_OK</span></span> 
  
> <span data-ttu-id="adb98-126">El proveedor se ha agregado correctamente al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="adb98-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="adb98-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="adb98-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="adb98-128">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="adb98-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="adb98-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="adb98-129">Remarks</span></span>

<span data-ttu-id="adb98-130">El método **IProviderAdmin::CreateProvider** agrega un proveedor de servicios para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="adb98-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="adb98-131">El parámetro _lpszProvider_ debe apuntar al nombre de un proveedor que pertenece al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="adb98-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="adb98-132">**CreateProvider** no comprueba si el nombre coincide con el nombre de un proveedor en el servicio; Si el nombre pasado no coincide con un nombre de servicio, la llamada se realiza correctamente, pero los resultados serán impredecibles.</span><span class="sxs-lookup"><span data-stu-id="adb98-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="adb98-133">La mayoría de los servicios de mensaje no permiten que los proveedores se agregan o eliminan mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="adb98-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="adb98-134">Después de todo de la información disponible sobre el servicio de proveedor se ha agregado al perfil desde el archivo Mapisvc.inf, **CreateProvider** llama la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_ PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="adb98-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="adb98-135">Si de MAPI_DIALOG se establece en el **CreateProvider** parámetro del método _ulFlags_ , los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="adb98-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="adb98-136">Estos parámetros adicionales habilitar el proveedor de servicios mostrar su hoja de propiedades, por lo que el usuario puede escribir valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="adb98-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adb98-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="adb98-137">See also</span></span>

- [<span data-ttu-id="adb98-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="adb98-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="adb98-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="adb98-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="adb98-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="adb98-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="adb98-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="adb98-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

