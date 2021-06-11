---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439733"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="482a8-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="482a8-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="482a8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="482a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="482a8-105">Muestra una hoja de propiedades que permite al usuario cambiar la configuración de un proveedor de servicios Este método no se admite en objetos de estado que implementa MAPI.</span><span class="sxs-lookup"><span data-stu-id="482a8-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="482a8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="482a8-106">Parameters</span></span>

 <span data-ttu-id="482a8-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="482a8-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="482a8-108">[in] Identificador de la ventana principal de la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="482a8-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="482a8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="482a8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="482a8-110">[in] Máscara de bits de marcas que controla la presentación de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="482a8-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="482a8-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="482a8-111">The following flag can be set:</span></span>
    
<span data-ttu-id="482a8-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="482a8-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="482a8-113">Sugiere que el proveedor no debe permitir que los usuarios cambien las propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="482a8-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="482a8-114">Esta marca es solo una sugerencia; puede omitirse.</span><span class="sxs-lookup"><span data-stu-id="482a8-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="482a8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="482a8-115">Return value</span></span>

<span data-ttu-id="482a8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="482a8-116">S_OK</span></span> 
  
> <span data-ttu-id="482a8-117">La hoja de propiedades de configuración se ha mostrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="482a8-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="482a8-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="482a8-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="482a8-119">El objeto status no admite este método, como se indica por la ausencia de la marca STATUS_SETTINGS_DIALOG en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="482a8-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="482a8-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="482a8-120">Remarks</span></span>

<span data-ttu-id="482a8-121">El **método IMAPIStatus::SettingsDialog** muestra una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="482a8-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="482a8-122">Todos los proveedores de servicios deben admitir **el método SettingsDialog,** pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="482a8-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="482a8-123">Los proveedores de servicios pueden implementar sus propias hojas de propiedades o usar la implementación proporcionada en el método [IMAPISupport::D oConfigPropsheet del](imapisupport-doconfigpropsheet.md) objeto de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="482a8-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="482a8-124">**DoConfigPropsheet** crea una hoja de propiedades de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="482a8-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="482a8-125">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="482a8-125">Notes to implementers</span></span>

<span data-ttu-id="482a8-126">Si un proveedor de transporte remoto tiene alguna configuración, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="482a8-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="482a8-127">Abra la sección de perfil del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="482a8-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="482a8-128">Obtener la configuración de la propiedad del proveedor de transporte desde el perfil.</span><span class="sxs-lookup"><span data-stu-id="482a8-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="482a8-129">Mostrar la configuración de la propiedad en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="482a8-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="482a8-130">Si el cuadro de diálogo permite editar la configuración de la propiedad, compruebe que la nueva configuración es válida y guárdala de nuevo en la sección de perfil del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="482a8-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="482a8-131">Devuelve S_OK, o cualquier valor de error devuelto durante los pasos anteriores.</span><span class="sxs-lookup"><span data-stu-id="482a8-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="482a8-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="482a8-132">Notes to callers</span></span>

<span data-ttu-id="482a8-133">Puede usar la hoja de propiedades que se muestra a través **de SettingsDialog** para realizar una variedad de tareas, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="482a8-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="482a8-134">Especifique un almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="482a8-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="482a8-135">Especifique un pedido de transporte.</span><span class="sxs-lookup"><span data-stu-id="482a8-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="482a8-136">Especifique un contenedor de libreta de direcciones predeterminado para la exploración.</span><span class="sxs-lookup"><span data-stu-id="482a8-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="482a8-137">Especifique un orden de búsqueda para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="482a8-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="482a8-138">Especifique una libreta de direcciones personal predeterminada.</span><span class="sxs-lookup"><span data-stu-id="482a8-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="482a8-139">Los proveedores de servicios pueden implementar hojas de propiedades de lectura y escritura, de solo lectura o una combinación de permisos, según la propiedad.</span><span class="sxs-lookup"><span data-stu-id="482a8-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="482a8-140">Los proveedores de servicios pueden implementar diferentes permisos en propiedades individuales estableciendo restricciones de propiedades.</span><span class="sxs-lookup"><span data-stu-id="482a8-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="482a8-141">El modo predeterminado para las hojas de propiedades es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="482a8-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="482a8-142">Puede solicitar hojas de propiedades de solo lectura estableciendo la marca UI_READONLY en las llamadas a **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="482a8-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="482a8-143">Los proveedores de servicios que pueden implementar hojas de propiedades de solo lectura pueden hacerlo.</span><span class="sxs-lookup"><span data-stu-id="482a8-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="482a8-144">Sin embargo, dado que algunos proveedores de servicios no pueden invalidar el modo predeterminado, debe estar preparado para controlar las hojas de propiedades de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="482a8-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="482a8-145">Dado que una interfaz de usuario siempre está implicada en esta operación, solo los clientes interactivos deben llamar a **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="482a8-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="482a8-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="482a8-146">See also</span></span>



[<span data-ttu-id="482a8-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="482a8-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="482a8-148">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="482a8-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="482a8-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="482a8-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

