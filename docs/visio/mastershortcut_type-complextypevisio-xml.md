---
title: MasterShortcut_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341695"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="b13fb-102">MasterShortcut_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b13fb-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b13fb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b13fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b13fb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b13fb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b13fb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b13fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b13fb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b13fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b13fb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b13fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b13fb-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b13fb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b13fb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b13fb-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b13fb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b13fb-110">Elements and attributes</span></span>

<span data-ttu-id="b13fb-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b13fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b13fb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b13fb-112">Child elements</span></span>

|<span data-ttu-id="b13fb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b13fb-113">**Element**</span></span>|<span data-ttu-id="b13fb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b13fb-114">**Type**</span></span>|<span data-ttu-id="b13fb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b13fb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b13fb-116">Icon</span><span class="sxs-lookup"><span data-stu-id="b13fb-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b13fb-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="b13fb-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b13fb-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b13fb-118">Attributes</span></span>

|<span data-ttu-id="b13fb-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b13fb-119">**Attribute**</span></span>|<span data-ttu-id="b13fb-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b13fb-120">**Type**</span></span>|<span data-ttu-id="b13fb-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b13fb-121">**Required**</span></span>|<span data-ttu-id="b13fb-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b13fb-122">**Description**</span></span>|<span data-ttu-id="b13fb-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b13fb-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b13fb-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="b13fb-124">AlignName</span></span>  <br/> |<span data-ttu-id="b13fb-125">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b13fb-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b13fb-126">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-126">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-127">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b13fb-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="b13fb-128">IconSize</span></span>  <br/> |<span data-ttu-id="b13fb-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b13fb-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b13fb-130">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-130">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b13fb-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-132">ID</span><span class="sxs-lookup"><span data-stu-id="b13fb-132">ID</span></span>  <br/> |<span data-ttu-id="b13fb-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b13fb-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b13fb-134">necesario</span><span class="sxs-lookup"><span data-stu-id="b13fb-134">required</span></span>  <br/> ||<span data-ttu-id="b13fb-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b13fb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="b13fb-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="b13fb-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="b13fb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b13fb-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-138">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-139">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b13fb-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="b13fb-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="b13fb-141">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="b13fb-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b13fb-142">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-142">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-143">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b13fb-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="b13fb-144">MasterType</span></span>  <br/> |<span data-ttu-id="b13fb-145">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b13fb-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b13fb-146">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-146">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-147">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b13fb-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="b13fb-148">Name</span></span>  <br/> |<span data-ttu-id="b13fb-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b13fb-149">xsd:string</span></span>  <br/> |<span data-ttu-id="b13fb-150">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-150">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-151">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b13fb-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-152">NameU</span><span class="sxs-lookup"><span data-stu-id="b13fb-152">NameU</span></span>  <br/> |<span data-ttu-id="b13fb-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b13fb-153">xsd:string</span></span>  <br/> |<span data-ttu-id="b13fb-154">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-154">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-155">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b13fb-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="b13fb-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="b13fb-157">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b13fb-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b13fb-158">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-158">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-159">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b13fb-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="b13fb-160">Prompt</span></span>  <br/> |<span data-ttu-id="b13fb-161">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b13fb-161">xsd:string</span></span>  <br/> |<span data-ttu-id="b13fb-162">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-162">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-163">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b13fb-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="b13fb-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="b13fb-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b13fb-165">xsd:string</span></span>  <br/> |<span data-ttu-id="b13fb-166">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-166">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-167">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b13fb-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b13fb-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="b13fb-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="b13fb-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b13fb-169">xsd:string</span></span>  <br/> |<span data-ttu-id="b13fb-170">opcional</span><span class="sxs-lookup"><span data-stu-id="b13fb-170">optional</span></span>  <br/> ||<span data-ttu-id="b13fb-171">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b13fb-171">Values of the xsd:string type.</span></span>  <br/> |
   

