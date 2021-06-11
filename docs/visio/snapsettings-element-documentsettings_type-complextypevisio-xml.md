---
title: Elemento SnapSettings (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540297"
---
# <a name="snapsettings-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="df198-103">Elemento SnapSettings (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="df198-103">SnapSettings element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="df198-104">Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.</span><span class="sxs-lookup"><span data-stu-id="df198-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df198-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="df198-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df198-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="df198-106">**Element type**</span></span> <br/> |[<span data-ttu-id="df198-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="df198-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="df198-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="df198-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="df198-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="df198-109">**Schema file**</span></span> <br/> |<span data-ttu-id="df198-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="df198-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="df198-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="df198-111">**Document parts**</span></span> <br/> |<span data-ttu-id="df198-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="df198-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df198-113">Definición</span><span class="sxs-lookup"><span data-stu-id="df198-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df198-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="df198-114">Elements and attributes</span></span>

<span data-ttu-id="df198-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="df198-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="df198-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="df198-116">Parent elements</span></span>

|<span data-ttu-id="df198-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="df198-117">**Element**</span></span>|<span data-ttu-id="df198-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df198-118">**Type**</span></span>|<span data-ttu-id="df198-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df198-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df198-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="df198-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df198-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="df198-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df198-122">Contiene elementos que especifican la configuración del documento.</span><span class="sxs-lookup"><span data-stu-id="df198-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df198-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df198-123">Child elements</span></span>

<span data-ttu-id="df198-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df198-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df198-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="df198-125">Attributes</span></span>

<span data-ttu-id="df198-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df198-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df198-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df198-127">Remarks</span></span>

<span data-ttu-id="df198-128">El valor puede ser una suma de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="df198-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="df198-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="df198-129">**Value**</span></span>|<span data-ttu-id="df198-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df198-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df198-131">0</span><span class="sxs-lookup"><span data-stu-id="df198-131">0</span></span>  <br/> |<span data-ttu-id="df198-132">No se ajusta a ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="df198-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="df198-133">1</span><span class="sxs-lookup"><span data-stu-id="df198-133">1</span></span>  <br/> |<span data-ttu-id="df198-134">Acoplar a subdivisiones de regla.</span><span class="sxs-lookup"><span data-stu-id="df198-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="df198-135">2</span><span class="sxs-lookup"><span data-stu-id="df198-135">2</span></span>  <br/> |<span data-ttu-id="df198-136">Acoplar a la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="df198-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="df198-137">4 </span><span class="sxs-lookup"><span data-stu-id="df198-137">4</span></span>  <br/> |<span data-ttu-id="df198-138">Se ajusta a las guías.</span><span class="sxs-lookup"><span data-stu-id="df198-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="df198-139">8 </span><span class="sxs-lookup"><span data-stu-id="df198-139">8</span></span>  <br/> |<span data-ttu-id="df198-140">Se ajustan a asas de selección.</span><span class="sxs-lookup"><span data-stu-id="df198-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="df198-141">16 </span><span class="sxs-lookup"><span data-stu-id="df198-141">16</span></span>  <br/> |<span data-ttu-id="df198-142">Se ajusta a los vértices.</span><span class="sxs-lookup"><span data-stu-id="df198-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="df198-143">32</span><span class="sxs-lookup"><span data-stu-id="df198-143">32</span></span>  <br/> |<span data-ttu-id="df198-144">Se ajusta a los puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="df198-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="df198-145">256</span><span class="sxs-lookup"><span data-stu-id="df198-145">256</span></span>  <br/> |<span data-ttu-id="df198-146">Acoplar a los bordes visibles de las formas.</span><span class="sxs-lookup"><span data-stu-id="df198-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="df198-147">512</span><span class="sxs-lookup"><span data-stu-id="df198-147">512</span></span>  <br/> |<span data-ttu-id="df198-148">Acoplar al cuadro de alineación.</span><span class="sxs-lookup"><span data-stu-id="df198-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="df198-149">1024</span><span class="sxs-lookup"><span data-stu-id="df198-149">1024</span></span>  <br/> |<span data-ttu-id="df198-150">Se ajusta a las opciones de extensión de las formas.</span><span class="sxs-lookup"><span data-stu-id="df198-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="df198-151">32768</span><span class="sxs-lookup"><span data-stu-id="df198-151">32768</span></span>  <br/> |<span data-ttu-id="df198-152">Acoplar deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="df198-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="df198-153">65536</span><span class="sxs-lookup"><span data-stu-id="df198-153">65536</span></span>  <br/> |<span data-ttu-id="df198-154">Se ajusta a las intersecciones.</span><span class="sxs-lookup"><span data-stu-id="df198-154">Snap to intersections.</span></span>  <br/> |
   

