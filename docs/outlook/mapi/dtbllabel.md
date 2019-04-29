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
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410689"
---
# <a name="dtbllabel"></a><span data-ttu-id="17a09-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="17a09-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="17a09-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17a09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17a09-105">Describe una etiqueta que se utilizará en un cuadro de diálogo que se genera a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="17a09-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17a09-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="17a09-106">Header file:</span></span>  <br/> |<span data-ttu-id="17a09-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="17a09-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="17a09-108">Macro relacionada</span><span class="sxs-lookup"><span data-stu-id="17a09-108">Related macro</span></span>  <br/> |[<span data-ttu-id="17a09-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="17a09-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="17a09-110">Members</span><span class="sxs-lookup"><span data-stu-id="17a09-110">Members</span></span>

 <span data-ttu-id="17a09-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="17a09-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="17a09-112">Posición en la memoria de la etiqueta de la cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="17a09-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="17a09-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="17a09-113">**ulFlags**</span></span>
  
> <span data-ttu-id="17a09-114">Máscara de la máscara usada para designar el formato de la etiqueta a la que señala el miembro **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="17a09-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="17a09-115">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="17a09-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="17a09-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="17a09-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="17a09-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="17a09-117">The label is in Unicode format.</span></span> <span data-ttu-id="17a09-118">Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="17a09-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17a09-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17a09-119">Remarks</span></span>

<span data-ttu-id="17a09-120">Una estructura **DTBLLABEL** describe un texto de control de etiqueta que se muestra con otro tipo de control para agregar significado a ese control.</span><span class="sxs-lookup"><span data-stu-id="17a09-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="17a09-121">Por ejemplo, la mayoría de los controles de edición se colocan junto a las etiquetas para informar al usuario del tipo de información que se va a especificar.</span><span class="sxs-lookup"><span data-stu-id="17a09-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="17a09-122">Algunos controles, como cuadros de grupo y botones de opción, contienen sus propias etiquetas.</span><span class="sxs-lookup"><span data-stu-id="17a09-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="17a09-123">La etiqueta puede incluir un acelerador de Windows, identificado como el carácter que sigue&amp;a la y comercial ().</span><span class="sxs-lookup"><span data-stu-id="17a09-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="17a09-124">Si se presiona la tecla de método abreviado, el foco se sitúa en el primer control que no sea una etiqueta y que no esté situado a continuación de esta etiqueta de la tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="17a09-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="17a09-125">No se admiten etiquetas de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="17a09-125">There is no support for multiline labels.</span></span> <span data-ttu-id="17a09-126">Mostrar varias líneas requiere varias etiquetas.</span><span class="sxs-lookup"><span data-stu-id="17a09-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="17a09-127">No se puede usar una etiqueta como control de edición de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="17a09-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="17a09-128">La diferencia es que un control de edición se puede seleccionar y copiar mientras que una etiqueta no puede.</span><span class="sxs-lookup"><span data-stu-id="17a09-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="17a09-129">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="17a09-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="17a09-130">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="17a09-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17a09-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="17a09-131">See also</span></span>



[<span data-ttu-id="17a09-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="17a09-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="17a09-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="17a09-133">MAPI Structures</span></span>](mapi-structures.md)

