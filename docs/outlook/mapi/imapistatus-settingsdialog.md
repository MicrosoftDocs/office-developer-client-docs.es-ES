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
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817472"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="4c192-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="4c192-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="4c192-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c192-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c192-105">Muestra una hoja de propiedades que permite al usuario que cambie la configuración de un proveedor de servicios que este método no se admite en los objetos de estado que implementa MAPI.</span><span class="sxs-lookup"><span data-stu-id="4c192-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4c192-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c192-106">Parameters</span></span>

 <span data-ttu-id="4c192-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4c192-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="4c192-108">[entrada] Identificador de la ventana principal de la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="4c192-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="4c192-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c192-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4c192-110">[entrada] Una máscara de bits de indicadores que controla la presentación de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c192-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="4c192-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="4c192-111">The following flag can be set:</span></span>
    
<span data-ttu-id="4c192-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="4c192-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="4c192-113">Sugiere que el proveedor no debe habilitar a los usuarios cambiar las propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="4c192-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="4c192-114">Esta marca es sólo una sugerencia; se puede hacer caso omiso.</span><span class="sxs-lookup"><span data-stu-id="4c192-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c192-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c192-115">Return value</span></span>

<span data-ttu-id="4c192-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c192-116">S_OK</span></span> 
  
> <span data-ttu-id="4c192-117">La hoja de propiedades de configuración se mostró correctamente.</span><span class="sxs-lookup"><span data-stu-id="4c192-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="4c192-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4c192-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4c192-119">El objeto de estado no es compatible con este método, como se indica por la ausencia de la marca STATUS_SETTINGS_DIALOG en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4c192-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c192-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c192-120">Remarks</span></span>

<span data-ttu-id="4c192-121">El método **SettingsDialog** muestra una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="4c192-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="4c192-122">Todos los proveedores de servicios deben admitir el método de **diálogo Configuración** , pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="4c192-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="4c192-123">Proveedores de servicio pueden implementar sus propias hojas (propiedad) o utilizar la implementación proporcionada en el soporte técnico método del objeto [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) .</span><span class="sxs-lookup"><span data-stu-id="4c192-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="4c192-124">**DoConfigPropsheet** crea una hoja de propiedades de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4c192-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4c192-125">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="4c192-125">Notes to implementers</span></span>

<span data-ttu-id="4c192-126">Si un proveedor de transporte remoto tiene cualquier opción de configuración, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4c192-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="4c192-127">Abrir la sección de perfil del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4c192-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="4c192-128">Obtenga el transporte valores de la propiedad del proveedor del perfil.</span><span class="sxs-lookup"><span data-stu-id="4c192-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="4c192-129">Mostrar los valores de propiedad en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c192-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="4c192-130">Si el cuadro de diálogo permite la edición de la configuración de propiedades, compruebe que la nueva configuración es válida y almacenarlas atrás en la sección de perfil del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4c192-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="4c192-131">Devolver S_OK o los valores de error devueltos durante los pasos anteriores.</span><span class="sxs-lookup"><span data-stu-id="4c192-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="4c192-132">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4c192-132">Notes to callers</span></span>

<span data-ttu-id="4c192-133">Puede usar la hoja de propiedades que se muestra a través de **diálogo Configuración** para realizar diversas tareas, como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="4c192-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="4c192-134">Especificar un almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4c192-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="4c192-135">Especificar un orden de transporte.</span><span class="sxs-lookup"><span data-stu-id="4c192-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="4c192-136">Especificar un contenedor de libreta de direcciones predeterminada para la exploración.</span><span class="sxs-lookup"><span data-stu-id="4c192-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="4c192-137">Especificar un criterio de búsqueda para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="4c192-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="4c192-138">Especifique una libreta de direcciones personales de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4c192-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="4c192-139">Pueden implementar proveedores de servicios de las hojas de propiedades que son de lectura y escritura, de sólo lectura, o una combinación de permisos, dependiendo de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c192-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="4c192-140">Proveedores de servicios pueden implementar permisos diferentes en las propiedades individuales mediante la configuración de restricciones de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c192-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="4c192-141">El modo predeterminado para las hojas de propiedades es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4c192-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="4c192-142">Puede solicitar las hojas de propiedades de sólo lectura estableciendo el indicador UI_READONLY en las llamadas al **diálogo Configuración**.</span><span class="sxs-lookup"><span data-stu-id="4c192-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="4c192-143">Proveedores de servicios que se pueden implementar las hojas de propiedades de sólo lectura pueden hacerlo.</span><span class="sxs-lookup"><span data-stu-id="4c192-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="4c192-144">Sin embargo, debido a que algunos proveedores de servicios no pueden reemplazar el modo predeterminado, debe estar preparado para tratar las hojas de propiedades de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="4c192-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="4c192-145">Debido a que una interfaz de usuario siempre está relacionada con esta operación, sólo los clientes interactivos deben llamar **diálogo Configuración**.</span><span class="sxs-lookup"><span data-stu-id="4c192-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c192-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c192-146">See also</span></span>



[<span data-ttu-id="4c192-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="4c192-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="4c192-148">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="4c192-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="4c192-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4c192-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

