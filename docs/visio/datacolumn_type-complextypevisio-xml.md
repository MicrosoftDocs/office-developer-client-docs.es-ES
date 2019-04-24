---
title: DataColumn_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344705"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="dc205-102">DataColumn_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="dc205-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="dc205-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="dc205-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc205-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dc205-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="dc205-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dc205-105">**Schema file**</span></span> <br/> |<span data-ttu-id="dc205-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="dc205-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="dc205-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="dc205-107">**Extension base**</span></span> <br/> |<span data-ttu-id="dc205-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dc205-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc205-109">Definición</span><span class="sxs-lookup"><span data-stu-id="dc205-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc205-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="dc205-110">Elements and attributes</span></span>

<span data-ttu-id="dc205-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="dc205-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dc205-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc205-112">Child elements</span></span>

<span data-ttu-id="dc205-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc205-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc205-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc205-114">Attributes</span></span>

|<span data-ttu-id="dc205-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="dc205-115">**Attribute**</span></span>|<span data-ttu-id="dc205-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dc205-116">**Type**</span></span>|<span data-ttu-id="dc205-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="dc205-117">**Required**</span></span>|<span data-ttu-id="dc205-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc205-118">**Description**</span></span>|<span data-ttu-id="dc205-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="dc205-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc205-120">Calendar</span><span class="sxs-lookup"><span data-stu-id="dc205-120">Calendar</span></span>  <br/> |<span data-ttu-id="dc205-121">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="dc205-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="dc205-122">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-122">optional</span></span>  <br/> ||<span data-ttu-id="dc205-123">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="dc205-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="dc205-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="dc205-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="dc205-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc205-125">xsd:string</span></span>  <br/> |<span data-ttu-id="dc205-126">necesario</span><span class="sxs-lookup"><span data-stu-id="dc205-126">required</span></span>  <br/> ||<span data-ttu-id="dc205-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc205-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc205-128">Moneda</span><span class="sxs-lookup"><span data-stu-id="dc205-128">Currency</span></span>  <br/> |<span data-ttu-id="dc205-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="dc205-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="dc205-130">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-130">optional</span></span>  <br/> ||<span data-ttu-id="dc205-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="dc205-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="dc205-132">DataType</span><span class="sxs-lookup"><span data-stu-id="dc205-132">DataType</span></span>  <br/> |<span data-ttu-id="dc205-133">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="dc205-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="dc205-134">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-134">optional</span></span>  <br/> ||<span data-ttu-id="dc205-135">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="dc205-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="dc205-136">Degree</span><span class="sxs-lookup"><span data-stu-id="dc205-136">Degree</span></span>  <br/> |<span data-ttu-id="dc205-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dc205-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dc205-138">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-138">optional</span></span>  <br/> ||<span data-ttu-id="dc205-139">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dc205-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dc205-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="dc205-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="dc205-141">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dc205-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dc205-142">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-142">optional</span></span>  <br/> ||<span data-ttu-id="dc205-143">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dc205-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dc205-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="dc205-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="dc205-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dc205-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dc205-146">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-146">optional</span></span>  <br/> ||<span data-ttu-id="dc205-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dc205-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dc205-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="dc205-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="dc205-149">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="dc205-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dc205-150">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-150">optional</span></span>  <br/> ||<span data-ttu-id="dc205-151">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="dc205-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dc205-152">Label</span><span class="sxs-lookup"><span data-stu-id="dc205-152">Label</span></span>  <br/> |<span data-ttu-id="dc205-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc205-153">xsd:string</span></span>  <br/> |<span data-ttu-id="dc205-154">necesario</span><span class="sxs-lookup"><span data-stu-id="dc205-154">required</span></span>  <br/> ||<span data-ttu-id="dc205-155">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc205-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc205-156">Idioma</span><span class="sxs-lookup"><span data-stu-id="dc205-156">LangID</span></span>  <br/> |<span data-ttu-id="dc205-157">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dc205-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dc205-158">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-158">optional</span></span>  <br/> ||<span data-ttu-id="dc205-159">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dc205-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dc205-160">Asignación</span><span class="sxs-lookup"><span data-stu-id="dc205-160">Mapped</span></span>  <br/> |<span data-ttu-id="dc205-161">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="dc205-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dc205-162">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-162">optional</span></span>  <br/> ||<span data-ttu-id="dc205-163">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="dc205-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dc205-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc205-164">Name</span></span>  <br/> |<span data-ttu-id="dc205-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc205-165">xsd:string</span></span>  <br/> |<span data-ttu-id="dc205-166">necesario</span><span class="sxs-lookup"><span data-stu-id="dc205-166">required</span></span>  <br/> ||<span data-ttu-id="dc205-167">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc205-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc205-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="dc205-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="dc205-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc205-169">xsd:string</span></span>  <br/> |<span data-ttu-id="dc205-170">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-170">optional</span></span>  <br/> ||<span data-ttu-id="dc205-171">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc205-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dc205-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="dc205-172">UnitType</span></span>  <br/> |<span data-ttu-id="dc205-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="dc205-173">xsd:string</span></span>  <br/> |<span data-ttu-id="dc205-174">opcional</span><span class="sxs-lookup"><span data-stu-id="dc205-174">optional</span></span>  <br/> ||<span data-ttu-id="dc205-175">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="dc205-175">Values of the xsd:string type.</span></span>  <br/> |
   

