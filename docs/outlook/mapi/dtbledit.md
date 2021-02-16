---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404683"
---
# <a name="dtbledit"></a><span data-ttu-id="54c52-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="54c52-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="54c52-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54c52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54c52-105">Describe un control de edición que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="54c52-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54c52-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="54c52-106">Header file:</span></span>  <br/> |<span data-ttu-id="54c52-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54c52-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="54c52-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="54c52-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="54c52-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="54c52-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="54c52-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="54c52-110">Members</span></span>

 <span data-ttu-id="54c52-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="54c52-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="54c52-112">Desplazamiento desde el principio de la estructura **DTBLEDIT** a un filtro de cadena de caracteres que describe las restricciones, si las hay, a los caracteres que se pueden introducir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="54c52-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="54c52-113">El filtro no se interpreta como una expresión regular y se aplica el mismo filtro a todos los caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="54c52-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="54c52-114">El formato del filtro es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="54c52-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="54c52-115">**Carácter**</span><span class="sxs-lookup"><span data-stu-id="54c52-115">**Character**</span></span>|<span data-ttu-id="54c52-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54c52-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="54c52-117">Se permite cualquier carácter (por ejemplo,  `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="54c52-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="54c52-118">Define un conjunto de caracteres (por ejemplo,  `"[0123456789]".` )</span><span class="sxs-lookup"><span data-stu-id="54c52-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="54c52-119">Indica un intervalo de caracteres (por ejemplo,  `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="54c52-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="54c52-120">Indica que estos caracteres no están permitidos (por ejemplo,  `"[~0-9]"` ).</span><span class="sxs-lookup"><span data-stu-id="54c52-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="54c52-121">Se usa para citar cualquiera de los símbolos anteriores (por ejemplo, se permiten los caracteres  `"[\-\\\[\]]"` -, \, [y ]).</span><span class="sxs-lookup"><span data-stu-id="54c52-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="54c52-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="54c52-122">**ulFlags**</span></span>
  
> <span data-ttu-id="54c52-123">Máscara de bits de marcas usadas para designar el formato del filtro de caracteres.</span><span class="sxs-lookup"><span data-stu-id="54c52-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="54c52-124">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="54c52-124">The following flag can be set:</span></span>
    
<span data-ttu-id="54c52-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54c52-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="54c52-126">El filtro está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="54c52-126">The filter is in Unicode format.</span></span> <span data-ttu-id="54c52-127">Si no MAPI_UNICODE marca, el filtro está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="54c52-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="54c52-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="54c52-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="54c52-129">Número máximo de caracteres que el usuario puede escribir en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="54c52-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="54c52-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="54c52-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="54c52-131">Etiqueta de propiedad para una propiedad de tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="54c52-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="54c52-132">El **miembro ulPropTag** identifica la propiedad de cadena cuyos datos se muestran y editan en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="54c52-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54c52-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54c52-133">Remarks</span></span>

<span data-ttu-id="54c52-134">Una **estructura DTBLEDIT** describe un control de edición en un área de un cuadro de diálogo que contiene información alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="54c52-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="54c52-135">Casi todos los cuadros de diálogo tienen al menos un control de edición.</span><span class="sxs-lookup"><span data-stu-id="54c52-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="54c52-136">Los controles de edición pueden ser modificables por un usuario o de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54c52-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="54c52-137">Los controles de edición también pueden ser de una sola línea o de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="54c52-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="54c52-138">Los controles de edición multilínea suelen tener asociada una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="54c52-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="54c52-139">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="54c52-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="54c52-140">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="54c52-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54c52-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="54c52-141">See also</span></span>



[<span data-ttu-id="54c52-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="54c52-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="54c52-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="54c52-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="54c52-144">Propiedad canónica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="54c52-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="54c52-145">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="54c52-145">MAPI Structures</span></span>](mapi-structures.md)

