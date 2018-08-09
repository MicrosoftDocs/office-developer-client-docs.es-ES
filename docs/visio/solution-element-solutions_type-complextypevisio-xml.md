---
title: Elemento Solution (Solutions_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Especifica una instancia de solución de que XML se almacena en el dibujo.
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823294"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="116cd-103">Elemento Solution (Solutions_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="116cd-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="116cd-104">Especifica una instancia de solución de que XML se almacena en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="116cd-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="116cd-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="116cd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="116cd-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="116cd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="116cd-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="116cd-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="116cd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="116cd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="116cd-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="116cd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="116cd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="116cd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="116cd-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="116cd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="116cd-112">Solutions.Xml</span><span class="sxs-lookup"><span data-stu-id="116cd-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="116cd-113">Definición</span><span class="sxs-lookup"><span data-stu-id="116cd-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="116cd-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="116cd-114">Elements and attributes</span></span>

<span data-ttu-id="116cd-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="116cd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="116cd-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="116cd-116">Parent elements</span></span>

|<span data-ttu-id="116cd-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="116cd-117">**Element**</span></span>|<span data-ttu-id="116cd-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="116cd-118">**Type**</span></span>|<span data-ttu-id="116cd-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="116cd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="116cd-120">Soluciones</span><span class="sxs-lookup"><span data-stu-id="116cd-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="116cd-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="116cd-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="116cd-122">Almacena las propiedades de las soluciones que se almacenan en el documento.</span><span class="sxs-lookup"><span data-stu-id="116cd-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="116cd-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="116cd-123">Child elements</span></span>

|<span data-ttu-id="116cd-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="116cd-124">**Element**</span></span>|<span data-ttu-id="116cd-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="116cd-125">**Type**</span></span>|<span data-ttu-id="116cd-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="116cd-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="116cd-127">Rel</span><span class="sxs-lookup"><span data-stu-id="116cd-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="116cd-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="116cd-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="116cd-129">Especifica la relación con una parte de la solución de que XML asociado con esta solución.</span><span class="sxs-lookup"><span data-stu-id="116cd-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="116cd-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="116cd-130">Attributes</span></span>

|<span data-ttu-id="116cd-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="116cd-131">**Attribute**</span></span>|<span data-ttu-id="116cd-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="116cd-132">**Type**</span></span>|<span data-ttu-id="116cd-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="116cd-133">**Required**</span></span>|<span data-ttu-id="116cd-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="116cd-134">**Description**</span></span>|<span data-ttu-id="116cd-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="116cd-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="116cd-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="116cd-136">Name</span></span>  <br/> |<span data-ttu-id="116cd-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="116cd-137">xsd:string</span></span>  <br/> |<span data-ttu-id="116cd-138">necesario</span><span class="sxs-lookup"><span data-stu-id="116cd-138">required</span></span>  <br/> |<span data-ttu-id="116cd-139">El nombre de la solución.</span><span class="sxs-lookup"><span data-stu-id="116cd-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="116cd-140">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="116cd-140">Values of the xsd:string type.</span></span>  <br/> |
   

