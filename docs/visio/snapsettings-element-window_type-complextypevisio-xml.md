---
title: Elemento SnapSettings (complexType Window_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica los objetos a los que se ajustan las formas cuando se activa ajustar en la ventana.
ms.openlocfilehash: 0fbe54f56f79d84e6c6bd8ddc11aa28b7e5ba1dc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540318"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="00893-103">Elemento SnapSettings (complexType Window_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="00893-103">SnapSettings element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="00893-104">Especifica los objetos a los que se ajustan las formas cuando se activa ajustar en la ventana.</span><span class="sxs-lookup"><span data-stu-id="00893-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00893-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="00893-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00893-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="00893-106">**Element type**</span></span> <br/> |[<span data-ttu-id="00893-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="00893-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="00893-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="00893-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="00893-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="00893-109">**Schema file**</span></span> <br/> |<span data-ttu-id="00893-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="00893-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="00893-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="00893-111">**Document parts**</span></span> <br/> |<span data-ttu-id="00893-112">Windows. XML</span><span class="sxs-lookup"><span data-stu-id="00893-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00893-113">Definición</span><span class="sxs-lookup"><span data-stu-id="00893-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="00893-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="00893-114">Elements and attributes</span></span>

<span data-ttu-id="00893-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="00893-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="00893-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="00893-116">Parent elements</span></span>

|<span data-ttu-id="00893-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="00893-117">**Element**</span></span>|<span data-ttu-id="00893-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="00893-118">**Type**</span></span>|<span data-ttu-id="00893-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00893-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="00893-120">Window</span><span class="sxs-lookup"><span data-stu-id="00893-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="00893-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="00893-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="00893-122">Representa una ventana abierta en una instancia de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="00893-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="00893-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="00893-123">Child elements</span></span>

<span data-ttu-id="00893-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00893-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00893-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="00893-125">Attributes</span></span>

<span data-ttu-id="00893-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00893-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00893-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00893-127">Remarks</span></span>

<span data-ttu-id="00893-128">El valor puede ser una suma de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="00893-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="00893-129">**Value**</span><span class="sxs-lookup"><span data-stu-id="00893-129">**Value**</span></span>|<span data-ttu-id="00893-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00893-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00893-131">comprendi</span><span class="sxs-lookup"><span data-stu-id="00893-131">0</span></span>  <br/> |<span data-ttu-id="00893-132">No se ajusta a ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="00893-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="00893-133">1 </span><span class="sxs-lookup"><span data-stu-id="00893-133">1</span></span>  <br/> |<span data-ttu-id="00893-134">Se ajusta a las subdivisiones de regla.</span><span class="sxs-lookup"><span data-stu-id="00893-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="00893-135">2 </span><span class="sxs-lookup"><span data-stu-id="00893-135">2</span></span>  <br/> |<span data-ttu-id="00893-136">Ajustar a la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="00893-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="00893-137">4 </span><span class="sxs-lookup"><span data-stu-id="00893-137">4</span></span>  <br/> |<span data-ttu-id="00893-138">Se ajusta a las guías.</span><span class="sxs-lookup"><span data-stu-id="00893-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="00893-139">8 </span><span class="sxs-lookup"><span data-stu-id="00893-139">8</span></span>  <br/> |<span data-ttu-id="00893-140">Se ajustan a asas de selección.</span><span class="sxs-lookup"><span data-stu-id="00893-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="00893-141">16 </span><span class="sxs-lookup"><span data-stu-id="00893-141">16</span></span>  <br/> |<span data-ttu-id="00893-142">Se ajusta a los vértices.</span><span class="sxs-lookup"><span data-stu-id="00893-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="00893-143">32</span><span class="sxs-lookup"><span data-stu-id="00893-143">32</span></span>  <br/> |<span data-ttu-id="00893-144">Se ajusta a los puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="00893-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="00893-145">256</span><span class="sxs-lookup"><span data-stu-id="00893-145">256</span></span>  <br/> |<span data-ttu-id="00893-146">Se ajusta a los bordes visibles de las formas.</span><span class="sxs-lookup"><span data-stu-id="00893-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="00893-147">512</span><span class="sxs-lookup"><span data-stu-id="00893-147">512</span></span>  <br/> |<span data-ttu-id="00893-148">Se ajusta al cuadro de alineación.</span><span class="sxs-lookup"><span data-stu-id="00893-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="00893-149">1024</span><span class="sxs-lookup"><span data-stu-id="00893-149">1024</span></span>  <br/> |<span data-ttu-id="00893-150">Se ajusta a las opciones de extensión de las formas.</span><span class="sxs-lookup"><span data-stu-id="00893-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="00893-151">32768</span><span class="sxs-lookup"><span data-stu-id="00893-151">32768</span></span>  <br/> |<span data-ttu-id="00893-152">Ajuste deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="00893-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="00893-153">65536</span><span class="sxs-lookup"><span data-stu-id="00893-153">65536</span></span>  <br/> |<span data-ttu-id="00893-154">Se ajusta a las intersecciones.</span><span class="sxs-lookup"><span data-stu-id="00893-154">Snap to intersections.</span></span>  <br/> |
   

