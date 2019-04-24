---
title: Elemento PageContents (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica la información sobre las formas de una página maestra o de dibujo de un dibujo.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334513"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="5592e-103">Elemento PageContents (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5592e-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="5592e-104">Especifica la información sobre las formas de una página maestra o de dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5592e-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5592e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5592e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5592e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5592e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5592e-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="5592e-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5592e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5592e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5592e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5592e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5592e-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="5592e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5592e-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="5592e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5592e-112">Página #. XML</span><span class="sxs-lookup"><span data-stu-id="5592e-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5592e-113">Definición</span><span class="sxs-lookup"><span data-stu-id="5592e-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5592e-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5592e-114">Elements and attributes</span></span>

<span data-ttu-id="5592e-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5592e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5592e-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5592e-116">Parent elements</span></span>

<span data-ttu-id="5592e-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5592e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5592e-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5592e-118">Child elements</span></span>

|<span data-ttu-id="5592e-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5592e-119">**Element**</span></span>|<span data-ttu-id="5592e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5592e-120">**Type**</span></span>|<span data-ttu-id="5592e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5592e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5592e-122">Connects</span><span class="sxs-lookup"><span data-stu-id="5592e-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5592e-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="5592e-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5592e-124">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5592e-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="5592e-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="5592e-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5592e-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="5592e-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5592e-127">Especifica una colección de formas.</span><span class="sxs-lookup"><span data-stu-id="5592e-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5592e-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="5592e-128">Attributes</span></span>

<span data-ttu-id="5592e-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5592e-129">None.</span></span>
  

