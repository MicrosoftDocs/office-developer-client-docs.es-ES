---
title: Elemento de FaceNames (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contiene una colección de elementos de nombre de fuente.
ms.openlocfilehash: 5d6f2ffbf54dd04e744e85909fbc8a6bd4a387a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386820"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ad6f4-103">Elemento de FaceNames (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ad6f4-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad6f4-104">Contiene una colección de elementos de **nombre de fuente** .</span><span class="sxs-lookup"><span data-stu-id="ad6f4-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ad6f4-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad6f4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad6f4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad6f4-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="ad6f4-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad6f4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad6f4-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad6f4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad6f4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad6f4-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad6f4-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="ad6f4-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad6f4-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ad6f4-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad6f4-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ad6f4-114">Elements and attributes</span></span>

<span data-ttu-id="ad6f4-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad6f4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad6f4-116">Parent elements</span></span>

|<span data-ttu-id="ad6f4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-117">**Element**</span></span>|<span data-ttu-id="ad6f4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-118">**Type**</span></span>|<span data-ttu-id="ad6f4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad6f4-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ad6f4-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ad6f4-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ad6f4-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad6f4-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad6f4-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad6f4-123">Child elements</span></span>

|<span data-ttu-id="ad6f4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-124">**Element**</span></span>|<span data-ttu-id="ad6f4-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-125">**Type**</span></span>|<span data-ttu-id="ad6f4-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad6f4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad6f4-127">Nombre de fuente</span><span class="sxs-lookup"><span data-stu-id="ad6f4-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad6f4-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="ad6f4-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad6f4-129">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad6f4-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad6f4-130">Attributes</span></span>

<span data-ttu-id="ad6f4-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad6f4-131">None.</span></span>
  

