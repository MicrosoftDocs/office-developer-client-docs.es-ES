---
title: elemento de CP (Text_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca el principio de un propiedades de carácter ejecutar es decir el formato de acuerdo con el correspondiente elemento de Char. La ejecución se define al final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: 16e5bb94afeb860220c6cb49a9b98e36e45d76cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821892"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="3a8bc-104">elemento de CP (Text_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="3a8bc-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3a8bc-105">Marca el principio de un propiedades de carácter ejecutar es decir el formato de acuerdo con el correspondiente elemento de Char.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="3a8bc-106">La ejecución se define al final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a8bc-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a8bc-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a8bc-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-108">**Element type**</span></span> <br/> |[<span data-ttu-id="3a8bc-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="3a8bc-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3a8bc-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3a8bc-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-111">**Schema file**</span></span> <br/> |<span data-ttu-id="3a8bc-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3a8bc-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3a8bc-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-113">**Document parts**</span></span> <br/> |<span data-ttu-id="3a8bc-114">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="3a8bc-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3a8bc-115">Definición</span><span class="sxs-lookup"><span data-stu-id="3a8bc-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3a8bc-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3a8bc-116">Elements and attributes</span></span>

<span data-ttu-id="3a8bc-117">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3a8bc-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a8bc-118">Parent elements</span></span>

|<span data-ttu-id="3a8bc-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-119">**Element**</span></span>|<span data-ttu-id="3a8bc-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-120">**Type**</span></span>|<span data-ttu-id="3a8bc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3a8bc-122">Text</span><span class="sxs-lookup"><span data-stu-id="3a8bc-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3a8bc-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="3a8bc-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3a8bc-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3a8bc-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a8bc-125">Child elements</span></span>

<span data-ttu-id="3a8bc-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a8bc-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a8bc-127">Attributes</span></span>

|<span data-ttu-id="3a8bc-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-128">**Attribute**</span></span>|<span data-ttu-id="3a8bc-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-129">**Type**</span></span>|<span data-ttu-id="3a8bc-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-130">**Required**</span></span>|<span data-ttu-id="3a8bc-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-131">**Description**</span></span>|<span data-ttu-id="3a8bc-132">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="3a8bc-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3a8bc-133">IX</span><span class="sxs-lookup"><span data-stu-id="3a8bc-133">IX</span></span>  <br/> |<span data-ttu-id="3a8bc-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3a8bc-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3a8bc-135">necesario</span><span class="sxs-lookup"><span data-stu-id="3a8bc-135">required</span></span>  <br/> |<span data-ttu-id="3a8bc-136">El índice del elemento de Char que representa esta propiedad ejecutar.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="3a8bc-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3a8bc-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

