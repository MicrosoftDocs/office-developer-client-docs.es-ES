---
title: Propiedad canónica PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734206"
---
# <a name="pidtagcontroltype-canonical-property"></a><span data-ttu-id="89436-103">Propiedad canónica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="89436-103">PidTagControlType Canonical Property</span></span>

  
  
<span data-ttu-id="89436-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89436-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89436-105">Contiene un valor que indica un tipo de control para un control usado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-105">Contains a value indicating a control type for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89436-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="89436-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89436-107">PR_CONTROL_TYPE</span><span class="sxs-lookup"><span data-stu-id="89436-107">PR_CONTROL_TYPE</span></span>  <br/> |
|<span data-ttu-id="89436-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="89436-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89436-109">0x3F02</span><span class="sxs-lookup"><span data-stu-id="89436-109">0x3F02</span></span>  <br/> |
|<span data-ttu-id="89436-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="89436-110">Data type:</span></span>  <br/> |<span data-ttu-id="89436-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="89436-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="89436-112">Área:</span><span class="sxs-lookup"><span data-stu-id="89436-112">Area:</span></span>  <br/> |<span data-ttu-id="89436-113">Tabla para mostrar MAPI</span><span class="sxs-lookup"><span data-stu-id="89436-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89436-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89436-114">Remarks</span></span>

<span data-ttu-id="89436-115">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="89436-115">This property can have exactly one of the following values:</span></span>
    
<span data-ttu-id="89436-116">DTCT_LABEL (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="89436-116">DTCT_LABEL (0x00000000)</span></span>
  
> <span data-ttu-id="89436-117">Una etiqueta de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-117">A dialog label.</span></span>
   
<span data-ttu-id="89436-118">DTCT_EDIT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="89436-118">DTCT_EDIT (0x00000001)</span></span>
  
> <span data-ttu-id="89436-119">Cuadro de texto de edición de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-119">A dialog edit text box.</span></span>

<span data-ttu-id="89436-120">DTCT_LBX (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="89436-120">DTCT_LBX (0x00000002)</span></span>
  
> <span data-ttu-id="89436-121">Cuadro de lista de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-121">A dialog list box.</span></span>
    
<span data-ttu-id="89436-122">DTCT_COMBOBOX (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="89436-122">DTCT_COMBOBOX (0x00000003)</span></span>
  
> <span data-ttu-id="89436-123">Cuadro combinado de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-123">A dialog combo box.</span></span>

<span data-ttu-id="89436-124">DTCT_DDLBX (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="89436-124">DTCT_DDLBX (0x00000004)</span></span>
  
> <span data-ttu-id="89436-125">Cuadro de lista desplegable de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-125">A dialog drop-down list box.</span></span>

<span data-ttu-id="89436-126">DTCT_CHECKBOX (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="89436-126">DTCT_CHECKBOX (0x00000005)</span></span>
  
> <span data-ttu-id="89436-127">Una casilla de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-127">A dialog check box.</span></span>

<span data-ttu-id="89436-128">DTCT_GROUPBOX (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="89436-128">DTCT_GROUPBOX (0x00000006)</span></span>
  
> <span data-ttu-id="89436-129">Un cuadro de diálogo de grupo.</span><span class="sxs-lookup"><span data-stu-id="89436-129">A dialog group box.</span></span>
  
<span data-ttu-id="89436-130">DTCT_BUTTON (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="89436-130">DTCT_BUTTON (0x00000007)</span></span>
  
> <span data-ttu-id="89436-131">Un control de botón de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-131">A dialog button control.</span></span>
    
<span data-ttu-id="89436-132">DTCT_PAGE (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="89436-132">DTCT_PAGE (0x00000008)</span></span>
  
> <span data-ttu-id="89436-133">Una página con pestañas de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-133">A dialog tabbed page.</span></span>
    
<span data-ttu-id="89436-134">DTCT_RADIOBUTTON (0x00000009)</span><span class="sxs-lookup"><span data-stu-id="89436-134">DTCT_RADIOBUTTON (0x00000009)</span></span>
  
> <span data-ttu-id="89436-135">Un botón de radio de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89436-135">A dialog radio button.</span></span>
    
<span data-ttu-id="89436-136">DTCT_MVLISTBOX (0x0000000B)</span><span class="sxs-lookup"><span data-stu-id="89436-136">DTCT_MVLISTBOX (0x0000000B)</span></span>
  
> <span data-ttu-id="89436-137">Cuadro de lista multivalor rellenado por una propiedad multivalor de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="89436-137">A multivalued list box populated by a multivalued property of type string.</span></span>
    
<span data-ttu-id="89436-138">DTCT_MVDDLBX (0x0000000C)</span><span class="sxs-lookup"><span data-stu-id="89436-138">DTCT_MVDDLBX (0x0000000C)</span></span>
  
> <span data-ttu-id="89436-139">Cuadro de lista desplegable con varios valores rellenado por una propiedad multivalor de tipo cadena.</span><span class="sxs-lookup"><span data-stu-id="89436-139">A multivalued drop-down list box populated by a multivalued property of type string.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="89436-140">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89436-140">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="89436-141">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="89436-141">Header files</span></span>

<span data-ttu-id="89436-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89436-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="89436-143">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="89436-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="89436-144">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89436-144">mapitags.h</span></span>
  
> <span data-ttu-id="89436-145">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="89436-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89436-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89436-146">See also</span></span>



[<span data-ttu-id="89436-147">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89436-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89436-148">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="89436-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89436-149">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="89436-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89436-150">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="89436-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

