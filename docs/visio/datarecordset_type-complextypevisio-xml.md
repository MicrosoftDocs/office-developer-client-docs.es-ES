---
title: DataRecordSet_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821927"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="85a9a-102">DataRecordSet_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="85a9a-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="85a9a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="85a9a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85a9a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85a9a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85a9a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85a9a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85a9a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="85a9a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85a9a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="85a9a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85a9a-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="85a9a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85a9a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="85a9a-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="85a9a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="85a9a-110">Elements and attributes</span></span>

<span data-ttu-id="85a9a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="85a9a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85a9a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85a9a-112">Child elements</span></span>

|<span data-ttu-id="85a9a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="85a9a-113">**Element**</span></span>|<span data-ttu-id="85a9a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85a9a-114">**Type**</span></span>|<span data-ttu-id="85a9a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85a9a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85a9a-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="85a9a-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a9a-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="85a9a-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a9a-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="85a9a-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a9a-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="85a9a-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a9a-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="85a9a-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a9a-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="85a9a-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a9a-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="85a9a-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a9a-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="85a9a-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a9a-124">Rel</span><span class="sxs-lookup"><span data-stu-id="85a9a-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a9a-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="85a9a-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="85a9a-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="85a9a-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85a9a-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="85a9a-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85a9a-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="85a9a-128">Attributes</span></span>

|<span data-ttu-id="85a9a-129">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="85a9a-129">**Attribute**</span></span>|<span data-ttu-id="85a9a-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85a9a-130">**Type**</span></span>|<span data-ttu-id="85a9a-131">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="85a9a-131">**Required**</span></span>|<span data-ttu-id="85a9a-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85a9a-132">**Description**</span></span>|<span data-ttu-id="85a9a-133">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="85a9a-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85a9a-134">Suma de comprobación</span><span class="sxs-lookup"><span data-stu-id="85a9a-134">Checksum</span></span>  <br/> |<span data-ttu-id="85a9a-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-136">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-136">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-138">Comando</span><span class="sxs-lookup"><span data-stu-id="85a9a-138">Command</span></span>  <br/> |<span data-ttu-id="85a9a-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="85a9a-139">xsd:string</span></span>  <br/> |<span data-ttu-id="85a9a-140">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-140">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-141">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="85a9a-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="85a9a-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="85a9a-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-144">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-144">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-146">ID</span><span class="sxs-lookup"><span data-stu-id="85a9a-146">ID</span></span>  <br/> |<span data-ttu-id="85a9a-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-148">necesario</span><span class="sxs-lookup"><span data-stu-id="85a9a-148">required</span></span>  <br/> ||<span data-ttu-id="85a9a-149">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="85a9a-150">Name</span></span>  <br/> |<span data-ttu-id="85a9a-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="85a9a-151">xsd:string</span></span>  <br/> |<span data-ttu-id="85a9a-152">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-152">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-153">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="85a9a-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="85a9a-154">NextRowID</span></span>  <br/> |<span data-ttu-id="85a9a-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-156">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-156">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-157">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-158">Options</span><span class="sxs-lookup"><span data-stu-id="85a9a-158">Options</span></span>  <br/> |<span data-ttu-id="85a9a-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-160">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-160">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-161">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="85a9a-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="85a9a-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-164">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-164">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-165">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="85a9a-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="85a9a-167">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="85a9a-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="85a9a-168">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-168">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-169">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="85a9a-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="85a9a-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="85a9a-171">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="85a9a-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="85a9a-172">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-172">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-173">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="85a9a-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="85a9a-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="85a9a-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="85a9a-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="85a9a-176">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-176">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-177">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="85a9a-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="85a9a-178">RowOrder</span></span>  <br/> |<span data-ttu-id="85a9a-179">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="85a9a-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="85a9a-180">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-180">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-181">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="85a9a-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="85a9a-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="85a9a-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="85a9a-183">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="85a9a-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="85a9a-184">opcional</span><span class="sxs-lookup"><span data-stu-id="85a9a-184">optional</span></span>  <br/> ||<span data-ttu-id="85a9a-185">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="85a9a-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

