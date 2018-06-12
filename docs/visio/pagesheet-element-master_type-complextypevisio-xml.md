---
title: Elemento PageSheet (Master_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Especifica las propiedades de la página de dibujo asociadas con el patrón.
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822762"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="ae328-103">Elemento PageSheet (Master_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ae328-103">PageSheet element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ae328-104">Especifica las propiedades de la página de dibujo asociadas con el patrón.</span><span class="sxs-lookup"><span data-stu-id="ae328-104">Specifies the properties of the drawing page associated with the master.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae328-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae328-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae328-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ae328-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ae328-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ae328-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ae328-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ae328-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ae328-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ae328-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ae328-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ae328-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ae328-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ae328-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ae328-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="ae328-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae328-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ae328-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ae328-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ae328-114">Elements and attributes</span></span>

<span data-ttu-id="ae328-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ae328-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ae328-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae328-116">Parent elements</span></span>

|<span data-ttu-id="ae328-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae328-117">**Element**</span></span>|<span data-ttu-id="ae328-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ae328-118">**Type**</span></span>|<span data-ttu-id="ae328-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae328-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae328-120">Master</span><span class="sxs-lookup"><span data-stu-id="ae328-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae328-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="ae328-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae328-122">Especifica a un patrón en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ae328-122">Specifies a master in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae328-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae328-123">Child elements</span></span>

<span data-ttu-id="ae328-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae328-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae328-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae328-125">Attributes</span></span>

|<span data-ttu-id="ae328-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ae328-126">**Attribute**</span></span>|<span data-ttu-id="ae328-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ae328-127">**Type**</span></span>|<span data-ttu-id="ae328-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ae328-128">**Required**</span></span>|<span data-ttu-id="ae328-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae328-129">**Description**</span></span>|<span data-ttu-id="ae328-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="ae328-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ae328-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="ae328-131">FillStyle</span></span>  <br/> |<span data-ttu-id="ae328-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae328-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae328-133">opcional</span><span class="sxs-lookup"><span data-stu-id="ae328-133">optional</span></span>  <br/> |<span data-ttu-id="ae328-134">Especifica el identificador de la hoja de estilos desde la que se heredan de formato de relleno.</span><span class="sxs-lookup"><span data-stu-id="ae328-134">specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="ae328-135">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="ae328-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="ae328-136">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae328-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae328-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="ae328-137">LineStyle</span></span>  <br/> |<span data-ttu-id="ae328-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae328-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae328-139">opcional</span><span class="sxs-lookup"><span data-stu-id="ae328-139">optional</span></span>  <br/> |<span data-ttu-id="ae328-140">Especifica el identificador de la hoja de estilos desde la que se heredan de formato de línea.</span><span class="sxs-lookup"><span data-stu-id="ae328-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="ae328-141">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="ae328-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="ae328-142">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae328-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae328-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="ae328-143">TextStyle</span></span>  <br/> |<span data-ttu-id="ae328-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae328-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae328-145">opcional</span><span class="sxs-lookup"><span data-stu-id="ae328-145">optional</span></span>  <br/> |<span data-ttu-id="ae328-146">Especifica el identificador de la hoja de estilos desde la que se heredan de formato de texto.</span><span class="sxs-lookup"><span data-stu-id="ae328-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="ae328-147">DEBE ser el valor del atributo **ID** asociado con un **StyleSheet_Type** en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="ae328-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="ae328-148">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ae328-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae328-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ae328-149">UniqueID</span></span>  <br/> |<span data-ttu-id="ae328-150">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ae328-150">xsd:string</span></span>  <br/> |<span data-ttu-id="ae328-151">opcional</span><span class="sxs-lookup"><span data-stu-id="ae328-151">optional</span></span>  <br/> |<span data-ttu-id="ae328-152">Identificador único del elemento dentro de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="ae328-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="ae328-153">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="ae328-153">Values of the xsd:string type.</span></span>  <br/> |
   

