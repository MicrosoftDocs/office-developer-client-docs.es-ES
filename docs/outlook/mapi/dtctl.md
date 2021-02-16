---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421504"
---
# <a name="dtctl"></a><span data-ttu-id="bf317-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="bf317-103">DTCTL</span></span>

<span data-ttu-id="bf317-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf317-105">Describe un control que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="bf317-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf317-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bf317-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf317-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf317-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a><span data-ttu-id="bf317-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf317-108">Members</span></span>

<span data-ttu-id="bf317-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="bf317-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="bf317-110">Tipo de control que se incluye en el miembro **ctl** y corresponde a la propiedad PR_CONTROL_TYPE **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) del control.</span><span class="sxs-lookup"><span data-stu-id="bf317-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="bf317-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf317-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="bf317-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="bf317-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="bf317-113">Control Etiqueta</span><span class="sxs-lookup"><span data-stu-id="bf317-113">Label control.</span></span>
    
<span data-ttu-id="bf317-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="bf317-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="bf317-115">Control de edición.</span><span class="sxs-lookup"><span data-stu-id="bf317-115">Edit control.</span></span>
    
<span data-ttu-id="bf317-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="bf317-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="bf317-117">Control cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="bf317-117">List box control.</span></span>
    
<span data-ttu-id="bf317-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="bf317-119">Control cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="bf317-119">Combo box control.</span></span>
    
<span data-ttu-id="bf317-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="bf317-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="bf317-121">Control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="bf317-121">Drop-down list control.</span></span>
    
<span data-ttu-id="bf317-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="bf317-123">Control casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="bf317-123">Check box control.</span></span>
    
<span data-ttu-id="bf317-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="bf317-125">Control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="bf317-125">Group box control.</span></span>
    
<span data-ttu-id="bf317-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="bf317-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="bf317-127">Control de botón.</span><span class="sxs-lookup"><span data-stu-id="bf317-127">Button control.</span></span>
    
<span data-ttu-id="bf317-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="bf317-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="bf317-129">Control de página con pestañas.</span><span class="sxs-lookup"><span data-stu-id="bf317-129">Tabbed page control.</span></span>
    
<span data-ttu-id="bf317-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="bf317-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="bf317-131">Control de botón de radio.</span><span class="sxs-lookup"><span data-stu-id="bf317-131">Radio button control.</span></span>
    
<span data-ttu-id="bf317-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="bf317-133">Control de lista de varios valores.</span><span class="sxs-lookup"><span data-stu-id="bf317-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="bf317-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="bf317-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="bf317-135">Control de lista desplegable de varios valores.</span><span class="sxs-lookup"><span data-stu-id="bf317-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="bf317-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="bf317-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="bf317-137">Máscara de bits de marcas que describe las características del control y corresponde a la propiedad PR_CONTROL_FLAGS **(** [PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) del control.</span><span class="sxs-lookup"><span data-stu-id="bf317-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="bf317-138">Estas marcas solo se pueden establecer para casillas de verificación, cuadros combinados, cuadros de lista y controles de edición.</span><span class="sxs-lookup"><span data-stu-id="bf317-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="bf317-139">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf317-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="bf317-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="bf317-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="bf317-141">Se acepta el formato ANSI o DBCS.</span><span class="sxs-lookup"><span data-stu-id="bf317-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="bf317-142">Esta marca solo es válida para controles de edición.</span><span class="sxs-lookup"><span data-stu-id="bf317-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="bf317-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="bf317-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="bf317-144">Un usuario puede modificar el texto del control.</span><span class="sxs-lookup"><span data-stu-id="bf317-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="bf317-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="bf317-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="bf317-146">El control puede contener varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="bf317-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="bf317-147">Esta marca solo es válida para controles de edición.</span><span class="sxs-lookup"><span data-stu-id="bf317-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="bf317-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="bf317-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="bf317-149">El control contiene una contraseña; por lo tanto, el contenido del control no debe mostrarse al usuario.</span><span class="sxs-lookup"><span data-stu-id="bf317-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="bf317-150">Esta marca solo es válida para controles de edición.</span><span class="sxs-lookup"><span data-stu-id="bf317-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="bf317-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="bf317-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="bf317-152">El control de cuadro de diálogo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bf317-152">The dialog box control is required.</span></span> <span data-ttu-id="bf317-153">Esta marca solo es válida para controles de edición y cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="bf317-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="bf317-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="bf317-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="bf317-155">Habilita la salida inmediata de un valor tras un cambio en el control.</span><span class="sxs-lookup"><span data-stu-id="bf317-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="bf317-156">Esto permite establecer una relación de dependencia entre dos controles.</span><span class="sxs-lookup"><span data-stu-id="bf317-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="bf317-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="bf317-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="bf317-158">Puntero a una estructura que consta de una [estructura GUID,](guid.md) para representar el proveedor de servicios y un identificador para el control.</span><span class="sxs-lookup"><span data-stu-id="bf317-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="bf317-159">Los **miembros lpbNotif** y **cbNotif** corresponden a la propiedad PR_CONTROL_ID ([PidTagControlId](pidtagcontrolid-canonical-property.md)) del control y se usan para notificar **a** la interfaz de usuario cuándo debe actualizarse el control.</span><span class="sxs-lookup"><span data-stu-id="bf317-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="bf317-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="bf317-160">**cbNotif**</span></span>
  
