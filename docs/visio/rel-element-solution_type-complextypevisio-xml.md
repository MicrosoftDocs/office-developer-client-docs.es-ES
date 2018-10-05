---
title: Elemento rel (Solution_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Especifica una relación con una parte de la solución de que XML asociado con esta solución.
ms.openlocfilehash: e8a1350691e8d29551fb126a2151655175cc068c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400792"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="7a58c-103">Elemento rel (Solution_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="7a58c-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7a58c-104">Especifica una relación con una parte de la solución de que XML asociado con esta solución.</span><span class="sxs-lookup"><span data-stu-id="7a58c-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a58c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7a58c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a58c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7a58c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7a58c-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="7a58c-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7a58c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7a58c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7a58c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7a58c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7a58c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7a58c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7a58c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7a58c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7a58c-112">Pages.XML, masters.xml, recordsets.xml, página # .xml, maestra # .xml</span><span class="sxs-lookup"><span data-stu-id="7a58c-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7a58c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="7a58c-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7a58c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7a58c-114">Elements and attributes</span></span>

<span data-ttu-id="7a58c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="7a58c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7a58c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7a58c-116">Parent elements</span></span>

|<span data-ttu-id="7a58c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a58c-117">**Element**</span></span>|<span data-ttu-id="7a58c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7a58c-118">**Type**</span></span>|<span data-ttu-id="7a58c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a58c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7a58c-120">Solution</span><span class="sxs-lookup"><span data-stu-id="7a58c-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a58c-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="7a58c-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7a58c-122">Especifica una instancia de solución de que XML se almacena en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="7a58c-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7a58c-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7a58c-123">Child elements</span></span>

<span data-ttu-id="7a58c-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7a58c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a58c-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="7a58c-125">Attributes</span></span>

|<span data-ttu-id="7a58c-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7a58c-126">**Attribute**</span></span>|<span data-ttu-id="7a58c-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7a58c-127">**Type**</span></span>|<span data-ttu-id="7a58c-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7a58c-128">**Required**</span></span>|<span data-ttu-id="7a58c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7a58c-129">**Description**</span></span>|<span data-ttu-id="7a58c-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="7a58c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7a58c-131">r: Id.</span><span class="sxs-lookup"><span data-stu-id="7a58c-131">r:id</span></span>  <br/> |<span data-ttu-id="7a58c-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7a58c-132">xsd:string</span></span>  <br/> <span data-ttu-id="7a58c-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7a58c-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="7a58c-134">necesario</span><span class="sxs-lookup"><span data-stu-id="7a58c-134">required</span></span>  <br/> |<span data-ttu-id="7a58c-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="7a58c-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="7a58c-136">"quitar #"</span><span class="sxs-lookup"><span data-stu-id="7a58c-136">"rId#"</span></span>  <br/> <span data-ttu-id="7a58c-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="7a58c-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a58c-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a58c-138">Remarks</span></span>

<span data-ttu-id="7a58c-139">El valor del atributo **id: r** debe ser un tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="7a58c-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="7a58c-140">El tipo **ST_RelationshipID** es una cadena que debe tener el formato '# deshacerse', donde el carácter final debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="7a58c-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="7a58c-141">El número debe ser único entre todos los elementos del mismo nivel del elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="7a58c-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="7a58c-142">Para obtener más información sobre el tipo de ST_RelationshipID, vea la [especificación ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="7a58c-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

