---
title: Elemento PageSheet (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Especifica las propiedades de la página de dibujo asociada al patrón.
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540619"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a><span data-ttu-id="b3363-103">Elemento PageSheet (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b3363-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b3363-104">Especifica las propiedades de la página de dibujo asociada al patrón.</span><span class="sxs-lookup"><span data-stu-id="b3363-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3363-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b3363-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3363-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b3363-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b3363-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="b3363-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b3363-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b3363-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b3363-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b3363-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b3363-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b3363-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b3363-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b3363-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b3363-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="b3363-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b3363-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b3363-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b3363-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b3363-114">Elements and attributes</span></span>

<span data-ttu-id="b3363-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b3363-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b3363-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b3363-116">Parent elements</span></span>

|<span data-ttu-id="b3363-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b3363-117">**Element**</span></span>|<span data-ttu-id="b3363-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3363-118">**Type**</span></span>|<span data-ttu-id="b3363-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3363-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b3363-120">Master</span><span class="sxs-lookup"><span data-stu-id="b3363-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b3363-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="b3363-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b3363-122">Especifica un patrón en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="b3363-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b3363-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b3363-123">Child elements</span></span>

<span data-ttu-id="b3363-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b3363-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3363-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="b3363-125">Attributes</span></span>

|<span data-ttu-id="b3363-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b3363-126">**Attribute**</span></span>|<span data-ttu-id="b3363-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3363-127">**Type**</span></span>|<span data-ttu-id="b3363-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b3363-128">**Required**</span></span>|<span data-ttu-id="b3363-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b3363-129">**Description**</span></span>|<span data-ttu-id="b3363-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b3363-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b3363-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="b3363-131">FillStyle</span></span>  <br/> |<span data-ttu-id="b3363-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3363-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b3363-133">opcional</span><span class="sxs-lookup"><span data-stu-id="b3363-133">optional</span></span>  <br/> |<span data-ttu-id="b3363-134">especifica el identificador de la hoja de estilos desde la que se va a heredar el formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="b3363-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="b3363-135">Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="b3363-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="b3363-136">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b3363-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b3363-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="b3363-137">LineStyle</span></span>  <br/> |<span data-ttu-id="b3363-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3363-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b3363-139">opcional</span><span class="sxs-lookup"><span data-stu-id="b3363-139">optional</span></span>  <br/> |<span data-ttu-id="b3363-140">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de línea.</span><span class="sxs-lookup"><span data-stu-id="b3363-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="b3363-141">Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="b3363-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="b3363-142">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b3363-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b3363-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="b3363-143">TextStyle</span></span>  <br/> |<span data-ttu-id="b3363-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3363-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b3363-145">opcional</span><span class="sxs-lookup"><span data-stu-id="b3363-145">optional</span></span>  <br/> |<span data-ttu-id="b3363-146">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="b3363-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="b3363-147">Debe ser el valor del atributo **ID** asociado a **un StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="b3363-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="b3363-148">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b3363-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b3363-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="b3363-149">UniqueID</span></span>  <br/> |<span data-ttu-id="b3363-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b3363-150">xsd:string</span></span>  <br/> |<span data-ttu-id="b3363-151">opcional</span><span class="sxs-lookup"><span data-stu-id="b3363-151">optional</span></span>  <br/> |<span data-ttu-id="b3363-152">El identificador único del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="b3363-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="b3363-153">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b3363-153">Values of the xsd:string type.</span></span>  <br/> |
   

