---
title: Elemento REL (complexType Solution_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Especifica una relación con un elemento con el XML de la solución asociado a esta solución.
ms.openlocfilehash: e8a1350691e8d29551fb126a2151655175cc068c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320016"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="7cf79-103">Elemento REL (complexType Solution_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="7cf79-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7cf79-104">Especifica una relación con un elemento con el XML de la solución asociado a esta solución.</span><span class="sxs-lookup"><span data-stu-id="7cf79-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cf79-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7cf79-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cf79-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7cf79-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7cf79-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="7cf79-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7cf79-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7cf79-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7cf79-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7cf79-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7cf79-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7cf79-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7cf79-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7cf79-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7cf79-112">Pages. XML, Masters. XML, Recordsets. XML, página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="7cf79-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7cf79-113">Definición</span><span class="sxs-lookup"><span data-stu-id="7cf79-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7cf79-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7cf79-114">Elements and attributes</span></span>

<span data-ttu-id="7cf79-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7cf79-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7cf79-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7cf79-116">Parent elements</span></span>

|<span data-ttu-id="7cf79-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7cf79-117">**Element**</span></span>|<span data-ttu-id="7cf79-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7cf79-118">**Type**</span></span>|<span data-ttu-id="7cf79-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cf79-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7cf79-120">Solution</span><span class="sxs-lookup"><span data-stu-id="7cf79-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7cf79-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="7cf79-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7cf79-122">Especifica una instancia de XML de solución almacenada en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="7cf79-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7cf79-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cf79-123">Child elements</span></span>

<span data-ttu-id="7cf79-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7cf79-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cf79-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="7cf79-125">Attributes</span></span>

|<span data-ttu-id="7cf79-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7cf79-126">**Attribute**</span></span>|<span data-ttu-id="7cf79-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7cf79-127">**Type**</span></span>|<span data-ttu-id="7cf79-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7cf79-128">**Required**</span></span>|<span data-ttu-id="7cf79-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cf79-129">**Description**</span></span>|<span data-ttu-id="7cf79-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7cf79-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7cf79-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="7cf79-131">r:id</span></span>  <br/> |<span data-ttu-id="7cf79-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7cf79-132">xsd:string</span></span>  <br/> <span data-ttu-id="7cf79-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7cf79-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="7cf79-134">necesario</span><span class="sxs-lookup"><span data-stu-id="7cf79-134">required</span></span>  <br/> |<span data-ttu-id="7cf79-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="7cf79-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="7cf79-136">"Nº rId"</span><span class="sxs-lookup"><span data-stu-id="7cf79-136">"rId#"</span></span>  <br/> <span data-ttu-id="7cf79-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7cf79-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cf79-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cf79-138">Remarks</span></span>

<span data-ttu-id="7cf79-139">El valor del atributo **r:ID** debe ser un tipo **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="7cf79-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="7cf79-140">El tipo **ST_RelationshipID** es una cadena que debe tener el formato "rId #", donde el último carácter debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="7cf79-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="7cf79-141">El número debe ser único entre todos los elementos del mismo nivel del elemento **REL** .</span><span class="sxs-lookup"><span data-stu-id="7cf79-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="7cf79-142">Para obtener más información acerca del tipo ST_RelationshipID, consulte la [especificación ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="7cf79-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

