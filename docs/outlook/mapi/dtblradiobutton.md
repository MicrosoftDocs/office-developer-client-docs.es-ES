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
ms.openlocfilehash: 493176029be3e7b154188aa164a95a8bc9c0e7d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569746"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="6d985-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="6d985-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="6d985-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d985-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d985-105">Describe un botón de opción que formará parte de un grupo de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="6d985-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="6d985-106">Se usará el grupo de botones de radio en un cuadro de diálogo que se genera a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6d985-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d985-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6d985-107">Header file:</span></span>  <br/> |<span data-ttu-id="6d985-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d985-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="6d985-109">Members</span><span class="sxs-lookup"><span data-stu-id="6d985-109">Members</span></span>

 <span data-ttu-id="6d985-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="6d985-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="6d985-111">Posición en la memoria de la etiqueta de cadena de caracteres para el botón de opción.</span><span class="sxs-lookup"><span data-stu-id="6d985-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="6d985-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="6d985-112">**ulFlags**</span></span>
  
> <span data-ttu-id="6d985-113">Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="6d985-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="6d985-114">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="6d985-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="6d985-115">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6d985-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6d985-116">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6d985-116">The label is in Unicode format.</span></span> <span data-ttu-id="6d985-117">Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6d985-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="6d985-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="6d985-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="6d985-119">Recuento de botones en el grupo de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="6d985-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="6d985-120">Las estructuras **DTBLRADIOBUTTON** para los otros botones en el grupo deben estar incluidas en las filas sucesivas de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6d985-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="6d985-121">Cada una de estas filas debe contener el mismo valor para el miembro **ulcButtons** .</span><span class="sxs-lookup"><span data-stu-id="6d985-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="6d985-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="6d985-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="6d985-123">Etiqueta de propiedad de una propiedad de tipo PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="6d985-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="6d985-124">La selección inicial en el grupo de botones de radio se basa en el valor inicial de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6d985-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="6d985-125">Cada botón en el grupo debe tener **ulPropTag** establecida en la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="6d985-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="6d985-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="6d985-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="6d985-127">Número único que identifica el botón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="6d985-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d985-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d985-128">Remarks</span></span>

<span data-ttu-id="6d985-129">Una estructura **DTBLRADIOBUTTON** describe un botón de opción de un control de botón que está asociado a un grupo de botones.</span><span class="sxs-lookup"><span data-stu-id="6d985-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="6d985-130">Sólo un botón en el grupo se puede proteger; establecer un botón hace que el resto de los botones en el grupo al que se va a anular.</span><span class="sxs-lookup"><span data-stu-id="6d985-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="6d985-131">El recuento de botón es el número de botones de opción en el grupo.</span><span class="sxs-lookup"><span data-stu-id="6d985-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="6d985-132">Las estructuras de los otros botones de opción en el grupo deben ser en filas posteriores en la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="6d985-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="6d985-133">Cada una de estas estructuras debe tener el mismo valor para su número de botones.</span><span class="sxs-lookup"><span data-stu-id="6d985-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="6d985-134">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6d985-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="6d985-135">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="6d985-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d985-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6d985-136">See also</span></span>



[<span data-ttu-id="6d985-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="6d985-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="6d985-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="6d985-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="6d985-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="6d985-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="6d985-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="6d985-140">MAPI Structures</span></span>](mapi-structures.md)

