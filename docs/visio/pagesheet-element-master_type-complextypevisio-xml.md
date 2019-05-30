---
title: Elemento PageSheet (complexType Master_Type) (XML de Visio)
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
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="bb148-103">Elemento PageSheet (complexType Master_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="bb148-103">PageSheet element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bb148-104">Especifica las propiedades de la página de dibujo asociada al patrón.</span><span class="sxs-lookup"><span data-stu-id="bb148-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb148-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb148-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb148-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="bb148-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bb148-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="bb148-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bb148-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bb148-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bb148-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bb148-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bb148-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="bb148-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bb148-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="bb148-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bb148-112">Masters. XML</span><span class="sxs-lookup"><span data-stu-id="bb148-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bb148-113">Definición</span><span class="sxs-lookup"><span data-stu-id="bb148-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bb148-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bb148-114">Elements and attributes</span></span>

<span data-ttu-id="bb148-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="bb148-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bb148-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb148-116">Parent elements</span></span>

|<span data-ttu-id="bb148-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb148-117">**Element**</span></span>|<span data-ttu-id="bb148-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bb148-118">**Type**</span></span>|<span data-ttu-id="bb148-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb148-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bb148-120">Master</span><span class="sxs-lookup"><span data-stu-id="bb148-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bb148-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="bb148-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bb148-122">Especifica un patrón en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="bb148-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb148-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb148-123">Child elements</span></span>

<span data-ttu-id="bb148-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb148-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb148-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb148-125">Attributes</span></span>

|<span data-ttu-id="bb148-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bb148-126">**Attribute**</span></span>|<span data-ttu-id="bb148-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bb148-127">**Type**</span></span>|<span data-ttu-id="bb148-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="bb148-128">**Required**</span></span>|<span data-ttu-id="bb148-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb148-129">**Description**</span></span>|<span data-ttu-id="bb148-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="bb148-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bb148-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="bb148-131">FillStyle</span></span>  <br/> |<span data-ttu-id="bb148-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bb148-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bb148-133">opcional</span><span class="sxs-lookup"><span data-stu-id="bb148-133">optional</span></span>  <br/> |<span data-ttu-id="bb148-134">especifica el identificador de la hoja de estilos de la que se va a heredar el formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="bb148-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="bb148-135">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="bb148-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="bb148-136">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bb148-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bb148-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="bb148-137">LineStyle</span></span>  <br/> |<span data-ttu-id="bb148-138">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bb148-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bb148-139">opcional</span><span class="sxs-lookup"><span data-stu-id="bb148-139">optional</span></span>  <br/> |<span data-ttu-id="bb148-140">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de línea.</span><span class="sxs-lookup"><span data-stu-id="bb148-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="bb148-141">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="bb148-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="bb148-142">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bb148-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bb148-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="bb148-143">TextStyle</span></span>  <br/> |<span data-ttu-id="bb148-144">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bb148-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bb148-145">opcional</span><span class="sxs-lookup"><span data-stu-id="bb148-145">optional</span></span>  <br/> |<span data-ttu-id="bb148-146">Especifica el identificador de la hoja de estilos de la que se va a heredar el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="bb148-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="bb148-147">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="bb148-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="bb148-148">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bb148-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bb148-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="bb148-149">UniqueID</span></span>  <br/> |<span data-ttu-id="bb148-150">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bb148-150">xsd:string</span></span>  <br/> |<span data-ttu-id="bb148-151">opcional</span><span class="sxs-lookup"><span data-stu-id="bb148-151">optional</span></span>  <br/> |<span data-ttu-id="bb148-152">IDENTIFICADOR único del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="bb148-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="bb148-153">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bb148-153">Values of the xsd:string type.</span></span>  <br/> |
   

