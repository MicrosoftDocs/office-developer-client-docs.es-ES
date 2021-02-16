---
title: Elemento SnapSettings (Window_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.
ms.openlocfilehash: 0fbe54f56f79d84e6c6bd8ddc11aa28b7e5ba1dc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540318"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a><span data-ttu-id="33155-103">Elemento SnapSettings (Window_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="33155-103">SnapSettings element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="33155-104">Especifica los objetos a los que se acoplan las formas cuando el ajuste está activo en la ventana.</span><span class="sxs-lookup"><span data-stu-id="33155-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33155-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="33155-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33155-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="33155-106">**Element type**</span></span> <br/> |[<span data-ttu-id="33155-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="33155-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="33155-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="33155-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="33155-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="33155-109">**Schema file**</span></span> <br/> |<span data-ttu-id="33155-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="33155-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="33155-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="33155-111">**Document parts**</span></span> <br/> |<span data-ttu-id="33155-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="33155-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="33155-113">Definición</span><span class="sxs-lookup"><span data-stu-id="33155-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="33155-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="33155-114">Elements and attributes</span></span>

<span data-ttu-id="33155-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="33155-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="33155-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="33155-116">Parent elements</span></span>

|<span data-ttu-id="33155-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="33155-117">**Element**</span></span>|<span data-ttu-id="33155-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="33155-118">**Type**</span></span>|<span data-ttu-id="33155-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33155-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="33155-120">Window</span><span class="sxs-lookup"><span data-stu-id="33155-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="33155-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="33155-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="33155-122">Representa una ventana abierta en una instancia de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="33155-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="33155-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="33155-123">Child elements</span></span>

<span data-ttu-id="33155-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="33155-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33155-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="33155-125">Attributes</span></span>

<span data-ttu-id="33155-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="33155-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33155-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33155-127">Remarks</span></span>

<span data-ttu-id="33155-128">El valor puede ser una suma de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="33155-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="33155-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="33155-129">**Value**</span></span>|<span data-ttu-id="33155-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33155-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33155-131">0</span><span class="sxs-lookup"><span data-stu-id="33155-131">0</span></span>  <br/> |<span data-ttu-id="33155-132">No se ajusta a ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="33155-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="33155-133">1 </span><span class="sxs-lookup"><span data-stu-id="33155-133">1</span></span>  <br/> |<span data-ttu-id="33155-134">Se ajusta a subdivisiones de regla.</span><span class="sxs-lookup"><span data-stu-id="33155-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="33155-135">2 </span><span class="sxs-lookup"><span data-stu-id="33155-135">2</span></span>  <br/> |<span data-ttu-id="33155-136">Se ajusta a la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="33155-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="33155-137">4 </span><span class="sxs-lookup"><span data-stu-id="33155-137">4</span></span>  <br/> |<span data-ttu-id="33155-138">Se ajusta a las guías.</span><span class="sxs-lookup"><span data-stu-id="33155-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="33155-139">8 </span><span class="sxs-lookup"><span data-stu-id="33155-139">8</span></span>  <br/> |<span data-ttu-id="33155-140">Se ajustan a asas de selección.</span><span class="sxs-lookup"><span data-stu-id="33155-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="33155-141">16 </span><span class="sxs-lookup"><span data-stu-id="33155-141">16</span></span>  <br/> |<span data-ttu-id="33155-142">Se ajusta a los vértices.</span><span class="sxs-lookup"><span data-stu-id="33155-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="33155-143">32</span><span class="sxs-lookup"><span data-stu-id="33155-143">32</span></span>  <br/> |<span data-ttu-id="33155-144">Se ajusta a los puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="33155-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="33155-145">256</span><span class="sxs-lookup"><span data-stu-id="33155-145">256</span></span>  <br/> |<span data-ttu-id="33155-146">Se ajusta a los bordes visibles de las formas.</span><span class="sxs-lookup"><span data-stu-id="33155-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="33155-147">512</span><span class="sxs-lookup"><span data-stu-id="33155-147">512</span></span>  <br/> |<span data-ttu-id="33155-148">Se ajusta al cuadro de alineación.</span><span class="sxs-lookup"><span data-stu-id="33155-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="33155-149">1024</span><span class="sxs-lookup"><span data-stu-id="33155-149">1024</span></span>  <br/> |<span data-ttu-id="33155-150">Se ajusta a las opciones de extensión de las formas.</span><span class="sxs-lookup"><span data-stu-id="33155-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="33155-151">32768</span><span class="sxs-lookup"><span data-stu-id="33155-151">32768</span></span>  <br/> |<span data-ttu-id="33155-152">Ajuste deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="33155-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="33155-153">65536</span><span class="sxs-lookup"><span data-stu-id="33155-153">65536</span></span>  <br/> |<span data-ttu-id="33155-154">Se ajusta a las intersecciones.</span><span class="sxs-lookup"><span data-stu-id="33155-154">Snap to intersections.</span></span>  <br/> |
   

