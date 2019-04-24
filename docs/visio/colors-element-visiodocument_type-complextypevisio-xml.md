---
title: Elemento Colors (VisioDocument_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contiene la tabla de colores del documento.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358761"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ad4ce-103">Elemento Colors (VisioDocument_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="ad4ce-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad4ce-104">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad4ce-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad4ce-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad4ce-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad4ce-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="ad4ce-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad4ce-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad4ce-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad4ce-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ad4ce-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad4ce-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad4ce-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="ad4ce-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad4ce-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ad4ce-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad4ce-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ad4ce-114">Elements and attributes</span></span>

<span data-ttu-id="ad4ce-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad4ce-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad4ce-116">Parent elements</span></span>

|<span data-ttu-id="ad4ce-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-117">**Element**</span></span>|<span data-ttu-id="ad4ce-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-118">**Type**</span></span>|<span data-ttu-id="ad4ce-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad4ce-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ad4ce-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ad4ce-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ad4ce-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad4ce-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad4ce-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad4ce-123">Child elements</span></span>

|<span data-ttu-id="ad4ce-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-124">**Element**</span></span>|<span data-ttu-id="ad4ce-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-125">**Type**</span></span>|<span data-ttu-id="ad4ce-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4ce-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad4ce-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="ad4ce-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad4ce-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="ad4ce-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad4ce-129">Contiene una entrada de la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad4ce-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad4ce-130">Attributes</span></span>

<span data-ttu-id="ad4ce-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad4ce-131">None.</span></span>
  

