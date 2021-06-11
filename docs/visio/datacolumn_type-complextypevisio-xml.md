---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541214"
---
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="8b875-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8b875-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8b875-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="8b875-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b875-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8b875-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8b875-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8b875-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8b875-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8b875-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8b875-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="8b875-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8b875-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8b875-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b875-109">Definición</span><span class="sxs-lookup"><span data-stu-id="8b875-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8b875-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8b875-110">Elements and attributes</span></span>

<span data-ttu-id="8b875-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8b875-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8b875-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b875-112">Child elements</span></span>

<span data-ttu-id="8b875-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8b875-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b875-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b875-114">Attributes</span></span>

|<span data-ttu-id="8b875-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8b875-115">**Attribute**</span></span>|<span data-ttu-id="8b875-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8b875-116">**Type**</span></span>|<span data-ttu-id="8b875-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8b875-117">**Required**</span></span>|<span data-ttu-id="8b875-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b875-118">**Description**</span></span>|<span data-ttu-id="8b875-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="8b875-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8b875-120">Calendar</span><span class="sxs-lookup"><span data-stu-id="8b875-120">Calendar</span></span>  <br/> |<span data-ttu-id="8b875-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8b875-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8b875-122">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-122">optional</span></span>  <br/> ||<span data-ttu-id="8b875-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8b875-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8b875-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="8b875-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="8b875-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8b875-125">xsd:string</span></span>  <br/> |<span data-ttu-id="8b875-126">necesario</span><span class="sxs-lookup"><span data-stu-id="8b875-126">required</span></span>  <br/> ||<span data-ttu-id="8b875-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8b875-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b875-128">Moneda</span><span class="sxs-lookup"><span data-stu-id="8b875-128">Currency</span></span>  <br/> |<span data-ttu-id="8b875-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8b875-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8b875-130">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-130">optional</span></span>  <br/> ||<span data-ttu-id="8b875-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8b875-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8b875-132">DataType</span><span class="sxs-lookup"><span data-stu-id="8b875-132">DataType</span></span>  <br/> |<span data-ttu-id="8b875-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="8b875-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="8b875-134">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-134">optional</span></span>  <br/> ||<span data-ttu-id="8b875-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="8b875-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="8b875-136">Degree</span><span class="sxs-lookup"><span data-stu-id="8b875-136">Degree</span></span>  <br/> |<span data-ttu-id="8b875-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b875-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b875-138">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-138">optional</span></span>  <br/> ||<span data-ttu-id="8b875-139">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b875-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8b875-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="8b875-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="8b875-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b875-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b875-142">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-142">optional</span></span>  <br/> ||<span data-ttu-id="8b875-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b875-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8b875-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="8b875-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="8b875-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b875-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b875-146">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-146">optional</span></span>  <br/> ||<span data-ttu-id="8b875-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b875-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8b875-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="8b875-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="8b875-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8b875-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8b875-150">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-150">optional</span></span>  <br/> ||<span data-ttu-id="8b875-151">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8b875-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8b875-152">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8b875-152">Label</span></span>  <br/> |<span data-ttu-id="8b875-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8b875-153">xsd:string</span></span>  <br/> |<span data-ttu-id="8b875-154">necesario</span><span class="sxs-lookup"><span data-stu-id="8b875-154">required</span></span>  <br/> ||<span data-ttu-id="8b875-155">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8b875-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b875-156">LangID</span><span class="sxs-lookup"><span data-stu-id="8b875-156">LangID</span></span>  <br/> |<span data-ttu-id="8b875-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8b875-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8b875-158">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-158">optional</span></span>  <br/> ||<span data-ttu-id="8b875-159">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8b875-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8b875-160">Asignado</span><span class="sxs-lookup"><span data-stu-id="8b875-160">Mapped</span></span>  <br/> |<span data-ttu-id="8b875-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8b875-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8b875-162">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-162">optional</span></span>  <br/> ||<span data-ttu-id="8b875-163">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="8b875-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8b875-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="8b875-164">Name</span></span>  <br/> |<span data-ttu-id="8b875-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8b875-165">xsd:string</span></span>  <br/> |<span data-ttu-id="8b875-166">necesario</span><span class="sxs-lookup"><span data-stu-id="8b875-166">required</span></span>  <br/> ||<span data-ttu-id="8b875-167">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8b875-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b875-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="8b875-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="8b875-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8b875-169">xsd:string</span></span>  <br/> |<span data-ttu-id="8b875-170">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-170">optional</span></span>  <br/> ||<span data-ttu-id="8b875-171">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8b875-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8b875-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="8b875-172">UnitType</span></span>  <br/> |<span data-ttu-id="8b875-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8b875-173">xsd:string</span></span>  <br/> |<span data-ttu-id="8b875-174">opcional</span><span class="sxs-lookup"><span data-stu-id="8b875-174">optional</span></span>  <br/> ||<span data-ttu-id="8b875-175">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8b875-175">Values of the xsd:string type.</span></span>  <br/> |
   

