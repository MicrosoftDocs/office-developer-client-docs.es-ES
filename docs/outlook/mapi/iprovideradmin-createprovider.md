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
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430808"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="b25f8-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="b25f8-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="b25f8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b25f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b25f8-105">Agrega un proveedor de servicios al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b25f8-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="b25f8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b25f8-106">Parameters</span></span>

 <span data-ttu-id="b25f8-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="b25f8-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="b25f8-108">[in] Puntero al nombre del proveedor que se agregará.</span><span class="sxs-lookup"><span data-stu-id="b25f8-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="b25f8-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="b25f8-109">_cValues_</span></span>
  
> <span data-ttu-id="b25f8-110">[in] Recuento de valores de propiedad señalados por el _parámetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="b25f8-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="b25f8-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="b25f8-111">_lpProps_</span></span>
  
> <span data-ttu-id="b25f8-112">[in] Puntero a una matriz de valores de propiedad que describe las propiedades del proveedor que se agregarán.</span><span class="sxs-lookup"><span data-stu-id="b25f8-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="b25f8-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b25f8-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="b25f8-114">[in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método.</span><span class="sxs-lookup"><span data-stu-id="b25f8-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="b25f8-115">El _parámetro ulUIParam_ se usa si la marca MAPI_DIALOG se establece en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b25f8-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b25f8-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b25f8-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b25f8-117">[in] Máscara de bits de marcas que controla la adición del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b25f8-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="b25f8-118">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="b25f8-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="b25f8-119">MAPI_DIALOG: muestra un cuadro de diálogo para solicitar información de configuración.</span><span class="sxs-lookup"><span data-stu-id="b25f8-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="b25f8-120">MAPI_UNICODE: el nombre del proveedor y las propiedades de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b25f8-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="b25f8-121">Si la MAPI_UNICODE no está establecida, estas cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b25f8-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b25f8-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="b25f8-122">_lpUID_</span></span>
  
> <span data-ttu-id="b25f8-123">[salida] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa el proveedor que se debe agregar.</span><span class="sxs-lookup"><span data-stu-id="b25f8-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b25f8-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b25f8-124">Return value</span></span>

<span data-ttu-id="b25f8-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="b25f8-125">S_OK</span></span> 
  
> <span data-ttu-id="b25f8-126">El proveedor se agregó correctamente al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b25f8-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="b25f8-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b25f8-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b25f8-128">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b25f8-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b25f8-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b25f8-129">Remarks</span></span>

<span data-ttu-id="b25f8-130">El **método IProviderAdmin::CreateProvider** agrega un proveedor de servicios al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b25f8-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="b25f8-131">El  _parámetro lpszProvider_ debe apuntar al nombre de un proveedor que pertenece al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b25f8-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="b25f8-132">**CreateProvider** no comprueba si el nombre coincide con el nombre de un proveedor en el servicio; si el nombre pasado no coincide con un nombre de servicio, la llamada se realiza correctamente, pero los resultados son impredecibles.</span><span class="sxs-lookup"><span data-stu-id="b25f8-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="b25f8-133">La mayoría de los servicios de mensajes no permiten agregar ni eliminar proveedores mientras el perfil está en uso.</span><span class="sxs-lookup"><span data-stu-id="b25f8-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="b25f8-134">Después de agregar toda la información disponible sobre el proveedor de servicios al perfil desde el archivo Mapisvc.inf, **CreateProvider** llama a la función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="b25f8-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="b25f8-135">Si MAPI_DIALOG se establece en el parámetro _ulFlags_ del método **CreateProvider,** los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b25f8-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="b25f8-136">Estos parámetros adicionales permiten al proveedor de servicios mostrar su hoja de propiedades para que el usuario pueda especificar las opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="b25f8-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b25f8-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b25f8-137">See also</span></span>

- [<span data-ttu-id="b25f8-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b25f8-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="b25f8-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="b25f8-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="b25f8-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b25f8-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="b25f8-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b25f8-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

