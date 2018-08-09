---
title: Elemento de FaceNames (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contiene una colección de elementos de nombre de fuente.
ms.openlocfilehash: 1c031d589883f34bbf9d69a3d537b82e1ecf3129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822115"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="86716-103">Elemento de FaceNames (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="86716-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="86716-104">Contiene una colección de elementos de **nombre de fuente** .</span><span class="sxs-lookup"><span data-stu-id="86716-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="86716-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86716-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86716-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="86716-106">**Element type**</span></span> <br/> |[<span data-ttu-id="86716-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="86716-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="86716-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="86716-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="86716-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="86716-109">**Schema file**</span></span> <br/> |<span data-ttu-id="86716-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="86716-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="86716-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="86716-111">**Document parts**</span></span> <br/> |<span data-ttu-id="86716-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="86716-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86716-113">Definición</span><span class="sxs-lookup"><span data-stu-id="86716-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="86716-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="86716-114">Elements and attributes</span></span>

<span data-ttu-id="86716-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="86716-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="86716-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86716-116">Parent elements</span></span>

|<span data-ttu-id="86716-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="86716-117">**Element**</span></span>|<span data-ttu-id="86716-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="86716-118">**Type**</span></span>|<span data-ttu-id="86716-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86716-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86716-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="86716-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="86716-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="86716-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86716-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="86716-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86716-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86716-123">Child elements</span></span>

|<span data-ttu-id="86716-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="86716-124">**Element**</span></span>|<span data-ttu-id="86716-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="86716-125">**Type**</span></span>|<span data-ttu-id="86716-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86716-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86716-127">Nombre de fuente</span><span class="sxs-lookup"><span data-stu-id="86716-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86716-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="86716-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86716-129">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="86716-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="86716-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="86716-130">Attributes</span></span>

<span data-ttu-id="86716-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="86716-131">None.</span></span>
  

