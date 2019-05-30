---
title: elemento PP (complexType Text_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Especifica el principio de un párrafo ejecutar propiedades. La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537741"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="b7aed-104">elemento PP (complexType Text_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="b7aed-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b7aed-105">Especifica el principio de un párrafo ejecutar propiedades.</span><span class="sxs-lookup"><span data-stu-id="b7aed-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="b7aed-106">La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b7aed-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7aed-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b7aed-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7aed-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b7aed-108">**Element type**</span></span> <br/> |[<span data-ttu-id="b7aed-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="b7aed-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b7aed-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b7aed-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b7aed-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b7aed-111">**Schema file**</span></span> <br/> |<span data-ttu-id="b7aed-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b7aed-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b7aed-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b7aed-113">**Document parts**</span></span> <br/> |<span data-ttu-id="b7aed-114">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="b7aed-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7aed-115">Definición</span><span class="sxs-lookup"><span data-stu-id="b7aed-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7aed-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b7aed-116">Elements and attributes</span></span>

<span data-ttu-id="b7aed-117">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b7aed-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b7aed-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b7aed-118">Parent elements</span></span>

|<span data-ttu-id="b7aed-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b7aed-119">**Element**</span></span>|<span data-ttu-id="b7aed-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7aed-120">**Type**</span></span>|<span data-ttu-id="b7aed-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7aed-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7aed-122">Text</span><span class="sxs-lookup"><span data-stu-id="b7aed-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7aed-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="b7aed-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7aed-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="b7aed-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7aed-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b7aed-125">Child elements</span></span>

<span data-ttu-id="b7aed-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b7aed-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7aed-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="b7aed-127">Attributes</span></span>

|<span data-ttu-id="b7aed-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b7aed-128">**Attribute**</span></span>|<span data-ttu-id="b7aed-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b7aed-129">**Type**</span></span>|<span data-ttu-id="b7aed-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b7aed-130">**Required**</span></span>|<span data-ttu-id="b7aed-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7aed-131">**Description**</span></span>|<span data-ttu-id="b7aed-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b7aed-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b7aed-133">IX</span><span class="sxs-lookup"><span data-stu-id="b7aed-133">IX</span></span>  <br/> |<span data-ttu-id="b7aed-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b7aed-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7aed-135">necesario</span><span class="sxs-lookup"><span data-stu-id="b7aed-135">required</span></span>  <br/> |<span data-ttu-id="b7aed-136">Índice del elemento **para** que especifica el formato que se aplica a este segmento.</span><span class="sxs-lookup"><span data-stu-id="b7aed-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="b7aed-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b7aed-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

