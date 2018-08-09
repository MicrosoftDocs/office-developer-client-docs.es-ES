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
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816766"
---
# <a name="dtctl"></a><span data-ttu-id="760d5-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="760d5-103">DTCTL</span></span>

<span data-ttu-id="760d5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="760d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="760d5-105">Describe un control que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="760d5-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="760d5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="760d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="760d5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="760d5-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="760d5-108">Members</span><span class="sxs-lookup"><span data-stu-id="760d5-108">Members</span></span>

<span data-ttu-id="760d5-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="760d5-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="760d5-110">Tipo de control que se incluye en el miembro **ctl** y corresponde a la propiedad del control **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="760d5-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="760d5-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="760d5-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="760d5-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="760d5-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="760d5-113">Control Etiqueta</span><span class="sxs-lookup"><span data-stu-id="760d5-113">Label control.</span></span>
    
<span data-ttu-id="760d5-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="760d5-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="760d5-115">Control de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-115">Edit control.</span></span>
    
<span data-ttu-id="760d5-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="760d5-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="760d5-117">Control cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="760d5-117">List box control.</span></span>
    
<span data-ttu-id="760d5-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="760d5-119">Control de cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="760d5-119">Combo box control.</span></span>
    
<span data-ttu-id="760d5-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="760d5-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="760d5-121">Control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="760d5-121">Drop-down list control.</span></span>
    
<span data-ttu-id="760d5-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="760d5-123">Control de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="760d5-123">Check box control.</span></span>
    
<span data-ttu-id="760d5-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="760d5-125">Control de cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="760d5-125">Group box control.</span></span>
    
<span data-ttu-id="760d5-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="760d5-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="760d5-127">Control de botón.</span><span class="sxs-lookup"><span data-stu-id="760d5-127">Button control.</span></span>
    
<span data-ttu-id="760d5-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="760d5-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="760d5-129">Control de la página con fichas.</span><span class="sxs-lookup"><span data-stu-id="760d5-129">Tabbed page control.</span></span>
    
<span data-ttu-id="760d5-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="760d5-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="760d5-131">Control de botón de radio.</span><span class="sxs-lookup"><span data-stu-id="760d5-131">Radio button control.</span></span>
    
<span data-ttu-id="760d5-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="760d5-133">Control de lista con múltiples valores.</span><span class="sxs-lookup"><span data-stu-id="760d5-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="760d5-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="760d5-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="760d5-135">Control de lista desplegable con múltiples valores.</span><span class="sxs-lookup"><span data-stu-id="760d5-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="760d5-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="760d5-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="760d5-137">Máscara de bits de indicadores que se describe las características del control y se corresponde con la propiedad del control **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="760d5-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="760d5-138">Estas marcas se pueden establecer para las casillas de verificación, cuadros combinados, cuadros de lista y sólo controles de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="760d5-139">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="760d5-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="760d5-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="760d5-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="760d5-141">Se acepta el formato ANSI o DBCS.</span><span class="sxs-lookup"><span data-stu-id="760d5-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="760d5-142">Esta marca es válida para sólo controles de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="760d5-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="760d5-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="760d5-144">Un usuario puede modificar el texto en el control.</span><span class="sxs-lookup"><span data-stu-id="760d5-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="760d5-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="760d5-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="760d5-146">El control puede contener varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="760d5-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="760d5-147">Esta marca es válida para sólo controles de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="760d5-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="760d5-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="760d5-149">El control contiene una contraseña; por lo tanto, el contenido del control no debe mostrarse al usuario.</span><span class="sxs-lookup"><span data-stu-id="760d5-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="760d5-150">Esta marca es válida para sólo controles de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="760d5-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="760d5-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="760d5-152">Se requiere el control de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="760d5-152">The dialog box control is required.</span></span> <span data-ttu-id="760d5-153">Esta marca sólo es válida para los controles de cuadro combinado y de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="760d5-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="760d5-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="760d5-155">Habilita la salida inmediata de un valor tras un cambio en el control.</span><span class="sxs-lookup"><span data-stu-id="760d5-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="760d5-156">Esto permite una relación de dependencia entre dos controles.</span><span class="sxs-lookup"><span data-stu-id="760d5-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="760d5-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="760d5-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="760d5-158">Puntero a una estructura que consta de una estructura [GUID](guid.md) , para representar el proveedor de servicios y un identificador para el control.</span><span class="sxs-lookup"><span data-stu-id="760d5-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="760d5-159">Los miembros de **lpbNotif** y **cbNotif** se corresponden con la propiedad del control **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) y se usan para notificar a la interfaz de usuario cuando el control tiene que actualizar.</span><span class="sxs-lookup"><span data-stu-id="760d5-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="760d5-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="760d5-160">**cbNotif**</span></span>
  
