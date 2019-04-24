---
title: elemento CP (complexType Text_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca el principio de una ejecución de propiedades de carácter que tiene un formato conforme al elemento char correspondiente. La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282953"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="f4715-104">elemento CP (complexType Text_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="f4715-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f4715-105">Marca el principio de una ejecución de propiedades de carácter que tiene un formato conforme al elemento char correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f4715-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="f4715-106">La ejecución se define hasta el final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f4715-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4715-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4715-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4715-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f4715-108">**Element type**</span></span> <br/> |[<span data-ttu-id="f4715-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="f4715-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f4715-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f4715-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f4715-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f4715-111">**Schema file**</span></span> <br/> |<span data-ttu-id="f4715-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="f4715-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f4715-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f4715-113">**Document parts**</span></span> <br/> |<span data-ttu-id="f4715-114">Página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="f4715-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4715-115">Definición</span><span class="sxs-lookup"><span data-stu-id="f4715-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4715-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f4715-116">Elements and attributes</span></span>

<span data-ttu-id="f4715-117">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f4715-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f4715-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4715-118">Parent elements</span></span>

|<span data-ttu-id="f4715-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f4715-119">**Element**</span></span>|<span data-ttu-id="f4715-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4715-120">**Type**</span></span>|<span data-ttu-id="f4715-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4715-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4715-122">Text</span><span class="sxs-lookup"><span data-stu-id="f4715-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4715-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="f4715-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f4715-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="f4715-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4715-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4715-125">Child elements</span></span>

<span data-ttu-id="f4715-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4715-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4715-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4715-127">Attributes</span></span>

|<span data-ttu-id="f4715-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f4715-128">**Attribute**</span></span>|<span data-ttu-id="f4715-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4715-129">**Type**</span></span>|<span data-ttu-id="f4715-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f4715-130">**Required**</span></span>|<span data-ttu-id="f4715-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4715-131">**Description**</span></span>|<span data-ttu-id="f4715-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f4715-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f4715-133">IX</span><span class="sxs-lookup"><span data-stu-id="f4715-133">IX</span></span>  <br/> |<span data-ttu-id="f4715-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f4715-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f4715-135">necesario</span><span class="sxs-lookup"><span data-stu-id="f4715-135">required</span></span>  <br/> |<span data-ttu-id="f4715-136">El índice del elemento char que esta propiedad ejecuta representa.</span><span class="sxs-lookup"><span data-stu-id="f4715-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="f4715-137">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f4715-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

