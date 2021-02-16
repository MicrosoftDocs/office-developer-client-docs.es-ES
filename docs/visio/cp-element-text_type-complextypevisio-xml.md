---
title: Elemento cp (Text_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Marca el principio de una ejecución de propiedades de carácter con formato según el elemento Char correspondiente. La ejecución se define al final del texto o hasta la siguiente etiqueta.
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540563"
---
# <a name="cp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="3293f-104">Elemento cp (Text_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="3293f-104">cp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3293f-105">Marca el principio de una ejecución de propiedades de carácter con formato según el elemento Char correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3293f-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="3293f-106">La ejecución se define al final del texto o hasta la siguiente etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3293f-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3293f-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3293f-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3293f-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3293f-108">**Element type**</span></span> <br/> |[<span data-ttu-id="3293f-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="3293f-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3293f-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3293f-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3293f-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3293f-111">**Schema file**</span></span> <br/> |<span data-ttu-id="3293f-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3293f-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3293f-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="3293f-113">**Document parts**</span></span> <br/> |<span data-ttu-id="3293f-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="3293f-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3293f-115">Definición</span><span class="sxs-lookup"><span data-stu-id="3293f-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3293f-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3293f-116">Elements and attributes</span></span>

<span data-ttu-id="3293f-117">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="3293f-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3293f-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3293f-118">Parent elements</span></span>

|<span data-ttu-id="3293f-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3293f-119">**Element**</span></span>|<span data-ttu-id="3293f-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3293f-120">**Type**</span></span>|<span data-ttu-id="3293f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3293f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3293f-122">Text</span><span class="sxs-lookup"><span data-stu-id="3293f-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3293f-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="3293f-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3293f-124">Contiene el texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="3293f-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3293f-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3293f-125">Child elements</span></span>

<span data-ttu-id="3293f-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3293f-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3293f-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="3293f-127">Attributes</span></span>

|<span data-ttu-id="3293f-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3293f-128">**Attribute**</span></span>|<span data-ttu-id="3293f-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3293f-129">**Type**</span></span>|<span data-ttu-id="3293f-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3293f-130">**Required**</span></span>|<span data-ttu-id="3293f-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3293f-131">**Description**</span></span>|<span data-ttu-id="3293f-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="3293f-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3293f-133">IX</span><span class="sxs-lookup"><span data-stu-id="3293f-133">IX</span></span>  <br/> |<span data-ttu-id="3293f-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3293f-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3293f-135">necesario</span><span class="sxs-lookup"><span data-stu-id="3293f-135">required</span></span>  <br/> |<span data-ttu-id="3293f-136">Índice del elemento Char que representa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3293f-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="3293f-137">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3293f-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

