---
title: Elemento PageContents (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica la información acerca de las formas de un patrón o página de dibujo de un dibujo.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538000"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="d0295-103">Elemento PageContents (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="d0295-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="d0295-104">Especifica la información acerca de las formas de un patrón o página de dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d0295-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0295-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0295-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0295-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d0295-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d0295-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="d0295-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d0295-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0295-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d0295-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d0295-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d0295-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d0295-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d0295-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="d0295-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d0295-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="d0295-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0295-113">Definición</span><span class="sxs-lookup"><span data-stu-id="d0295-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0295-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d0295-114">Elements and attributes</span></span>

<span data-ttu-id="d0295-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d0295-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d0295-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0295-116">Parent elements</span></span>

<span data-ttu-id="d0295-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0295-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0295-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0295-118">Child elements</span></span>

|<span data-ttu-id="d0295-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d0295-119">**Element**</span></span>|<span data-ttu-id="d0295-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d0295-120">**Type**</span></span>|<span data-ttu-id="d0295-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0295-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0295-122">Connects</span><span class="sxs-lookup"><span data-stu-id="d0295-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0295-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="d0295-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0295-124">Contiene un **elemento Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d0295-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="d0295-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="d0295-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0295-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="d0295-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0295-127">Especifica una colección de formas.</span><span class="sxs-lookup"><span data-stu-id="d0295-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d0295-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0295-128">Attributes</span></span>

<span data-ttu-id="d0295-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0295-129">None.</span></span>
  

