---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816741"
---
# <a name="dtbllabel"></a><span data-ttu-id="c9342-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="c9342-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="c9342-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9342-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9342-105">Describe una etiqueta que se usará en un cuadro de diálogo que se genera a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c9342-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9342-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c9342-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9342-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9342-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c9342-108">Macro relacionado</span><span class="sxs-lookup"><span data-stu-id="c9342-108">Related macro</span></span>  <br/> |[<span data-ttu-id="c9342-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="c9342-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="c9342-110">Members</span><span class="sxs-lookup"><span data-stu-id="c9342-110">Members</span></span>

 <span data-ttu-id="c9342-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="c9342-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="c9342-112">Posición en la memoria de la etiqueta de cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c9342-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="c9342-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c9342-113">**ulFlags**</span></span>
  
> <span data-ttu-id="c9342-114">Máscara de bits de indicadores que se utilizan para designar el formato de la etiqueta que señala el miembro **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="c9342-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="c9342-115">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="c9342-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="c9342-116">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c9342-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c9342-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c9342-117">The label is in Unicode format.</span></span> <span data-ttu-id="c9342-118">Si no está establecido el indicador MAPI_UNICODE., la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c9342-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9342-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9342-119">Remarks</span></span>

<span data-ttu-id="c9342-120">Una estructura **DTBLLABEL** describe un texto de control de etiqueta que se muestra con otro tipo de control que se va a agregar significado a ese control.</span><span class="sxs-lookup"><span data-stu-id="c9342-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="c9342-121">Por ejemplo, la mayoría de los controles de edición se coloca junto a las etiquetas para informar al usuario del tipo de información que debe escribirse.</span><span class="sxs-lookup"><span data-stu-id="c9342-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="c9342-122">Algunos controles, como cuadros de grupo y los botones de radio, mantenga sus propias etiquetas.</span><span class="sxs-lookup"><span data-stu-id="c9342-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="c9342-123">La etiqueta puede incluir un acelerador de Windows, identificado como el carácter que sigue la y comercial (&amp;).</span><span class="sxs-lookup"><span data-stu-id="c9342-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="c9342-124">Al presionar la tecla de aceleración coloca el foco en el primer nonlabel, control de nonbutton seguir esta etiqueta en la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c9342-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="c9342-125">No hay ninguna compatibilidad para las etiquetas de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="c9342-125">There is no support for multiline labels.</span></span> <span data-ttu-id="c9342-126">Mostrar varias líneas requiere varias etiquetas.</span><span class="sxs-lookup"><span data-stu-id="c9342-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="c9342-127">No es posible utilizar una etiqueta como un control de edición de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9342-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="c9342-128">La diferencia es que un control de edición se puede seleccionar y copiar mientras que una etiqueta no se puede.</span><span class="sxs-lookup"><span data-stu-id="c9342-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="c9342-129">Para obtener información general de las tablas para mostrar, vea [Mostrar tablas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c9342-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c9342-130">Para obtener información acerca de cómo implementar una tabla para mostrar, vea [implementar una tabla mostrar](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c9342-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9342-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9342-131">See also</span></span>



[<span data-ttu-id="c9342-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c9342-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="c9342-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c9342-133">MAPI Structures</span></span>](mapi-structures.md)
