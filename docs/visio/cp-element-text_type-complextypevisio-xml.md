---
title: elemento de CP (Text_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca el principio de un propiedades de carácter ejecutar es decir el formato de acuerdo con el correspondiente elemento de Char. La ejecución se define al final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388199"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="df38e-104">elemento de CP (Text_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="df38e-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="df38e-105">Marca el principio de un propiedades de carácter ejecutar es decir el formato de acuerdo con el correspondiente elemento de Char.</span><span class="sxs-lookup"><span data-stu-id="df38e-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="df38e-106">La ejecución se define al final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="df38e-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df38e-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="df38e-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df38e-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="df38e-108">**Element type**</span></span> <br/> |[<span data-ttu-id="df38e-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="df38e-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="df38e-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="df38e-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="df38e-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="df38e-111">**Schema file**</span></span> <br/> |<span data-ttu-id="df38e-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="df38e-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="df38e-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="df38e-113">**Document parts**</span></span> <br/> |<span data-ttu-id="df38e-114">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="df38e-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df38e-115">Definición</span><span class="sxs-lookup"><span data-stu-id="df38e-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df38e-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="df38e-116">Elements and attributes</span></span>

<span data-ttu-id="df38e-117">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="df38e-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="df38e-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="df38e-118">Parent elements</span></span>

|<span data-ttu-id="df38e-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="df38e-119">**Element**</span></span>|<span data-ttu-id="df38e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df38e-120">**Type**</span></span>|<span data-ttu-id="df38e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df38e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df38e-122">Text</span><span class="sxs-lookup"><span data-stu-id="df38e-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df38e-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="df38e-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df38e-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="df38e-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df38e-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df38e-125">Child elements</span></span>

<span data-ttu-id="df38e-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df38e-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df38e-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="df38e-127">Attributes</span></span>

|<span data-ttu-id="df38e-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="df38e-128">**Attribute**</span></span>|<span data-ttu-id="df38e-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df38e-129">**Type**</span></span>|<span data-ttu-id="df38e-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="df38e-130">**Required**</span></span>|<span data-ttu-id="df38e-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df38e-131">**Description**</span></span>|<span data-ttu-id="df38e-132">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="df38e-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="df38e-133">IX</span><span class="sxs-lookup"><span data-stu-id="df38e-133">IX</span></span>  <br/> |<span data-ttu-id="df38e-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="df38e-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="df38e-135">necesario</span><span class="sxs-lookup"><span data-stu-id="df38e-135">required</span></span>  <br/> |<span data-ttu-id="df38e-136">El índice del elemento de Char que representa esta propiedad ejecutar.</span><span class="sxs-lookup"><span data-stu-id="df38e-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="df38e-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="df38e-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