> <span data-ttu-id="760d5-161">Recuento de bytes de la estructura que señala el miembro **lpbNotif** .</span><span class="sxs-lookup"><span data-stu-id="760d5-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="760d5-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="760d5-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="760d5-163">Puntero a una cadena de caracteres que se describe los caracteres que se puede introducir en un control de cuadro combinado o de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="760d5-164">Para otros tipos de controles, el miembro **lpszFilter** puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="760d5-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="760d5-165">Para los controles de cuadro combinado y de edición, debe ser una expresión regular que se aplica a un solo carácter a la vez.</span><span class="sxs-lookup"><span data-stu-id="760d5-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="760d5-166">El mismo filtro se aplica a todos los caracteres en el control.</span><span class="sxs-lookup"><span data-stu-id="760d5-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="760d5-167">El formato de la cadena de filtro es como sigue:</span><span class="sxs-lookup"><span data-stu-id="760d5-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="760d5-168">**Carácter**</span><span class="sxs-lookup"><span data-stu-id="760d5-168">**Character**</span></span>|<span data-ttu-id="760d5-169">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="760d5-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="760d5-170">Se permite cualquier carácter (por ejemplo, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="760d5-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="760d5-171">Define un conjunto de caracteres (por ejemplo, `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="760d5-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="760d5-172">Indica un intervalo de caracteres (por ejemplo, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="760d5-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="760d5-173">Indica que no se permiten estos caracteres (por ejemplo, `"[~0-9]")`.</span><span class="sxs-lookup"><span data-stu-id="760d5-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="760d5-174">Utilizada para entrecomillar cualquiera de los símbolos anteriores (por ejemplo, `"[\-\\\[\]]"` significa-, \, [, y] se permiten caracteres).</span><span class="sxs-lookup"><span data-stu-id="760d5-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="760d5-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="760d5-175">**ulItemID**</span></span>
  
> <span data-ttu-id="760d5-176">Valor que identifica el control en el recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="760d5-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="760d5-177">Para controles de páginas con fichas del tipo DTCT_PAGE la **ulItemID** miembro, opcionalmente, se utiliza para cargar el nombre del componente de la página desde un recurso de cadena.</span><span class="sxs-lookup"><span data-stu-id="760d5-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="760d5-178">Posición y la información de la etiqueta se leen desde el recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="760d5-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="760d5-179">**CTL**</span><span class="sxs-lookup"><span data-stu-id="760d5-179">**ctl**</span></span>
  
> <span data-ttu-id="760d5-180">Una estructura que contiene los datos para el control y se corresponde con la propiedad del control **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="760d5-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="760d5-181">Cada tipo de control tiene una estructura diferente.</span><span class="sxs-lookup"><span data-stu-id="760d5-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="760d5-182">Comentarios</span><span class="sxs-lookup"><span data-stu-id="760d5-182">Remarks</span></span>

<span data-ttu-id="760d5-183">La estructura **DTCTL** describe un control de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="760d5-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="760d5-184">La mayoría de sus miembros se usa para establecer las propiedades en el control.</span><span class="sxs-lookup"><span data-stu-id="760d5-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="760d5-185">El miembro **ctl** es la unión de las estructuras que se relacionan con un tipo concreto de control.</span><span class="sxs-lookup"><span data-stu-id="760d5-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="760d5-186">Si la estructura **DTCTL** que describe un control de edición, por ejemplo, el miembro **ctl** señalará a una estructura [DTBLEDIT](dtbledit.md) .</span><span class="sxs-lookup"><span data-stu-id="760d5-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="760d5-187">Esta estructura corresponde a la propiedad del control **PR_CONTROL_STRUCTURE** .</span><span class="sxs-lookup"><span data-stu-id="760d5-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="760d5-188">La unión tiene como su primer miembro de una variable de tipo LPVOID para permitir la inicialización en tiempo de compilación de la estructura **DTCTL** .</span><span class="sxs-lookup"><span data-stu-id="760d5-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="760d5-189">Aunque la función [BuildDisplayTable](builddisplaytable.md) utiliza la estructura **DTCTL** para la creación de la tabla para mostrar de los recursos de control, la estructura **DTCTL** nunca aparece en la propia tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="760d5-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="760d5-190">Esta estructura sólo suministra información a **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="760d5-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="760d5-191">En el miembro **ulCtlFlags** , cuatro indicadores DT_ACCEPT_DBCS, DT_EDITABLE, afectan al DT_MULTILINE_and DT_PASSWORD_EDIT de sólo controles de edición.</span><span class="sxs-lookup"><span data-stu-id="760d5-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="760d5-192">Otros dos DT_REQUIRED y DT_SET_IMMEDIATE afecta a cualquier control modificable.</span><span class="sxs-lookup"><span data-stu-id="760d5-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="760d5-193">Los controles disponibles para un cuadro de diálogo son etiqueta, cuadro de texto, cuadro de texto compatible con entrada de lápiz, lista, lista desplegable, cuadro combinado, casilla de verificación, cuadro de grupo, botón, botón de radio y página con fichas.</span><span class="sxs-lookup"><span data-stu-id="760d5-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="760d5-194">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="760d5-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="760d5-195">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="760d5-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="760d5-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="760d5-196">See also</span></span>

- [<span data-ttu-id="760d5-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="760d5-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="760d5-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="760d5-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="760d5-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="760d5-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="760d5-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="760d5-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="760d5-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="760d5-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="760d5-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="760d5-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="760d5-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="760d5-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="760d5-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="760d5-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="760d5-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="760d5-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="760d5-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="760d5-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="760d5-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="760d5-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="760d5-210">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="760d5-210">MAPI Structures</span></span>](mapi-structures.md)

