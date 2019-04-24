---
title: Elemento FaceNames (complexType VisioDocument_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contiene una colección de elementos FaceName.
ms.openlocfilehash: 5d6f2ffbf54dd04e744e85909fbc8a6bd4a387a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322585"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="99ec9-103">Elemento FaceNames (complexType VisioDocument_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="99ec9-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="99ec9-104">Contiene una colección de elementos **FaceName** .</span><span class="sxs-lookup"><span data-stu-id="99ec9-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="99ec9-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="99ec9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99ec9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="99ec9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="99ec9-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="99ec9-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="99ec9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="99ec9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="99ec9-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="99ec9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="99ec9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="99ec9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="99ec9-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="99ec9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="99ec9-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="99ec9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99ec9-113">Definición</span><span class="sxs-lookup"><span data-stu-id="99ec9-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="99ec9-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="99ec9-114">Elements and attributes</span></span>

<span data-ttu-id="99ec9-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="99ec9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="99ec9-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="99ec9-116">Parent elements</span></span>

|<span data-ttu-id="99ec9-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99ec9-117">**Element**</span></span>|<span data-ttu-id="99ec9-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99ec9-118">**Type**</span></span>|<span data-ttu-id="99ec9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99ec9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99ec9-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="99ec9-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="99ec9-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="99ec9-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="99ec9-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="99ec9-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99ec9-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99ec9-123">Child elements</span></span>

|<span data-ttu-id="99ec9-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99ec9-124">**Element**</span></span>|<span data-ttu-id="99ec9-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="99ec9-125">**Type**</span></span>|<span data-ttu-id="99ec9-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99ec9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99ec9-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="99ec9-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="99ec9-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="99ec9-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="99ec9-129">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="99ec9-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="99ec9-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="99ec9-130">Attributes</span></span>

<span data-ttu-id="99ec9-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99ec9-131">None.</span></span>
  

