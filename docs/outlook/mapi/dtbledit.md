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
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816734"
---
# <a name="dtbledit"></a><span data-ttu-id="d141f-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="d141f-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="d141f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d141f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d141f-105">Describe un control de edición que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="d141f-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d141f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d141f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d141f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d141f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d141f-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="d141f-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="d141f-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="d141f-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="d141f-110">Members</span><span class="sxs-lookup"><span data-stu-id="d141f-110">Members</span></span>

 <span data-ttu-id="d141f-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="d141f-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="d141f-112">Un desplazamiento desde el comienzo de la estructura **DTBLEDIT** a un filtro de cadena de caracteres que se describe las restricciones, si hay alguno, para los caracteres que se pueden escribir en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="d141f-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="d141f-113">El filtro no se interpreta como una expresión regular y el mismo filtro se aplica a todos los caracteres que ha escrito.</span><span class="sxs-lookup"><span data-stu-id="d141f-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="d141f-114">El formato del filtro es como sigue:</span><span class="sxs-lookup"><span data-stu-id="d141f-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="d141f-115">**Carácter**</span><span class="sxs-lookup"><span data-stu-id="d141f-115">**Character**</span></span>|<span data-ttu-id="d141f-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d141f-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="d141f-117">Se permite cualquier carácter (por ejemplo, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="d141f-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="d141f-118">Define un conjunto de caracteres (por ejemplo, `"[0123456789]".`)</span><span class="sxs-lookup"><span data-stu-id="d141f-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="d141f-119">Indica un intervalo de caracteres (por ejemplo, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="d141f-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="d141f-120">Indica que no se permiten estos caracteres (por ejemplo, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="d141f-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="d141f-121">Utilizada para entrecomillar cualquiera de los símbolos anteriores (por ejemplo, `"[\-\\\[\]]"` significa-, \, [, y] se permiten caracteres).</span><span class="sxs-lookup"><span data-stu-id="d141f-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="d141f-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d141f-122">**ulFlags**</span></span>
  
> <span data-ttu-id="d141f-123">Máscara de bits de indicadores que se utilizan para designar el formato del filtro de carácter.</span><span class="sxs-lookup"><span data-stu-id="d141f-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="d141f-124">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="d141f-124">The following flag can be set:</span></span>
    
<span data-ttu-id="d141f-125">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d141f-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d141f-126">El filtro está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d141f-126">The filter is in Unicode format.</span></span> <span data-ttu-id="d141f-127">Si no está establecido el indicador MAPI_UNICODE., el filtro está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d141f-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="d141f-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="d141f-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="d141f-129">Número máximo de caracteres que el usuario puede escribir en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="d141f-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="d141f-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="d141f-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="d141f-131">Etiqueta de propiedad de una propiedad de tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="d141f-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="d141f-132">El miembro **ulPropTag** identifica la propiedad de cadena cuyos datos se muestran y se modifica en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="d141f-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d141f-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d141f-133">Remarks</span></span>

<span data-ttu-id="d141f-134">Una estructura **DTBLEDIT** describe un control de edición en un cuadro de diálogo que contiene información alfanumérico un área.</span><span class="sxs-lookup"><span data-stu-id="d141f-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="d141f-135">Casi todos los cuadros de diálogo tienen control de edición al menos uno.</span><span class="sxs-lookup"><span data-stu-id="d141f-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="d141f-136">Controles de edición pueden ser modificable por un usuario o de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d141f-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="d141f-137">Controles de edición también pueden ser única línea o multiline.</span><span class="sxs-lookup"><span data-stu-id="d141f-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="d141f-138">Controles de edición de múltiples líneas suelen tener una barra de desplazamiento asociada a ellos.</span><span class="sxs-lookup"><span data-stu-id="d141f-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="d141f-139">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d141f-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="d141f-140">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="d141f-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d141f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d141f-141">See also</span></span>



[<span data-ttu-id="d141f-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="d141f-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="d141f-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d141f-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d141f-144">Propiedad canónica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="d141f-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="d141f-145">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d141f-145">MAPI Structures</span></span>](mapi-structures.md)

