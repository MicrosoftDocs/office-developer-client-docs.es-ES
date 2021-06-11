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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406979"
---
# <a name="dtblcombobox"></a><span data-ttu-id="e254c-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="e254c-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="e254c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e254c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e254c-105">Describe un control de cuadro combinado que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e254c-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e254c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e254c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e254c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e254c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e254c-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="e254c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="e254c-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="e254c-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
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

## <a name="members"></a><span data-ttu-id="e254c-110">Members</span><span class="sxs-lookup"><span data-stu-id="e254c-110">Members</span></span>

 <span data-ttu-id="e254c-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="e254c-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="e254c-112">Desplazamiento desde el inicio de la estructura **DTBLCOMBOBOX** a un filtro de cadena de caracteres que describe restricciones, si las hay, a los caracteres que se pueden especificar en el control de edición del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e254c-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="e254c-113">El filtro no se interpreta como una expresión regular y el mismo filtro se aplica a todos los caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="e254c-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="e254c-114">El formato del filtro es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="e254c-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="e254c-115">**Carácter**</span><span class="sxs-lookup"><span data-stu-id="e254c-115">**Character**</span></span>|<span data-ttu-id="e254c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e254c-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="e254c-117">Se permite cualquier carácter (por ejemplo,  `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="e254c-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="e254c-118">Define un conjunto de caracteres (por ejemplo,  `"[0123456789]"` ).</span><span class="sxs-lookup"><span data-stu-id="e254c-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="e254c-119">Indica un intervalo de caracteres (por ejemplo,  `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="e254c-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="e254c-120">Indica que estos caracteres no están permitidos.</span><span class="sxs-lookup"><span data-stu-id="e254c-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="e254c-121">(por ejemplo,  `"[~0-9]"` ).</span><span class="sxs-lookup"><span data-stu-id="e254c-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="e254c-122">Se usa para citar cualquiera de los símbolos anteriores (por ejemplo, se permiten los caracteres  `"[\-\\\[\]]"` -, \, [y ] ).</span><span class="sxs-lookup"><span data-stu-id="e254c-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="e254c-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e254c-123">**ulFlags**</span></span>
  
> <span data-ttu-id="e254c-124">Máscara de bits de marcas usadas para designar el formato del filtro de cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e254c-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="e254c-125">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="e254c-125">The following flag can be set:</span></span>
    
<span data-ttu-id="e254c-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e254c-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e254c-127">El filtro está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e254c-127">The filter is in Unicode format.</span></span> <span data-ttu-id="e254c-128">Si la MAPI_UNICODE no está establecida, el filtro está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e254c-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="e254c-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="e254c-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="e254c-130">Número máximo de caracteres que se pueden especificar en el cuadro de texto del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e254c-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="e254c-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="e254c-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="e254c-132">Etiqueta de propiedad para una propiedad de tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e254c-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="e254c-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="e254c-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="e254c-134">Etiqueta de propiedad para una propiedad de tipo PT_OBJECT en la que se puede abrir una interfaz **IMAPITable** mediante una **llamada OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="e254c-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="e254c-135">La tabla debe tener una columna con una propiedad que sea del mismo tipo que la propiedad identificada por el **miembro ulPRPropertyName.**</span><span class="sxs-lookup"><span data-stu-id="e254c-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="e254c-136">Las filas de la tabla se usan para rellenar la lista.</span><span class="sxs-lookup"><span data-stu-id="e254c-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e254c-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e254c-137">Remarks</span></span>

<span data-ttu-id="e254c-138">Una **estructura DTBLCOMBOBOX** describe un cuadro combinado un control que consta de una lista y un campo de selección.</span><span class="sxs-lookup"><span data-stu-id="e254c-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="e254c-139">La lista presenta la información desde la que un usuario puede seleccionar y el campo de selección muestra la selección actual.</span><span class="sxs-lookup"><span data-stu-id="e254c-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="e254c-140">El campo de selección es un control de edición que también se puede usar para escribir texto que aún no esté en la lista.</span><span class="sxs-lookup"><span data-stu-id="e254c-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="e254c-141">Los dos miembros de la etiqueta de propiedad trabajan juntos para coordinar la presentación de la lista con el control de edición.</span><span class="sxs-lookup"><span data-stu-id="e254c-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="e254c-142">Cuando MAPI muestra por primera vez el cuadro combinado, llama al método **OpenProperty** de la implementación **IMAPIProp** asociada a la tabla para mostrar para recuperar la tabla representada por el **miembro ulPRTableName.**</span><span class="sxs-lookup"><span data-stu-id="e254c-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="e254c-143">Esta tabla tiene una columna que contiene valores para la propiedad representada por el **miembro ulPRPropertyName.**</span><span class="sxs-lookup"><span data-stu-id="e254c-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="e254c-144">Por lo tanto, esta columna debe ser del mismo tipo que la **propiedad ulPRPropertyName** y ambas columnas deben ser cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e254c-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="e254c-145">Los valores de la columna se muestran en la sección de lista del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e254c-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="e254c-146">Por lo **tanto, PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) no es una etiqueta de propiedad válida para **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="e254c-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="e254c-147">Cuando un usuario selecciona una de las filas o escribe nuevos datos en el cuadro de texto, la propiedad **ulPRPropertyName** se establece en el valor seleccionado o especificado.</span><span class="sxs-lookup"><span data-stu-id="e254c-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="e254c-148">Para mostrar un valor inicial para el control de edición, MAPI llama a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar los valores de propiedad de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e254c-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="e254c-149">Si una de las propiedades recuperadas coincide con la propiedad representada por el **miembro ulPRPropertyName,** su valor se convierte en el valor inicial.</span><span class="sxs-lookup"><span data-stu-id="e254c-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="e254c-150">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="e254c-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e254c-151">Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e254c-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e254c-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e254c-152">See also</span></span>



[<span data-ttu-id="e254c-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e254c-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="e254c-154">Propiedad canónica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="e254c-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="e254c-155">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e254c-155">MAPI Structures</span></span>](mapi-structures.md)

