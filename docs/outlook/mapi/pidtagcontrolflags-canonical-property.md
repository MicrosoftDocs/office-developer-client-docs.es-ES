---
title: Propiedad canónica PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430885"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="17284-103">Propiedad canónica PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="17284-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="17284-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17284-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17284-105">Contiene una máscara de bits de marcas que rigen el comportamiento de un control usado en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="17284-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17284-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="17284-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17284-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="17284-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="17284-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17284-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17284-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="17284-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="17284-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="17284-110">Data type:</span></span>  <br/> |<span data-ttu-id="17284-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="17284-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="17284-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17284-112">Area:</span></span>  <br/> |<span data-ttu-id="17284-113">Tabla para mostrar MAPI</span><span class="sxs-lookup"><span data-stu-id="17284-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17284-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17284-114">Remarks</span></span>

<span data-ttu-id="17284-115">Se pueden establecer una o varias de las siguientes marcas para esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="17284-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="17284-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="17284-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="17284-117">El control puede tener Double-Byte de juego de caracteres (DBCS) en él.</span><span class="sxs-lookup"><span data-stu-id="17284-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="17284-118">Esta marca se usa con controles de edición.</span><span class="sxs-lookup"><span data-stu-id="17284-118">This flag is used with edit controls.</span></span> <span data-ttu-id="17284-119">Permite conjuntos de caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="17284-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="17284-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="17284-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="17284-121">El control se puede editar; se puede cambiar el valor asociado al control.</span><span class="sxs-lookup"><span data-stu-id="17284-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="17284-122">Cuando no se establece esta marca, el control es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17284-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="17284-123">Este valor se omite en los controles de etiqueta, cuadro de grupo, botón de inserción estándar, cuadro de lista desplegable multivalor y cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="17284-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="17284-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="17284-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="17284-125">El control de edición puede contener varias líneas.</span><span class="sxs-lookup"><span data-stu-id="17284-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="17284-126">Esto significa que se puede especificar un carácter devuelto dentro del control.</span><span class="sxs-lookup"><span data-stu-id="17284-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="17284-127">Esta marca solo es válida para los controles de edición.</span><span class="sxs-lookup"><span data-stu-id="17284-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="17284-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="17284-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="17284-129">Se aplica a los controles de edición.</span><span class="sxs-lookup"><span data-stu-id="17284-129">Applies to edit controls.</span></span> <span data-ttu-id="17284-130">El control de edición se trata como una contraseña.</span><span class="sxs-lookup"><span data-stu-id="17284-130">The edit control is treated like a password.</span></span> <span data-ttu-id="17284-131">El valor se muestra con asteriscos en lugar de hacer eco de los caracteres reales especificados.</span><span class="sxs-lookup"><span data-stu-id="17284-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="17284-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="17284-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="17284-133">Si el control permite cambios (DT_EDITABLE), debe tener un valor antes de llamar a [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="17284-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="17284-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="17284-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="17284-135">Habilita la configuración inmediata de un valor; tan pronto como cambia un valor en el control, MAPI llama al **método SetProps** para la propiedad asociada con ese control.</span><span class="sxs-lookup"><span data-stu-id="17284-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="17284-136">Cuando no se establece esta marca, los valores se establecen cuando se descarta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17284-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="17284-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="17284-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="17284-138">Cuando se realiza una selección en el cuadro de lista, la columna de índice de ese cuadro de lista se establece como una propiedad.</span><span class="sxs-lookup"><span data-stu-id="17284-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="17284-139">Siempre se usa con DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="17284-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="17284-140">Esta propiedad se almacena en el miembro ulCtlFlags de la [estructura DTCTL de un](dtctl.md) control.</span><span class="sxs-lookup"><span data-stu-id="17284-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="17284-141">La mayoría de las marcas de control se aplican a todos los controles que permiten la entrada del usuario; algunos solo se aplican al control de edición.</span><span class="sxs-lookup"><span data-stu-id="17284-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="17284-142">Los controles que no permiten la entrada del usuario, como un botón o una etiqueta, establecen 0 para sus marcas de control.</span><span class="sxs-lookup"><span data-stu-id="17284-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="17284-143">Muchos de los valores de marca son autoexplicativos.</span><span class="sxs-lookup"><span data-stu-id="17284-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="17284-144">Por ejemplo, DT_REQUIRED se establece para un control, debe contener un valor antes de que se pueda descartar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17284-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="17284-145">El proveedor de servicios puede proporcionar un valor a través de su **implementación imapiprop** o el usuario puede escribir uno.</span><span class="sxs-lookup"><span data-stu-id="17284-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="17284-146">DT_EDITABLE indica que se puede modificar el valor del control.</span><span class="sxs-lookup"><span data-stu-id="17284-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="17284-147">DT_MULTILINE permite que el valor de un control de edición abarque varias líneas.</span><span class="sxs-lookup"><span data-stu-id="17284-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="17284-148">Algunas marcas de control no son tan obvias en su significado.</span><span class="sxs-lookup"><span data-stu-id="17284-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="17284-149">Cuando un control establece la marca DT_SET_IMMEDIATE, cualquier cambio en su valor afectará tan pronto como el usuario se mueva a un nuevo control.</span><span class="sxs-lookup"><span data-stu-id="17284-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="17284-150">MAPI realiza una sola llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la interfaz de propiedad para la propiedad del control.</span><span class="sxs-lookup"><span data-stu-id="17284-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="17284-151">Esto es diferente del comportamiento predeterminado, que es posponer que los cambios en los valores de control tengan efecto hasta que el usuario seleccione el botón **Aceptar** o descarte el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17284-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="17284-152">La DT_SET_IMMEDIATE se usa a menudo en combinación con las notificaciones de tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="17284-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="17284-153">En la tabla siguiente se enumeran los tipos de controles y todos los valores de marca que se pueden establecer para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="17284-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="17284-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="17284-154">**Control**</span></span>|<span data-ttu-id="17284-155">**Valores válidos para esta propiedad**</span><span class="sxs-lookup"><span data-stu-id="17284-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17284-156">Botón</span><span class="sxs-lookup"><span data-stu-id="17284-156">Button</span></span>  <br/> |<span data-ttu-id="17284-157">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-158">Casilla</span><span class="sxs-lookup"><span data-stu-id="17284-158">Check box</span></span>  <br/> |<span data-ttu-id="17284-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="17284-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="17284-160">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="17284-160">Combo box</span></span>  <br/> |<span data-ttu-id="17284-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="17284-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="17284-162">Cuadro de lista desplegable</span><span class="sxs-lookup"><span data-stu-id="17284-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="17284-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="17284-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="17284-164">Editar</span><span class="sxs-lookup"><span data-stu-id="17284-164">Edit</span></span>  <br/> |<span data-ttu-id="17284-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="17284-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="17284-166">Cuadro de grupo</span><span class="sxs-lookup"><span data-stu-id="17284-166">Group box</span></span>  <br/> |<span data-ttu-id="17284-167">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-168">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="17284-168">Label</span></span>  <br/> |<span data-ttu-id="17284-169">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-170">Cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="17284-170">List box</span></span>  <br/> |<span data-ttu-id="17284-171">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-172">Cuadro de lista desplegable De varios valores</span><span class="sxs-lookup"><span data-stu-id="17284-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="17284-173">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-174">Cuadro de lista Multivalor</span><span class="sxs-lookup"><span data-stu-id="17284-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="17284-175">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-176">Página con pestañas</span><span class="sxs-lookup"><span data-stu-id="17284-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="17284-177">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="17284-178">Botón de radio</span><span class="sxs-lookup"><span data-stu-id="17284-178">Radio button</span></span>  <br/> |<span data-ttu-id="17284-179">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="17284-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="17284-180">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17284-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="17284-181">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="17284-181">Header files</span></span>

<span data-ttu-id="17284-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17284-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="17284-183">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="17284-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="17284-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17284-184">Mapitags.h</span></span>
  
> <span data-ttu-id="17284-185">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="17284-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17284-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="17284-186">See also</span></span>



[<span data-ttu-id="17284-187">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17284-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17284-188">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="17284-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17284-189">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="17284-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17284-190">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="17284-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

