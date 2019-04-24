---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287272"
---
# <a name="dtblcheckbox"></a><span data-ttu-id="cb492-103">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="cb492-103">DTBLCHECKBOX</span></span>

  
  
<span data-ttu-id="cb492-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb492-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb492-105">Contiene información sobre una casilla de verificación que se utilizará en un cuadro de diálogo generado a partir de una tabla de presentación.</span><span class="sxs-lookup"><span data-stu-id="cb492-105">Contains information about a check box that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cb492-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cb492-106">Header file:</span></span>  <br/> |<span data-ttu-id="cb492-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cb492-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cb492-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="cb492-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="cb492-109">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="cb492-109">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a><span data-ttu-id="cb492-110">Members</span><span class="sxs-lookup"><span data-stu-id="cb492-110">Members</span></span>

 <span data-ttu-id="cb492-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="cb492-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="cb492-112">Posición en la memoria de la cadena de caracteres que se muestra con la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="cb492-112">Position in memory of the character string that is displayed with the check box.</span></span> 
    
 <span data-ttu-id="cb492-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="cb492-113">**ulFlags**</span></span>
  
> <span data-ttu-id="cb492-114">Máscara de la máscara usada para designar el formato de la etiqueta de casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="cb492-114">Bitmask of flags used to designate the format of the check box label.</span></span> <span data-ttu-id="cb492-115">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="cb492-115">The following flag can be set:</span></span>
    
<span data-ttu-id="cb492-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb492-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cb492-117">La etiqueta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb492-117">The label is in Unicode format.</span></span> <span data-ttu-id="cb492-118">Si no se establece la marca MAPI_UNICODE, la etiqueta está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="cb492-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="cb492-119">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="cb492-119">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="cb492-120">Etiqueta de propiedad de una propiedad de tipo PT_BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="cb492-120">Property tag for a property of type PT_BOOLEAN.</span></span> <span data-ttu-id="cb492-121">El valor de esta propiedad se ve afectado por el estado de la casilla.</span><span class="sxs-lookup"><span data-stu-id="cb492-121">The value of this property is affected by the state of the check box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb492-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb492-122">Remarks</span></span>

<span data-ttu-id="cb492-123">Una estructura **DTBLCHECKBOX** describe una casilla de verificación de un control que refleja uno de los dos Estados: habilitado (casilla activada) o deshabilitado (un cuadro vacío).</span><span class="sxs-lookup"><span data-stu-id="cb492-123">A **DTBLCHECKBOX** structure describes a check box a control that reflects one of two states: enabled (a checked box) or disabled (an empty box).</span></span> 
  
<span data-ttu-id="cb492-124">El miembro **ulPRPropertyName** describe una propiedad booleana cuyo valor se manipula cambiando el estado de la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="cb492-124">The **ulPRPropertyName** member describes a Boolean property whose value is manipulated by changing the state of the check box.</span></span> <span data-ttu-id="cb492-125">Cuando la casilla aparece por primera vez, MAPI llama al método **GetProps** de la implementación de **IMAPIProp** asociada a la tabla de presentación para recuperar un conjunto de propiedades predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="cb492-125">When the check box is first displayed, MAPI calls the **GetProps** method of the **IMAPIProp** implementation that is associated with the display table to retrieve a set of default properties.</span></span> <span data-ttu-id="cb492-126">Si una de las propiedades se asigna a la etiqueta de propiedad en la estructura **DTBLCHECKBOX** , el valor de esa propiedad se muestra como el valor inicial de la casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="cb492-126">If one of the properties maps to the property tag in the **DTBLCHECKBOX** structure, the value for that property is displayed as the check box's initial value.</span></span> 
  
<span data-ttu-id="cb492-127">Los controles de casilla de verificación pueden poder modificarse.</span><span class="sxs-lookup"><span data-stu-id="cb492-127">Check box controls can be modifiable.</span></span> <span data-ttu-id="cb492-128">Esto permite a un usuario cambiar sus Estados.</span><span class="sxs-lookup"><span data-stu-id="cb492-128">This allows a user to change their states.</span></span> <span data-ttu-id="cb492-129">Las casillas de verificación modificables establecen la marca DT_EDITABLE en el miembro **ulCtlFlags** de su estructura [DTCTL](dtctl.md) y en su propiedad **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cb492-129">Modifiable check boxes set the DT_EDITABLE flag in the **ulCtlFlags** member of their [DTCTL](dtctl.md) structure and in their **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="cb492-130">Cuando una casilla de verificación cambia su estado, MAPI llama a [IMAPIProp:: SetProps](imapiprop-setprops.md) para establecer la propiedad identificada en el miembro de etiqueta de propiedad de la estructura **DTBLCHECKBOX** en el nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="cb492-130">When a check box changes its state, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the property identified in the property tag member of the **DTBLCHECKBOX** structure to the new state.</span></span> 
  
<span data-ttu-id="cb492-131">Por ejemplo, un proveedor de libreta de direcciones puede incluir un control de casilla de verificación modificable en su cuadro de diálogo de configuración para ajustar la configuración de la propiedad **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="cb492-131">For example, an address book provider might include a modifiable check box control in its configuration dialog box to adjust the setting of a recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property.</span></span> <span data-ttu-id="cb492-132">Cuando el usuario selecciona la casilla de verificación, MAPI establece esta propiedad en TRUE.</span><span class="sxs-lookup"><span data-stu-id="cb492-132">When the user selects the check box, MAPI sets this property to TRUE.</span></span> <span data-ttu-id="cb492-133">Cuando no se selecciona la casilla de verificación, la propiedad se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="cb492-133">When the check box is unselected, the property is set to FALSE.</span></span>
  
<span data-ttu-id="cb492-134">Para obtener información general sobre las tablas de presentación, consulte [Display tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cb492-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="cb492-135">Para obtener información acerca de cómo implementar una tabla de visualización, consulte [Implementing a display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cb492-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="cb492-136">Para obtener información acerca de los tipos de propiedades, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cb492-136">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb492-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb492-137">See also</span></span>



[<span data-ttu-id="cb492-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="cb492-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="cb492-139">Propiedad canónica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="cb492-139">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="cb492-140">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="cb492-140">MAPI Structures</span></span>](mapi-structures.md)

