---
title: Elemento rel (ForeignData_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Especifica una relación entre una forma y un elemento de documento que contiene los datos de la imagen asociados con la forma.
ms.openlocfilehash: f54cd76788d6f5d916b9ed181f309687109dd589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822936"
---
# <a name="rel-element-foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="87c4c-103">Elemento rel (ForeignData_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="87c4c-103">Rel element (ForeignData_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="87c4c-104">Especifica una relación entre una forma y un elemento de documento que contiene los datos de la imagen asociados con la forma.</span><span class="sxs-lookup"><span data-stu-id="87c4c-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87c4c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="87c4c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87c4c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="87c4c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87c4c-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="87c4c-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87c4c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87c4c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87c4c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="87c4c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87c4c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="87c4c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87c4c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="87c4c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87c4c-112">Pages.XML, masters.xml, recordsets.xml, página # .xml, maestra # .xml</span><span class="sxs-lookup"><span data-stu-id="87c4c-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87c4c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="87c4c-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87c4c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="87c4c-114">Elements and attributes</span></span>

<span data-ttu-id="87c4c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="87c4c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87c4c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="87c4c-116">Parent elements</span></span>

|<span data-ttu-id="87c4c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="87c4c-117">**Element**</span></span>|<span data-ttu-id="87c4c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87c4c-118">**Type**</span></span>|<span data-ttu-id="87c4c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87c4c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87c4c-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="87c4c-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87c4c-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="87c4c-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87c4c-122">Especifica una instancia de datos de imagen almacenados en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="87c4c-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87c4c-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87c4c-123">Child elements</span></span>

<span data-ttu-id="87c4c-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87c4c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87c4c-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="87c4c-125">Attributes</span></span>

|<span data-ttu-id="87c4c-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="87c4c-126">**Attribute**</span></span>|<span data-ttu-id="87c4c-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87c4c-127">**Type**</span></span>|<span data-ttu-id="87c4c-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="87c4c-128">**Required**</span></span>|<span data-ttu-id="87c4c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87c4c-129">**Description**</span></span>|<span data-ttu-id="87c4c-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="87c4c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87c4c-131">r: Id.</span><span class="sxs-lookup"><span data-stu-id="87c4c-131">r:id</span></span>  <br/> |<span data-ttu-id="87c4c-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="87c4c-132">xsd:string</span></span>  <br/> <span data-ttu-id="87c4c-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="87c4c-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="87c4c-134">necesario</span><span class="sxs-lookup"><span data-stu-id="87c4c-134">required</span></span>  <br/> |<span data-ttu-id="87c4c-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="87c4c-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="87c4c-136">"quitar #"</span><span class="sxs-lookup"><span data-stu-id="87c4c-136">"rId#"</span></span>  <br/> <span data-ttu-id="87c4c-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="87c4c-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87c4c-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87c4c-138">Remarks</span></span>

<span data-ttu-id="87c4c-139">El valor del atributo **id: r** debe ser un tipo de **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="87c4c-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="87c4c-140">El tipo **ST_RelationshipID** es una cadena que debe tener el formato '# deshacerse', donde el carácter final debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="87c4c-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="87c4c-141">El número debe ser único entre todos los elementos del mismo nivel del elemento **Rel** .</span><span class="sxs-lookup"><span data-stu-id="87c4c-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="87c4c-142">Para obtener más información sobre el tipo de ST_RelationshipID, vea la [especificación ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="87c4c-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

