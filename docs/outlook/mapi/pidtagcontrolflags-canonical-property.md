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
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819392"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="42ff5-103">Propiedad canónica PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="42ff5-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="42ff5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42ff5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42ff5-105">Contiene una máscara de bits de indicadores que rigen el comportamiento de un control que se utiliza en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="42ff5-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42ff5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="42ff5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42ff5-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="42ff5-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="42ff5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="42ff5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42ff5-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="42ff5-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="42ff5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="42ff5-110">Data type:</span></span>  <br/> |<span data-ttu-id="42ff5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="42ff5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="42ff5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="42ff5-112">Area:</span></span>  <br/> |<span data-ttu-id="42ff5-113">Tabla MAPI para mostrar</span><span class="sxs-lookup"><span data-stu-id="42ff5-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42ff5-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42ff5-114">Remarks</span></span>

<span data-ttu-id="42ff5-115">Esta propiedad se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="42ff5-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="42ff5-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="42ff5-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="42ff5-117">El control puede tener caracteres del juego de caracteres de doble Byte (DBCS) en ella.</span><span class="sxs-lookup"><span data-stu-id="42ff5-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="42ff5-118">Este indicador se utiliza con controles de edición.</span><span class="sxs-lookup"><span data-stu-id="42ff5-118">This flag is used with edit controls.</span></span> <span data-ttu-id="42ff5-119">Permite que los conjuntos de caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="42ff5-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="42ff5-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="42ff5-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="42ff5-121">El control se puede editar; se puede cambiar el valor asociado al control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="42ff5-122">Cuando no se establece este indicador, el control es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="42ff5-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="42ff5-123">Este valor se omite en la etiqueta, cuadro de grupo, botón de comando estándar, multivalor desplegable de un cuadro de lista y controles de cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="42ff5-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="42ff5-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="42ff5-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="42ff5-125">El control de edición puede contener varias líneas.</span><span class="sxs-lookup"><span data-stu-id="42ff5-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="42ff5-126">Esto significa que un carácter de retorno puede especificarse dentro del control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="42ff5-127">Esta marca es válida para sólo controles de edición.</span><span class="sxs-lookup"><span data-stu-id="42ff5-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="42ff5-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="42ff5-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="42ff5-129">Se aplica a controles de edición.</span><span class="sxs-lookup"><span data-stu-id="42ff5-129">Applies to edit controls.</span></span> <span data-ttu-id="42ff5-130">El control de edición se trata como una contraseña.</span><span class="sxs-lookup"><span data-stu-id="42ff5-130">The edit control is treated like a password.</span></span> <span data-ttu-id="42ff5-131">El valor se muestra con asteriscos en lugar de eco de los caracteres reales especificados.</span><span class="sxs-lookup"><span data-stu-id="42ff5-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="42ff5-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="42ff5-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="42ff5-133">Si el control permite cambios (DT_EDITABLE), debe tener un valor antes de llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="42ff5-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="42ff5-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="42ff5-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="42ff5-135">Permite la configuración de ejecución de un valor; tan pronto como un valor en el control de cambios, MAPI llama al método de **SetProps** para la propiedad asociada a ese control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="42ff5-136">Cuando no se establece este marcador, se establecen los valores cuando se cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42ff5-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="42ff5-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="42ff5-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="42ff5-138">Cuando se realiza una selección dentro del cuadro de lista, la columna de índice de ese cuadro de lista se establece como una propiedad.</span><span class="sxs-lookup"><span data-stu-id="42ff5-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="42ff5-139">Siempre se utiliza con DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="42ff5-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="42ff5-140">Esta propiedad se almacena en el miembro ulCtlFlags de la estructura de un control [DTCTL](dtctl.md) .</span><span class="sxs-lookup"><span data-stu-id="42ff5-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="42ff5-141">La mayoría de los indicadores de control se aplican a todos los controles que permiten la entrada del usuario; Algunas se aplican sólo para el control de edición.</span><span class="sxs-lookup"><span data-stu-id="42ff5-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="42ff5-142">Los controles que no permiten la entrada del usuario, como un botón o una etiqueta, establecen 0 para sus indicadores de control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="42ff5-143">Muchos de los valores de indicador son explican por sí solos.</span><span class="sxs-lookup"><span data-stu-id="42ff5-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="42ff5-144">Por ejemplo, cuando DT_REQUIRED se establece para un control, debe contener un valor antes de que se permite el cuadro de diálogo para ser descartados.</span><span class="sxs-lookup"><span data-stu-id="42ff5-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="42ff5-145">El proveedor de servicios puede proporcionar un valor a través de su implementación de **IMAPIProp** o el usuario puede escribir uno.</span><span class="sxs-lookup"><span data-stu-id="42ff5-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="42ff5-146">DT_EDITABLE indica que se puede modificar el valor para el control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="42ff5-147">DT_MULTILINE permite que el valor de un control de edición abarcar varias líneas.</span><span class="sxs-lookup"><span data-stu-id="42ff5-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="42ff5-148">Algunos indicadores de control no son tan obvias en su significado.</span><span class="sxs-lookup"><span data-stu-id="42ff5-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="42ff5-149">Cuando un control establece la marca DT_SET_IMMEDIATE, afecta los cambios en su valor tomar tan pronto como el usuario se mueve a un nuevo control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="42ff5-150">MAPI realiza una única llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la interfaz de la propiedad para la propiedad del control.</span><span class="sxs-lookup"><span data-stu-id="42ff5-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="42ff5-151">Esto es diferente del comportamiento predeterminado, que es posponer la necesidad de los cambios realizados en los valores de control tendrán efecto hasta después de que el usuario selecciona el botón **Aceptar** o cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42ff5-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="42ff5-152">El indicador DT_SET_IMMEDIATE a menudo se usa en combinación con las notificaciones de tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="42ff5-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="42ff5-153">En la siguiente tabla se enumera los tipos de controles y todos los valores de indicador que se pueden establecer para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="42ff5-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="42ff5-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="42ff5-154">**Control**</span></span>|<span data-ttu-id="42ff5-155">**Valores válidos para esta propiedad**</span><span class="sxs-lookup"><span data-stu-id="42ff5-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42ff5-156">Botón</span><span class="sxs-lookup"><span data-stu-id="42ff5-156">Button</span></span>  <br/> |<span data-ttu-id="42ff5-157">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-158">Casilla</span><span class="sxs-lookup"><span data-stu-id="42ff5-158">Check box</span></span>  <br/> |<span data-ttu-id="42ff5-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="42ff5-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="42ff5-160">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="42ff5-160">Combo box</span></span>  <br/> |<span data-ttu-id="42ff5-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="42ff5-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="42ff5-162">Cuadro de lista desplegable</span><span class="sxs-lookup"><span data-stu-id="42ff5-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="42ff5-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="42ff5-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="42ff5-164">Edit</span><span class="sxs-lookup"><span data-stu-id="42ff5-164">Edit</span></span>  <br/> |<span data-ttu-id="42ff5-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="42ff5-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="42ff5-166">Cuadro de grupo</span><span class="sxs-lookup"><span data-stu-id="42ff5-166">Group box</span></span>  <br/> |<span data-ttu-id="42ff5-167">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-168">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="42ff5-168">Label</span></span>  <br/> |<span data-ttu-id="42ff5-169">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-170">Cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="42ff5-170">List box</span></span>  <br/> |<span data-ttu-id="42ff5-171">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-172">Cuadro de lista desplegable con varios valores</span><span class="sxs-lookup"><span data-stu-id="42ff5-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="42ff5-173">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-174">Cuadro de lista con varios valores</span><span class="sxs-lookup"><span data-stu-id="42ff5-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="42ff5-175">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-176">Página con fichas</span><span class="sxs-lookup"><span data-stu-id="42ff5-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="42ff5-177">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="42ff5-178">Botón de opción</span><span class="sxs-lookup"><span data-stu-id="42ff5-178">Radio button</span></span>  <br/> |<span data-ttu-id="42ff5-179">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="42ff5-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="42ff5-180">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="42ff5-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="42ff5-181">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="42ff5-181">Header files</span></span>

<span data-ttu-id="42ff5-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42ff5-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="42ff5-183">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="42ff5-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="42ff5-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="42ff5-184">Mapitags.h</span></span>
  
> <span data-ttu-id="42ff5-185">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="42ff5-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42ff5-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="42ff5-186">See also</span></span>



[<span data-ttu-id="42ff5-187">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="42ff5-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42ff5-188">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="42ff5-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42ff5-189">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="42ff5-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42ff5-190">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="42ff5-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

