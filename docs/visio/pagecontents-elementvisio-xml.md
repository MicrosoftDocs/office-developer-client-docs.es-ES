---
title: Elemento PageContents ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396571"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="72283-103">Elemento PageContents ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="72283-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="72283-104">Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="72283-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72283-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="72283-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72283-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="72283-106">**Element type**</span></span> <br/> |[<span data-ttu-id="72283-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="72283-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="72283-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="72283-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="72283-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="72283-109">**Schema file**</span></span> <br/> |<span data-ttu-id="72283-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="72283-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="72283-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="72283-111">**Document parts**</span></span> <br/> |<span data-ttu-id="72283-112">página # .xml</span><span class="sxs-lookup"><span data-stu-id="72283-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72283-113">Definición</span><span class="sxs-lookup"><span data-stu-id="72283-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="72283-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="72283-114">Elements and attributes</span></span>

<span data-ttu-id="72283-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="72283-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="72283-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="72283-116">Parent elements</span></span>

<span data-ttu-id="72283-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72283-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="72283-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72283-118">Child elements</span></span>

|<span data-ttu-id="72283-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="72283-119">**Element**</span></span>|<span data-ttu-id="72283-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="72283-120">**Type**</span></span>|<span data-ttu-id="72283-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72283-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72283-122">Connects</span><span class="sxs-lookup"><span data-stu-id="72283-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72283-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="72283-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="72283-124">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="72283-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="72283-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="72283-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72283-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="72283-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="72283-127">Especifica una colección de formas.</span><span class="sxs-lookup"><span data-stu-id="72283-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="72283-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="72283-128">Attributes</span></span>

<span data-ttu-id="72283-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72283-129">None.</span></span>
  

