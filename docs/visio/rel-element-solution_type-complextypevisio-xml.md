---
title: Elemento REL (complexType Solution_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Especifica una relación con un elemento con el XML de la solución asociado a esta solución.
ms.openlocfilehash: 1fe48579da28501b74fedd507f3e44d59736ae87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542768"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="954e8-103">Elemento REL (complexType Solution_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="954e8-103">Rel element (Solution_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="954e8-104">Especifica una relación con un elemento con el XML de la solución asociado a esta solución.</span><span class="sxs-lookup"><span data-stu-id="954e8-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="954e8-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="954e8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="954e8-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="954e8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="954e8-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="954e8-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="954e8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="954e8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="954e8-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="954e8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="954e8-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="954e8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="954e8-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="954e8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="954e8-112">Pages. XML, Masters. XML, Recordsets. XML, página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="954e8-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="954e8-113">Definición</span><span class="sxs-lookup"><span data-stu-id="954e8-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="954e8-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="954e8-114">Elements and attributes</span></span>

<span data-ttu-id="954e8-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="954e8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="954e8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="954e8-116">Parent elements</span></span>

|<span data-ttu-id="954e8-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="954e8-117">**Element**</span></span>|<span data-ttu-id="954e8-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="954e8-118">**Type**</span></span>|<span data-ttu-id="954e8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="954e8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="954e8-120">Solution</span><span class="sxs-lookup"><span data-stu-id="954e8-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="954e8-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="954e8-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="954e8-122">Especifica una instancia de XML de solución almacenada en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="954e8-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="954e8-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="954e8-123">Child elements</span></span>

<span data-ttu-id="954e8-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="954e8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="954e8-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="954e8-125">Attributes</span></span>

|<span data-ttu-id="954e8-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="954e8-126">**Attribute**</span></span>|<span data-ttu-id="954e8-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="954e8-127">**Type**</span></span>|<span data-ttu-id="954e8-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="954e8-128">**Required**</span></span>|<span data-ttu-id="954e8-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="954e8-129">**Description**</span></span>|<span data-ttu-id="954e8-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="954e8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="954e8-131">r:id</span><span class="sxs-lookup"><span data-stu-id="954e8-131">r:id</span></span>  <br/> |<span data-ttu-id="954e8-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="954e8-132">xsd:string</span></span>  <br/> <span data-ttu-id="954e8-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="954e8-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="954e8-134">necesario</span><span class="sxs-lookup"><span data-stu-id="954e8-134">required</span></span>  <br/> |<span data-ttu-id="954e8-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="954e8-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="954e8-136">"Nº rId"</span><span class="sxs-lookup"><span data-stu-id="954e8-136">"rId#"</span></span>  <br/> <span data-ttu-id="954e8-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="954e8-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="954e8-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="954e8-138">Remarks</span></span>

<span data-ttu-id="954e8-139">El valor del atributo **r:ID** debe ser un tipo **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="954e8-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="954e8-140">El tipo **ST_RelationshipID** es una cadena que debe tener el formato "rId #", donde el último carácter debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="954e8-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="954e8-141">El número debe ser único entre todos los elementos del mismo nivel del elemento **REL** .</span><span class="sxs-lookup"><span data-stu-id="954e8-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="954e8-142">Para obtener más información acerca del tipo ST_RelationshipID, consulte la [especificación ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="954e8-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

