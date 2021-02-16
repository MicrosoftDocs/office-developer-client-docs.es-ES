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
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="08acd-102">DataColumn_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="08acd-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="08acd-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="08acd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08acd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08acd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="08acd-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="08acd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="08acd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="08acd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="08acd-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="08acd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="08acd-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="08acd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08acd-109">Definición</span><span class="sxs-lookup"><span data-stu-id="08acd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="08acd-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="08acd-110">Elements and attributes</span></span>

<span data-ttu-id="08acd-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="08acd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="08acd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08acd-112">Child elements</span></span>

<span data-ttu-id="08acd-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08acd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08acd-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="08acd-114">Attributes</span></span>

|<span data-ttu-id="08acd-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="08acd-115">**Attribute**</span></span>|<span data-ttu-id="08acd-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08acd-116">**Type**</span></span>|<span data-ttu-id="08acd-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="08acd-117">**Required**</span></span>|<span data-ttu-id="08acd-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08acd-118">**Description**</span></span>|<span data-ttu-id="08acd-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="08acd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="08acd-120">Calendar</span><span class="sxs-lookup"><span data-stu-id="08acd-120">Calendar</span></span>  <br/> |<span data-ttu-id="08acd-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="08acd-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="08acd-122">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-122">optional</span></span>  <br/> ||<span data-ttu-id="08acd-123">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="08acd-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="08acd-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="08acd-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="08acd-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="08acd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="08acd-126">necesario</span><span class="sxs-lookup"><span data-stu-id="08acd-126">required</span></span>  <br/> ||<span data-ttu-id="08acd-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="08acd-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08acd-128">Divisa</span><span class="sxs-lookup"><span data-stu-id="08acd-128">Currency</span></span>  <br/> |<span data-ttu-id="08acd-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="08acd-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="08acd-130">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-130">optional</span></span>  <br/> ||<span data-ttu-id="08acd-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="08acd-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="08acd-132">DataType</span><span class="sxs-lookup"><span data-stu-id="08acd-132">DataType</span></span>  <br/> |<span data-ttu-id="08acd-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="08acd-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="08acd-134">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-134">optional</span></span>  <br/> ||<span data-ttu-id="08acd-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="08acd-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="08acd-136">Degree</span><span class="sxs-lookup"><span data-stu-id="08acd-136">Degree</span></span>  <br/> |<span data-ttu-id="08acd-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08acd-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08acd-138">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-138">optional</span></span>  <br/> ||<span data-ttu-id="08acd-139">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08acd-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="08acd-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="08acd-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="08acd-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08acd-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08acd-142">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-142">optional</span></span>  <br/> ||<span data-ttu-id="08acd-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08acd-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="08acd-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="08acd-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="08acd-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08acd-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08acd-146">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-146">optional</span></span>  <br/> ||<span data-ttu-id="08acd-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08acd-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="08acd-148">Hipervínculo</span><span class="sxs-lookup"><span data-stu-id="08acd-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="08acd-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="08acd-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="08acd-150">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-150">optional</span></span>  <br/> ||<span data-ttu-id="08acd-151">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="08acd-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="08acd-152">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="08acd-152">Label</span></span>  <br/> |<span data-ttu-id="08acd-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="08acd-153">xsd:string</span></span>  <br/> |<span data-ttu-id="08acd-154">necesario</span><span class="sxs-lookup"><span data-stu-id="08acd-154">required</span></span>  <br/> ||<span data-ttu-id="08acd-155">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="08acd-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08acd-156">LangID</span><span class="sxs-lookup"><span data-stu-id="08acd-156">LangID</span></span>  <br/> |<span data-ttu-id="08acd-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="08acd-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="08acd-158">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-158">optional</span></span>  <br/> ||<span data-ttu-id="08acd-159">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="08acd-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="08acd-160">Asignado</span><span class="sxs-lookup"><span data-stu-id="08acd-160">Mapped</span></span>  <br/> |<span data-ttu-id="08acd-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="08acd-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="08acd-162">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-162">optional</span></span>  <br/> ||<span data-ttu-id="08acd-163">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="08acd-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="08acd-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="08acd-164">Name</span></span>  <br/> |<span data-ttu-id="08acd-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="08acd-165">xsd:string</span></span>  <br/> |<span data-ttu-id="08acd-166">necesario</span><span class="sxs-lookup"><span data-stu-id="08acd-166">required</span></span>  <br/> ||<span data-ttu-id="08acd-167">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="08acd-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08acd-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="08acd-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="08acd-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="08acd-169">xsd:string</span></span>  <br/> |<span data-ttu-id="08acd-170">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-170">optional</span></span>  <br/> ||<span data-ttu-id="08acd-171">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="08acd-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="08acd-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="08acd-172">UnitType</span></span>  <br/> |<span data-ttu-id="08acd-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="08acd-173">xsd:string</span></span>  <br/> |<span data-ttu-id="08acd-174">opcional</span><span class="sxs-lookup"><span data-stu-id="08acd-174">optional</span></span>  <br/> ||<span data-ttu-id="08acd-175">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="08acd-175">Values of the xsd:string type.</span></span>  <br/> |
   