> <span data-ttu-id="bf317-161">Recuento de bytes en la estructura a la que apunta el **miembro lpbNotif.**</span><span class="sxs-lookup"><span data-stu-id="bf317-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="bf317-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="bf317-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="bf317-163">Puntero a una cadena de caracteres que describe los caracteres que se pueden introducir en un control de edición o cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="bf317-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="bf317-164">Para otros tipos de controles, el **miembro lpszFilter** puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="bf317-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="bf317-165">Para los controles de edición y cuadro combinado, debe ser una expresión regular que se aplique a un solo carácter a la vez.</span><span class="sxs-lookup"><span data-stu-id="bf317-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="bf317-166">Se aplica el mismo filtro a todos los caracteres del control.</span><span class="sxs-lookup"><span data-stu-id="bf317-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="bf317-167">El formato de la cadena de filtro es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf317-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="bf317-168">**Carácter**</span><span class="sxs-lookup"><span data-stu-id="bf317-168">**Character**</span></span>|<span data-ttu-id="bf317-169">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf317-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="bf317-170">Se permite cualquier carácter (por ejemplo, `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="bf317-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="bf317-171">Define un conjunto de caracteres (por ejemplo, `"[0123456789]"` .)</span><span class="sxs-lookup"><span data-stu-id="bf317-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="bf317-172">Indica un intervalo de caracteres (por ejemplo, `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="bf317-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="bf317-173">Indica que no se permiten estos caracteres (por ejemplo, `"[~0-9]")` .</span><span class="sxs-lookup"><span data-stu-id="bf317-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="bf317-174">Se usa para citar cualquiera de los símbolos anteriores (por ejemplo, se permiten los caracteres `"[\-\\\[\]]"` -, \, [y ]).</span><span class="sxs-lookup"><span data-stu-id="bf317-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="bf317-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="bf317-175">**ulItemID**</span></span>
  
> <span data-ttu-id="bf317-176">Valor que identifica el control en el recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf317-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="bf317-177">Para controles de páginas con pestañas de tipo DTCT_PAGE el **miembro ulItemID** se usa opcionalmente para cargar el nombre del componente de la página desde un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="bf317-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="bf317-178">La información de posición y etiqueta se lee en el recurso del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bf317-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="bf317-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="bf317-179">**ctl**</span></span>
  
> <span data-ttu-id="bf317-180">Estructura que contiene los datos del control y que corresponde a la propiedad PR_CONTROL_STRUCTURE **del** control ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bf317-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="bf317-181">Cada tipo de control tiene una estructura diferente.</span><span class="sxs-lookup"><span data-stu-id="bf317-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf317-182">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf317-182">Remarks</span></span>

<span data-ttu-id="bf317-183">La **estructura DTCTL** describe un control de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="bf317-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="bf317-184">La mayoría de sus miembros se usan para establecer propiedades en el control.</span><span class="sxs-lookup"><span data-stu-id="bf317-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="bf317-185">El **miembro ctl** es una unión de estructuras relacionadas con un tipo determinado de control.</span><span class="sxs-lookup"><span data-stu-id="bf317-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="bf317-186">Si la **estructura DTCTL** describe un control de edición, por ejemplo, el miembro **ctl** apuntará a una [estructura DTBLEDIT.](dtbledit.md)</span><span class="sxs-lookup"><span data-stu-id="bf317-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="bf317-187">Esta estructura corresponde a la propiedad PR_CONTROL_STRUCTURE **control.**</span><span class="sxs-lookup"><span data-stu-id="bf317-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="bf317-188">La unión tiene como primer miembro una variable de tipo LPVOID para permitir la inicialización en tiempo de compilación de la **estructura DTCTL.**</span><span class="sxs-lookup"><span data-stu-id="bf317-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="bf317-189">Aunque la [función BuildDisplayTable](builddisplaytable.md) usa la estructura **DTCTL** para crear la tabla de visualización a partir de recursos de control, la estructura **DTCTL** nunca aparece en la propia tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="bf317-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="bf317-190">Esta estructura simplemente proporciona información a **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="bf317-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="bf317-191">En el **miembro ulCtlFlags,** cuatro marcas DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT sólo afectan a los controles de edición.</span><span class="sxs-lookup"><span data-stu-id="bf317-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="bf317-192">Otros dos DT_REQUIRED y DT_SET_IMMEDIATE a cualquier control editable.</span><span class="sxs-lookup"><span data-stu-id="bf317-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="bf317-193">Los controles disponibles para un cuadro de diálogo son etiqueta, cuadro de texto, cuadro de texto para entrada de lápiz, lista, lista desplegable, cuadro combinado, casilla, cuadro de grupo, botón, botón de radio y página con pestañas.</span><span class="sxs-lookup"><span data-stu-id="bf317-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="bf317-194">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="bf317-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="bf317-195">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="bf317-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf317-196">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf317-196">See also</span></span>

- [<span data-ttu-id="bf317-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="bf317-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="bf317-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="bf317-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="bf317-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="bf317-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="bf317-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="bf317-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="bf317-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="bf317-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="bf317-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="bf317-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="bf317-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="bf317-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="bf317-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="bf317-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="bf317-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="bf317-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="bf317-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="bf317-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="bf317-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="bf317-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="bf317-210">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="bf317-210">MAPI Structures</span></span>](mapi-structures.md)

