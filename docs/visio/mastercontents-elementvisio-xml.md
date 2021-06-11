---
title: Elemento MasterContents (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Especifica información sobre las formas de un patrón de un dibujo.
ms.openlocfilehash: 26bc86aedeb96544f61f53052ab723b13b29500d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538042"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="e8bf5-103">Elemento MasterContents (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e8bf5-103">MasterContents element (Visio XML)</span></span>

<span data-ttu-id="e8bf5-104">Especifica información sobre las formas de un patrón de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="e8bf5-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e8bf5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8bf5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8bf5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e8bf5-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="e8bf5-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e8bf5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e8bf5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e8bf5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e8bf5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e8bf5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e8bf5-112">master#.xml</span><span class="sxs-lookup"><span data-stu-id="e8bf5-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e8bf5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e8bf5-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e8bf5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e8bf5-114">Elements and attributes</span></span>

<span data-ttu-id="e8bf5-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e8bf5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e8bf5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8bf5-116">Parent elements</span></span>

<span data-ttu-id="e8bf5-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8bf5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8bf5-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8bf5-118">Child elements</span></span>

|<span data-ttu-id="e8bf5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-119">**Element**</span></span>|<span data-ttu-id="e8bf5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-120">**Type**</span></span>|<span data-ttu-id="e8bf5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e8bf5-122">Connects</span><span class="sxs-lookup"><span data-stu-id="e8bf5-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e8bf5-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="e8bf5-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e8bf5-124">Contiene un **Conectar** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="e8bf5-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="e8bf5-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="e8bf5-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e8bf5-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e8bf5-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e8bf5-127">Contiene una colección de **elementos Shape.**</span><span class="sxs-lookup"><span data-stu-id="e8bf5-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e8bf5-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8bf5-128">Attributes</span></span>

<span data-ttu-id="e8bf5-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8bf5-129">None.</span></span>
  

