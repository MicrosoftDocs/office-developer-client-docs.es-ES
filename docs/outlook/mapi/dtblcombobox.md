---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287471"
---
# <a name="dtblcombobox"></a><span data-ttu-id="96b58-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="96b58-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="96b58-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96b58-105">Describe un control de cuadro combinado que se utilizará en un cuadro de diálogo generado a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="96b58-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96b58-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="96b58-106">Header file:</span></span>  <br/> |<span data-ttu-id="96b58-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="96b58-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="96b58-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="96b58-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="96b58-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="96b58-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a><span data-ttu-id="96b58-110">Members</span><span class="sxs-lookup"><span data-stu-id="96b58-110">Members</span></span>

 <span data-ttu-id="96b58-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="96b58-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="96b58-112">Un desplazamiento desde el principio de la estructura **DTBLCOMBOBOX** a un filtro de cadena de caracteres que describe las restricciones, si las hay, a los caracteres que se pueden escribir en el control de edición del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="96b58-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="96b58-113">El filtro no se interpreta como una expresión regular y se aplica el mismo filtro a todos los caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="96b58-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="96b58-114">El formato del filtro es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="96b58-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="96b58-115">**Carácter**</span><span class="sxs-lookup"><span data-stu-id="96b58-115">**Character**</span></span>|<span data-ttu-id="96b58-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96b58-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="96b58-117">Se permite cualquier carácter (por ejemplo, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="96b58-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="96b58-118">Define un conjunto de caracteres (por ejemplo, `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="96b58-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="96b58-119">Indica un intervalo de caracteres (por ejemplo, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="96b58-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="96b58-120">Indica que estos caracteres no están permitidos.</span><span class="sxs-lookup"><span data-stu-id="96b58-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="96b58-121">(por ejemplo, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="96b58-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="96b58-122">Se usa para cotizar cualquiera de los símbolos anteriores (por `"[\-\\\[\]]"` ejemplo, los \, caracteres significados-, [y]).</span><span class="sxs-lookup"><span data-stu-id="96b58-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="96b58-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="96b58-123">**ulFlags**</span></span>
  
> <span data-ttu-id="96b58-124">Máscara de caracteres de marcas usada para designar el formato del filtro de la cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="96b58-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="96b58-125">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="96b58-125">The following flag can be set:</span></span>
    
<span data-ttu-id="96b58-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="96b58-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="96b58-127">El filtro está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="96b58-127">The filter is in Unicode format.</span></span> <span data-ttu-id="96b58-128">Si no se establece la marca MAPI_UNICODE, el filtro está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="96b58-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="96b58-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="96b58-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="96b58-130">Número máximo de caracteres que se pueden escribir en el cuadro de texto del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="96b58-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="96b58-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="96b58-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="96b58-132">Etiqueta de propiedad de una propiedad de tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="96b58-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="96b58-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="96b58-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="96b58-134">Etiqueta de propiedad de una propiedad de tipo PT Object en la que se puede abrir una interfaz **IMAPITable** mediante una llamada de **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="96b58-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="96b58-135">La tabla debe tener una columna con una propiedad que sea del mismo tipo que la propiedad identificada por el miembro **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="96b58-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="96b58-136">Las filas de la tabla se usan para rellenar la lista.</span><span class="sxs-lookup"><span data-stu-id="96b58-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="96b58-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96b58-137">Remarks</span></span>

<span data-ttu-id="96b58-138">Una estructura **DTBLCOMBOBOX** describe un cuadro combinado que contiene un control List y un campo de selección.</span><span class="sxs-lookup"><span data-stu-id="96b58-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="96b58-139">La lista presenta la información que el usuario puede seleccionar y el campo de selección muestra la selección actual.</span><span class="sxs-lookup"><span data-stu-id="96b58-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="96b58-140">El campo de selección es un control de edición que también se puede usar para escribir texto que todavía no está en la lista.</span><span class="sxs-lookup"><span data-stu-id="96b58-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="96b58-141">Los dos miembros de la etiqueta de propiedad funcionan conjuntamente para coordinar la presentación de la lista con el control de edición.</span><span class="sxs-lookup"><span data-stu-id="96b58-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="96b58-142">Cuando MAPI muestra el cuadro combinado por primera vez, llama al método **OpenProperty** de la implementación de **IMAPIProp** asociada a la tabla de presentación para recuperar la tabla representada por el miembro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="96b58-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="96b58-143">Esta tabla tiene una columna con una columna que contiene valores para la propiedad representada por el miembro **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="96b58-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="96b58-144">Por lo tanto, esta columna debe ser del mismo tipo que la propiedad **ulPRPropertyName** y ambas columnas deben ser cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="96b58-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="96b58-145">Los valores de la columna se muestran en la sección de lista del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="96b58-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="96b58-146">Por lo tanto, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no es una etiqueta de propiedad válida para **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="96b58-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="96b58-147">Cuando un usuario selecciona una de las filas o escribe nuevos datos en el cuadro de texto, la propiedad **ulPRPropertyName** se establece en el valor seleccionado o escrito.</span><span class="sxs-lookup"><span data-stu-id="96b58-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="96b58-148">Para mostrar un valor inicial para el control de edición, MAPI llama a [IMAPIProp:: GetProps](imapiprop-getprops.md) para recuperar los valores de propiedad de la tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="96b58-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="96b58-149">Si una de las propiedades recuperadas coincide con la propiedad que representa el miembro **ulPRPropertyName** , su valor pasa a ser el valor inicial.</span><span class="sxs-lookup"><span data-stu-id="96b58-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="96b58-150">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="96b58-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="96b58-151">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="96b58-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96b58-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="96b58-152">See also</span></span>



[<span data-ttu-id="96b58-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="96b58-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="96b58-154">Propiedad canónica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="96b58-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="96b58-155">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="96b58-155">MAPI Structures</span></span>](mapi-structures.md)

