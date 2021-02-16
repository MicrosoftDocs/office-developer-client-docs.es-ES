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
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="2dfa4-103">Propiedad canónica PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="2dfa4-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="2dfa4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dfa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dfa4-105">Contiene una máscara de bits de marcas que rigen el comportamiento de un control usado en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2dfa4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2dfa4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2dfa4-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2dfa4-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="2dfa4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2dfa4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2dfa4-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="2dfa4-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="2dfa4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2dfa4-110">Data type:</span></span>  <br/> |<span data-ttu-id="2dfa4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2dfa4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2dfa4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2dfa4-112">Area:</span></span>  <br/> |<span data-ttu-id="2dfa4-113">Tabla para mostrar MAPI</span><span class="sxs-lookup"><span data-stu-id="2dfa4-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dfa4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2dfa4-114">Remarks</span></span>

<span data-ttu-id="2dfa4-115">Se pueden establecer una o varias de las siguientes marcas para esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="2dfa4-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="2dfa4-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="2dfa4-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="2dfa4-117">El control puede tener Double-Byte juego de caracteres (DBCS) en él.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="2dfa4-118">Esta marca se usa con controles de edición.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-118">This flag is used with edit controls.</span></span> <span data-ttu-id="2dfa4-119">Permite juegos de caracteres de varios bytes.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="2dfa4-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="2dfa4-121">El control se puede editar; se puede cambiar el valor asociado con el control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="2dfa4-122">Cuando no se establece esta marca, el control es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="2dfa4-123">Este valor se omite en los controles de etiqueta, cuadro de grupo, botón de inserción estándar, cuadro de lista desplegable multivalor y cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="2dfa4-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="2dfa4-125">El control de edición puede contener varias líneas.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="2dfa4-126">Esto significa que se puede especificar un carácter devuelto dentro del control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="2dfa4-127">Esta marca solo es válida para controles de edición.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="2dfa4-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="2dfa4-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="2dfa4-129">Se aplica a controles de edición.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-129">Applies to edit controls.</span></span> <span data-ttu-id="2dfa4-130">El control de edición se trata como una contraseña.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-130">The edit control is treated like a password.</span></span> <span data-ttu-id="2dfa4-131">El valor se muestra con asteriscos en lugar de hacer eco de los caracteres reales especificados.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="2dfa4-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="2dfa4-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="2dfa4-133">Si el control permite cambios (DT_EDITABLE), debe tener un valor antes de llamar a [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="2dfa4-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="2dfa4-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="2dfa4-135">Habilita la configuración inmediata de un valor; Tan pronto como cambia un valor en el control, MAPI llama al **método SetProps** para la propiedad asociada con ese control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="2dfa4-136">Cuando no se establece esta marca, los valores se establecen cuando se descarta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="2dfa4-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="2dfa4-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="2dfa4-138">Cuando se realiza una selección dentro del cuadro de lista, la columna de índice de ese cuadro de lista se establece como una propiedad.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="2dfa4-139">Siempre se usa con DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="2dfa4-140">Esta propiedad se almacena en el miembro ulCtlFlags de la estructura [DTCTL](dtctl.md) de un control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="2dfa4-141">La mayoría de las marcas de control se aplican a todos los controles que permiten la entrada del usuario; algunos se aplican solo al control de edición.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="2dfa4-142">Los controles que no permiten la entrada del usuario, como un botón o una etiqueta, establecen 0 para sus marcas de control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="2dfa4-143">Muchos de los valores de marca se explican por sí solos.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="2dfa4-144">Por ejemplo, cuando DT_REQUIRED para un control, debe contener un valor antes de que se pueda descartar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="2dfa4-145">El proveedor de servicios puede proporcionar un valor a través de su **implementación IMAPIProp** o el usuario puede escribir uno.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="2dfa4-146">DT_EDITABLE indica que se puede modificar el valor del control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="2dfa4-147">DT_MULTILINE permite que el valor de un control de edición abarque varias líneas.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="2dfa4-148">Algunas marcas de control no son tan obvias en su significado.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="2dfa4-149">Cuando un control establece DT_SET_IMMEDIATE marca, cualquier cambio en su valor tendrá efecto en cuanto el usuario se mueva a un nuevo control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="2dfa4-150">MAPI realiza una sola llamada al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la interfaz de propiedades para la propiedad del control.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="2dfa4-151">Esto es diferente del comportamiento predeterminado, que es posponer que los cambios  en los valores de control tengan efecto hasta que el usuario selecciona el botón Aceptar o descarta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="2dfa4-152">La DT_SET_IMMEDIATE se usa a menudo en combinación con las notificaciones de la tabla de visualización.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="2dfa4-153">En la tabla siguiente se enumeran los tipos de controles y todos los valores de marca que se pueden establecer para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="2dfa4-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="2dfa4-154">**Control**</span></span>|<span data-ttu-id="2dfa4-155">**Valores válidos para esta propiedad**</span><span class="sxs-lookup"><span data-stu-id="2dfa4-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dfa4-156">Botón</span><span class="sxs-lookup"><span data-stu-id="2dfa4-156">Button</span></span>  <br/> |<span data-ttu-id="2dfa4-157">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-158">Casilla</span><span class="sxs-lookup"><span data-stu-id="2dfa4-158">Check box</span></span>  <br/> |<span data-ttu-id="2dfa4-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="2dfa4-160">Cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="2dfa4-160">Combo box</span></span>  <br/> |<span data-ttu-id="2dfa4-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="2dfa4-162">Cuadro de lista desplegable</span><span class="sxs-lookup"><span data-stu-id="2dfa4-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="2dfa4-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="2dfa4-164">Editar</span><span class="sxs-lookup"><span data-stu-id="2dfa4-164">Edit</span></span>  <br/> |<span data-ttu-id="2dfa4-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="2dfa4-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="2dfa4-166">Cuadro de grupo</span><span class="sxs-lookup"><span data-stu-id="2dfa4-166">Group box</span></span>  <br/> |<span data-ttu-id="2dfa4-167">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-168">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2dfa4-168">Label</span></span>  <br/> |<span data-ttu-id="2dfa4-169">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-170">Cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="2dfa4-170">List box</span></span>  <br/> |<span data-ttu-id="2dfa4-171">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-172">Cuadro de lista desplegable con varios valores</span><span class="sxs-lookup"><span data-stu-id="2dfa4-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="2dfa4-173">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-174">Cuadro de lista de varios valores</span><span class="sxs-lookup"><span data-stu-id="2dfa4-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="2dfa4-175">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-176">Página con pestañas</span><span class="sxs-lookup"><span data-stu-id="2dfa4-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="2dfa4-177">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="2dfa4-178">Botón de radio</span><span class="sxs-lookup"><span data-stu-id="2dfa4-178">Radio button</span></span>  <br/> |<span data-ttu-id="2dfa4-179">Debe ser cero</span><span class="sxs-lookup"><span data-stu-id="2dfa4-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="2dfa4-180">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2dfa4-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2dfa4-181">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2dfa4-181">Header files</span></span>

<span data-ttu-id="2dfa4-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2dfa4-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="2dfa4-183">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="2dfa4-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2dfa4-184">Mapitags.h</span></span>
  
> <span data-ttu-id="2dfa4-185">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2dfa4-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2dfa4-186">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2dfa4-186">See also</span></span>



[<span data-ttu-id="2dfa4-187">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2dfa4-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2dfa4-188">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2dfa4-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2dfa4-189">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2dfa4-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2dfa4-190">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2dfa4-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

