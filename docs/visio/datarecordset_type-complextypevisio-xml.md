---
title: DataRecordSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360365"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="ad4a2-102">DataRecordSet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ad4a2-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ad4a2-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ad4a2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad4a2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad4a2-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad4a2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ad4a2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad4a2-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad4a2-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ad4a2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad4a2-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ad4a2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ad4a2-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ad4a2-110">Elements and attributes</span></span>

<span data-ttu-id="ad4a2-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad4a2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad4a2-112">Child elements</span></span>

|<span data-ttu-id="ad4a2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-113">**Element**</span></span>|<span data-ttu-id="ad4a2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-114">**Type**</span></span>|<span data-ttu-id="ad4a2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad4a2-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="ad4a2-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4a2-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="ad4a2-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad4a2-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="ad4a2-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4a2-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="ad4a2-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad4a2-120">ClavePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad4a2-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4a2-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="ad4a2-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad4a2-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="ad4a2-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4a2-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="ad4a2-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad4a2-124">REL</span><span class="sxs-lookup"><span data-stu-id="ad4a2-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4a2-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ad4a2-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad4a2-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="ad4a2-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4a2-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="ad4a2-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad4a2-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad4a2-128">Attributes</span></span>

|<span data-ttu-id="ad4a2-129">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-129">**Attribute**</span></span>|<span data-ttu-id="ad4a2-130">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-130">**Type**</span></span>|<span data-ttu-id="ad4a2-131">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-131">**Required**</span></span>|<span data-ttu-id="ad4a2-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-132">**Description**</span></span>|<span data-ttu-id="ad4a2-133">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ad4a2-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad4a2-134">Suma de comprobación</span><span class="sxs-lookup"><span data-stu-id="ad4a2-134">Checksum</span></span>  <br/> |<span data-ttu-id="ad4a2-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-136">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-136">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-138">Command</span><span class="sxs-lookup"><span data-stu-id="ad4a2-138">Command</span></span>  <br/> |<span data-ttu-id="ad4a2-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ad4a2-139">xsd:string</span></span>  <br/> |<span data-ttu-id="ad4a2-140">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-140">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-141">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="ad4a2-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="ad4a2-143">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-144">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-144">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-145">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-146">ID</span><span class="sxs-lookup"><span data-stu-id="ad4a2-146">ID</span></span>  <br/> |<span data-ttu-id="ad4a2-147">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-148">necesario</span><span class="sxs-lookup"><span data-stu-id="ad4a2-148">required</span></span>  <br/> ||<span data-ttu-id="ad4a2-149">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad4a2-150">Name</span></span>  <br/> |<span data-ttu-id="ad4a2-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ad4a2-151">xsd:string</span></span>  <br/> |<span data-ttu-id="ad4a2-152">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-152">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-153">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="ad4a2-154">NextRowID</span></span>  <br/> |<span data-ttu-id="ad4a2-155">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-156">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-156">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-157">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-158">Opciones</span><span class="sxs-lookup"><span data-stu-id="ad4a2-158">Options</span></span>  <br/> |<span data-ttu-id="ad4a2-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-160">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-160">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-161">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="ad4a2-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="ad4a2-163">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-164">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-164">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-165">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="ad4a2-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="ad4a2-167">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ad4a2-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ad4a2-168">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-168">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-169">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="ad4a2-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="ad4a2-171">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ad4a2-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ad4a2-172">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-172">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-173">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="ad4a2-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="ad4a2-175">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad4a2-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad4a2-176">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-176">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-177">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="ad4a2-178">RowOrder</span></span>  <br/> |<span data-ttu-id="ad4a2-179">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ad4a2-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ad4a2-180">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-180">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-181">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ad4a2-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="ad4a2-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="ad4a2-183">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="ad4a2-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="ad4a2-184">opcional</span><span class="sxs-lookup"><span data-stu-id="ad4a2-184">optional</span></span>  <br/> ||<span data-ttu-id="ad4a2-185">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

