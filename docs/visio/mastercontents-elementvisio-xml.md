---
title: Elemento MasterContents ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Especifica información acerca de las formas de un patrón en un dibujo.
ms.openlocfilehash: d1ba67a414ac80be9da2beebb93acc89faf71172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822580"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="e4dae-103">Elemento MasterContents ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e4dae-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="e4dae-104">Especifica información acerca de las formas de un patrón en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="e4dae-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e4dae-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e4dae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4dae-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e4dae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e4dae-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="e4dae-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e4dae-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e4dae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e4dae-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e4dae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e4dae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e4dae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e4dae-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e4dae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e4dae-112">maestro # .xml</span><span class="sxs-lookup"><span data-stu-id="e4dae-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e4dae-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e4dae-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e4dae-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e4dae-114">Elements and attributes</span></span>

<span data-ttu-id="e4dae-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e4dae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e4dae-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e4dae-116">Parent elements</span></span>

<span data-ttu-id="e4dae-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e4dae-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e4dae-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e4dae-118">Child elements</span></span>

|<span data-ttu-id="e4dae-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="e4dae-119">**Element**</span></span>|<span data-ttu-id="e4dae-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e4dae-120">**Type**</span></span>|<span data-ttu-id="e4dae-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4dae-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e4dae-122">Connects</span><span class="sxs-lookup"><span data-stu-id="e4dae-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e4dae-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="e4dae-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e4dae-124">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="e4dae-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="e4dae-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="e4dae-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e4dae-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e4dae-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e4dae-127">Contiene una colección de elementos de la **forma** .</span><span class="sxs-lookup"><span data-stu-id="e4dae-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e4dae-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="e4dae-128">Attributes</span></span>

<span data-ttu-id="e4dae-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e4dae-129">None.</span></span>
  

