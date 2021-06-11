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
# <a name="dtbllabel"></a><span data-ttu-id="82971-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="82971-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="82971-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82971-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82971-105">Describe una etiqueta que se usará en un cuadro de diálogo creado a partir de una tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="82971-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82971-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="82971-106">Header file:</span></span>  <br/> |<span data-ttu-id="82971-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82971-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="82971-108">Macro relacionada</span><span class="sxs-lookup"><span data-stu-id="82971-108">Related macro</span></span>  <br/> |[<span data-ttu-id="82971-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="82971-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="82971-110">Members</span><span class="sxs-lookup"><span data-stu-id="82971-110">Members</span></span>

 <span data-ttu-id="82971-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="82971-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="82971-112">Posición en la memoria de la etiqueta de cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="82971-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="82971-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="82971-113">**ulFlags**</span></span>
  
> <span data-ttu-id="82971-114">Máscara de bits de las marcas usadas para designar el formato de la etiqueta a la que apunta el **miembro ulbLpszLabelName.**</span><span class="sxs-lookup"><span data-stu-id="82971-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="82971-115">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="82971-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="82971-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82971-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="82971-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="82971-117">The label is in Unicode format.</span></span> <span data-ttu-id="82971-118">Si la MAPI_UNICODE no está establecida, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="82971-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82971-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82971-119">Remarks</span></span>

<span data-ttu-id="82971-120">Una **estructura DTBLLABEL** describe un texto de control de etiqueta que se muestra con otro tipo de control para agregar significado a ese control.</span><span class="sxs-lookup"><span data-stu-id="82971-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="82971-121">Por ejemplo, la mayoría de los controles de edición se sitúan junto a las etiquetas para informar al usuario del tipo de información que se va a especificar.</span><span class="sxs-lookup"><span data-stu-id="82971-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="82971-122">Algunos controles, como cuadros de grupo y botones de radio, tienen sus propias etiquetas.</span><span class="sxs-lookup"><span data-stu-id="82971-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="82971-123">La etiqueta puede incluir un acelerador Windows, identificado como el carácter que sigue a la ampersand ( &amp; ).</span><span class="sxs-lookup"><span data-stu-id="82971-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="82971-124">Al presionar la tecla de aceleración, se coloca el foco en el primer control sin etiqueta y sin botón que sigue a esta etiqueta en la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="82971-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="82971-125">No hay compatibilidad con etiquetas de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="82971-125">There is no support for multiline labels.</span></span> <span data-ttu-id="82971-126">Mostrar varias líneas requiere varias etiquetas.</span><span class="sxs-lookup"><span data-stu-id="82971-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="82971-127">No es posible usar una etiqueta como control de edición de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="82971-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="82971-128">La diferencia es que un control de edición se puede seleccionar y copiar mientras que una etiqueta no puede.</span><span class="sxs-lookup"><span data-stu-id="82971-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="82971-129">Para obtener información general sobre las tablas para mostrar, vea [Tablas para mostrar.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="82971-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="82971-130">Para obtener información sobre cómo implementar una tabla para mostrar, vea [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="82971-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82971-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="82971-131">See also</span></span>



[<span data-ttu-id="82971-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="82971-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="82971-133">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="82971-133">MAPI Structures</span></span>](mapi-structures.md)

