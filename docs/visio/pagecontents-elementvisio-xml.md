---
title: Elemento PageContents ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.
ms.openlocfilehash: 0ca705081ad42d799a0155b26eb42ff0b64cd7d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822705"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="5b384-103">Elemento PageContents ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5b384-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="5b384-104">Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5b384-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b384-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5b384-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b384-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5b384-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5b384-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="5b384-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5b384-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b384-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5b384-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5b384-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5b384-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5b384-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5b384-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="5b384-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5b384-112">página # .xml</span><span class="sxs-lookup"><span data-stu-id="5b384-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b384-113">Definición</span><span class="sxs-lookup"><span data-stu-id="5b384-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b384-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5b384-114">Elements and attributes</span></span>

<span data-ttu-id="5b384-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5b384-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5b384-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5b384-116">Parent elements</span></span>

<span data-ttu-id="5b384-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b384-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b384-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b384-118">Child elements</span></span>

|<span data-ttu-id="5b384-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b384-119">**Element**</span></span>|<span data-ttu-id="5b384-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5b384-120">**Type**</span></span>|<span data-ttu-id="5b384-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b384-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b384-122">Connects</span><span class="sxs-lookup"><span data-stu-id="5b384-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b384-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="5b384-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b384-124">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5b384-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="5b384-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="5b384-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b384-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="5b384-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b384-127">Especifica una colección de formas.</span><span class="sxs-lookup"><span data-stu-id="5b384-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5b384-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b384-128">Attributes</span></span>

<span data-ttu-id="5b384-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b384-129">None.</span></span>
  

