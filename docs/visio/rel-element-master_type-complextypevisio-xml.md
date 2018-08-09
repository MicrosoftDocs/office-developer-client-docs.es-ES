---
title: Elemento rel (Master_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Especifica una relación con un elemento con el XML principal correspondiente.
ms.openlocfilehash: 8cd16c55b24cd6edec993cb913709beff72ee325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822931"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="b82fa-103">Elemento rel (Master_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b82fa-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b82fa-104">Especifica una relación con un elemento con el XML principal correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b82fa-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b82fa-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b82fa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b82fa-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b82fa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b82fa-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="b82fa-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b82fa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b82fa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b82fa-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b82fa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b82fa-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b82fa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b82fa-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b82fa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b82fa-112">Pages.XML, masters.xml, recordsets.xml, página # .xml, maestra # .xml</span><span class="sxs-lookup"><span data-stu-id="b82fa-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b82fa-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b82fa-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b82fa-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b82fa-114">Elements and attributes</span></span>

<span data-ttu-id="b82fa-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b82fa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b82fa-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b82fa-116">Parent elements</span></span>

|<span data-ttu-id="b82fa-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b82fa-117">**Element**</span></span>|<span data-ttu-id="b82fa-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b82fa-118">**Type**</span></span>|<span data-ttu-id="b82fa-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b82fa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b82fa-120">Master</span><span class="sxs-lookup"><span data-stu-id="b82fa-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b82fa-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="b82fa-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b82fa-122">Especifica una instancia de XML maestra almacenadas en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="b82fa-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b82fa-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b82fa-123">Child elements</span></span>

<span data-ttu-id="b82fa-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b82fa-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b82fa-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="b82fa-125">Attributes</span></span>

|<span data-ttu-id="b82fa-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b82fa-126">**Attribute**</span></span>|<span data-ttu-id="b82fa-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b82fa-127">**Type**</span></span>|<span data-ttu-id="b82fa-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b82fa-128">**Required**</span></span>|<span data-ttu-id="b82fa-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b82fa-129">**Description**</span></span>|<span data-ttu-id="b82fa-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="b82fa-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b82fa-131">r: Id.</span><span class="sxs-lookup"><span data-stu-id="b82fa-131">r:id</span></span>  <br/> |<span data-ttu-id="b82fa-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b82fa-132">xsd:string</span></span>  <br/> <span data-ttu-id="b82fa-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b82fa-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="b82fa-134">necesario</span><span class="sxs-lookup"><span data-stu-id="b82fa-134">required</span></span>  <br/> |<span data-ttu-id="b82fa-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="b82fa-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="b82fa-136">"quitar #"</span><span class="sxs-lookup"><span data-stu-id="b82fa-136">"rId#"</span></span>  <br/> <span data-ttu-id="b82fa-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b82fa-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b82fa-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b82fa-138">Remarks</span></span>

<span data-ttu-id="b82fa-139">El valor del atributo **id: r** debe ser un tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="b82fa-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="b82fa-140">El tipo **ST_RelationshipID** es una cadena que debe tener el formato '# deshacerse', donde el carácter final debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="b82fa-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="b82fa-141">El número debe ser único entre todos los elementos del mismo nivel del elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="b82fa-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="b82fa-142">Para obtener más información sobre el tipo de ST_RelationshipID, vea la [especificación ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="b82fa-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

