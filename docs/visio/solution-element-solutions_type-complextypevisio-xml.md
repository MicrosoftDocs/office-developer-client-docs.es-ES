---
title: Elemento Solution (complexType Solutions_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Especifica una instancia de XML de solución almacenada en el dibujo.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335269"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="acdae-103">Elemento Solution (complexType Solutions_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="acdae-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="acdae-104">Especifica una instancia de XML de solución almacenada en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="acdae-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acdae-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="acdae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acdae-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="acdae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="acdae-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="acdae-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="acdae-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="acdae-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="acdae-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="acdae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="acdae-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="acdae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="acdae-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="acdae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="acdae-112">Solutions. XML</span><span class="sxs-lookup"><span data-stu-id="acdae-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="acdae-113">Definición</span><span class="sxs-lookup"><span data-stu-id="acdae-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="acdae-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="acdae-114">Elements and attributes</span></span>

<span data-ttu-id="acdae-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="acdae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="acdae-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="acdae-116">Parent elements</span></span>

|<span data-ttu-id="acdae-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acdae-117">**Element**</span></span>|<span data-ttu-id="acdae-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acdae-118">**Type**</span></span>|<span data-ttu-id="acdae-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acdae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acdae-120">Soluciones</span><span class="sxs-lookup"><span data-stu-id="acdae-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="acdae-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="acdae-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdae-122">Almacena las propiedades de las soluciones almacenadas en el documento.</span><span class="sxs-lookup"><span data-stu-id="acdae-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="acdae-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="acdae-123">Child elements</span></span>

|<span data-ttu-id="acdae-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="acdae-124">**Element**</span></span>|<span data-ttu-id="acdae-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acdae-125">**Type**</span></span>|<span data-ttu-id="acdae-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acdae-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="acdae-127">REL</span><span class="sxs-lookup"><span data-stu-id="acdae-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="acdae-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="acdae-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="acdae-129">Especifica la relación con un elemento con el XML de la solución asociado a esta solución.</span><span class="sxs-lookup"><span data-stu-id="acdae-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="acdae-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="acdae-130">Attributes</span></span>

|<span data-ttu-id="acdae-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="acdae-131">**Attribute**</span></span>|<span data-ttu-id="acdae-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="acdae-132">**Type**</span></span>|<span data-ttu-id="acdae-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="acdae-133">**Required**</span></span>|<span data-ttu-id="acdae-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="acdae-134">**Description**</span></span>|<span data-ttu-id="acdae-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="acdae-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="acdae-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="acdae-136">Name</span></span>  <br/> |<span data-ttu-id="acdae-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="acdae-137">xsd:string</span></span>  <br/> |<span data-ttu-id="acdae-138">necesario</span><span class="sxs-lookup"><span data-stu-id="acdae-138">required</span></span>  <br/> |<span data-ttu-id="acdae-139">Nombre de la solución.</span><span class="sxs-lookup"><span data-stu-id="acdae-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="acdae-140">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="acdae-140">Values of the xsd:string type.</span></span>  <br/> |
   

