---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434602"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="16146-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="16146-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="16146-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16146-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16146-105">Describe un botón de radio que formará parte de un grupo de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="16146-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="16146-106">El grupo de botones de radio se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="16146-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16146-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="16146-107">Header file:</span></span>  <br/> |<span data-ttu-id="16146-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16146-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a><span data-ttu-id="16146-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="16146-109">Members</span></span>

 <span data-ttu-id="16146-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="16146-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="16146-111">Posición en la memoria de la etiqueta de cadena de caracteres del botón de radio.</span><span class="sxs-lookup"><span data-stu-id="16146-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="16146-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="16146-112">**ulFlags**</span></span>
  
> <span data-ttu-id="16146-113">Máscara de bits de marcas usadas para designar el formato de la etiqueta a la que apunta el **miembro ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="16146-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="16146-114">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="16146-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="16146-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16146-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="16146-116">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="16146-116">The label is in Unicode format.</span></span> <span data-ttu-id="16146-117">Si no MAPI_UNICODE marca, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="16146-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="16146-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="16146-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="16146-119">Número de botones del grupo de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="16146-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="16146-120">Las **estructuras DTBLRADIOBUTTON** para los demás botones del grupo deben estar contenidas en filas sucesivas de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="16146-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="16146-121">Cada una de estas filas debe contener el mismo valor para el **miembro ulcButtons.**</span><span class="sxs-lookup"><span data-stu-id="16146-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="16146-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="16146-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="16146-123">Etiqueta de propiedad de una propiedad de tipo PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="16146-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="16146-124">La selección inicial en el grupo de botones de radio se basa en el valor inicial de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="16146-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="16146-125">Cada botón del grupo debe tener **ulPropTag** establecido en la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="16146-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="16146-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="16146-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="16146-127">Número único que identifica el botón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="16146-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16146-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16146-128">Remarks</span></span>

<span data-ttu-id="16146-129">Una **estructura DTBLRADIOBUTTON** describe un botón de radio de un control de botón asociado a un grupo de botones.</span><span class="sxs-lookup"><span data-stu-id="16146-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="16146-130">Solo se puede comprobar un botón del grupo; establecer un botón hace que los demás botones del grupo se desconjunte.</span><span class="sxs-lookup"><span data-stu-id="16146-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="16146-131">El recuento de botones es el número de botones de radio del grupo.</span><span class="sxs-lookup"><span data-stu-id="16146-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="16146-132">Las estructuras de los demás botones de radio del grupo deben estar en filas posteriores de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="16146-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="16146-133">Cada una de estas estructuras debe tener el mismo valor para su recuento de botones.</span><span class="sxs-lookup"><span data-stu-id="16146-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="16146-134">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="16146-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="16146-135">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [Implementar una tabla para mostrar.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="16146-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16146-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16146-136">See also</span></span>



[<span data-ttu-id="16146-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="16146-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="16146-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="16146-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="16146-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="16146-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="16146-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="16146-140">MAPI Structures</span></span>](mapi-structures.md)

