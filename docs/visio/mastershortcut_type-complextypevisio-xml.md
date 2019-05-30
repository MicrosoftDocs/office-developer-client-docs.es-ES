---
title: ComplexType MasterShortcut_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538063"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="ab65c-102">ComplexType MasterShortcut_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="ab65c-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ab65c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ab65c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab65c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab65c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ab65c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ab65c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ab65c-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ab65c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ab65c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ab65c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ab65c-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ab65c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab65c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ab65c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ab65c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ab65c-110">Elements and attributes</span></span>

<span data-ttu-id="ab65c-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ab65c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ab65c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab65c-112">Child elements</span></span>

|<span data-ttu-id="ab65c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ab65c-113">**Element**</span></span>|<span data-ttu-id="ab65c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ab65c-114">**Type**</span></span>|<span data-ttu-id="ab65c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab65c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ab65c-116">Icon</span><span class="sxs-lookup"><span data-stu-id="ab65c-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ab65c-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="ab65c-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ab65c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab65c-118">Attributes</span></span>

|<span data-ttu-id="ab65c-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ab65c-119">**Attribute**</span></span>|<span data-ttu-id="ab65c-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ab65c-120">**Type**</span></span>|<span data-ttu-id="ab65c-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ab65c-121">**Required**</span></span>|<span data-ttu-id="ab65c-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab65c-122">**Description**</span></span>|<span data-ttu-id="ab65c-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ab65c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab65c-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="ab65c-124">AlignName</span></span>  <br/> |<span data-ttu-id="ab65c-125">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ab65c-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ab65c-126">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-126">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-127">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ab65c-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="ab65c-128">IconSize</span></span>  <br/> |<span data-ttu-id="ab65c-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ab65c-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ab65c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-130">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ab65c-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-132">ID</span><span class="sxs-lookup"><span data-stu-id="ab65c-132">ID</span></span>  <br/> |<span data-ttu-id="ab65c-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ab65c-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ab65c-134">necesario</span><span class="sxs-lookup"><span data-stu-id="ab65c-134">required</span></span>  <br/> ||<span data-ttu-id="ab65c-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ab65c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="ab65c-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="ab65c-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ab65c-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ab65c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-138">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-139">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ab65c-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="ab65c-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ab65c-141">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="ab65c-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ab65c-142">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-142">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-143">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ab65c-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="ab65c-144">MasterType</span></span>  <br/> |<span data-ttu-id="ab65c-145">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ab65c-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ab65c-146">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-146">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-147">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ab65c-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab65c-148">Name</span></span>  <br/> |<span data-ttu-id="ab65c-149">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ab65c-149">xsd:string</span></span>  <br/> |<span data-ttu-id="ab65c-150">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-150">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-151">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ab65c-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-152">NameU</span><span class="sxs-lookup"><span data-stu-id="ab65c-152">NameU</span></span>  <br/> |<span data-ttu-id="ab65c-153">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ab65c-153">xsd:string</span></span>  <br/> |<span data-ttu-id="ab65c-154">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-154">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-155">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ab65c-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="ab65c-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="ab65c-157">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ab65c-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ab65c-158">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-158">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-159">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ab65c-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="ab65c-160">Prompt</span></span>  <br/> |<span data-ttu-id="ab65c-161">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ab65c-161">xsd:string</span></span>  <br/> |<span data-ttu-id="ab65c-162">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-162">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-163">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ab65c-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="ab65c-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="ab65c-165">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ab65c-165">xsd:string</span></span>  <br/> |<span data-ttu-id="ab65c-166">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-166">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-167">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ab65c-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ab65c-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="ab65c-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="ab65c-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ab65c-169">xsd:string</span></span>  <br/> |<span data-ttu-id="ab65c-170">opcional</span><span class="sxs-lookup"><span data-stu-id="ab65c-170">optional</span></span>  <br/> ||<span data-ttu-id="ab65c-171">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ab65c-171">Values of the xsd:string type.</span></span>  <br/> |
   

