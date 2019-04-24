---
title: Elemento MasterContents (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Especifica información sobre las formas de un patrón en un dibujo.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341359"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="0785e-103">Elemento MasterContents (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0785e-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="0785e-104">Especifica información sobre las formas de un patrón en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="0785e-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0785e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0785e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0785e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0785e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0785e-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="0785e-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0785e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0785e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0785e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0785e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0785e-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0785e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0785e-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="0785e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0785e-112">Master #. XML</span><span class="sxs-lookup"><span data-stu-id="0785e-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0785e-113">Definición</span><span class="sxs-lookup"><span data-stu-id="0785e-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0785e-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0785e-114">Elements and attributes</span></span>

<span data-ttu-id="0785e-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0785e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0785e-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0785e-116">Parent elements</span></span>

<span data-ttu-id="0785e-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0785e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0785e-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0785e-118">Child elements</span></span>

|<span data-ttu-id="0785e-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0785e-119">**Element**</span></span>|<span data-ttu-id="0785e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0785e-120">**Type**</span></span>|<span data-ttu-id="0785e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0785e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0785e-122">Connects</span><span class="sxs-lookup"><span data-stu-id="0785e-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0785e-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="0785e-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0785e-124">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="0785e-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="0785e-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="0785e-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0785e-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="0785e-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0785e-127">Contiene una colección de elementos **Shape** .</span><span class="sxs-lookup"><span data-stu-id="0785e-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0785e-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="0785e-128">Attributes</span></span>

<span data-ttu-id="0785e-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0785e-129">None.</span></span>
  

