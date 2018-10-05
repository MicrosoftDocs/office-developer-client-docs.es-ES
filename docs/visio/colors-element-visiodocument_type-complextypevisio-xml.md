---
title: Elemento de colores (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contiene la tabla de colores del documento.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400533"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="44478-103">Elemento de colores (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="44478-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="44478-104">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="44478-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44478-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44478-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44478-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="44478-106">**Element type**</span></span> <br/> |[<span data-ttu-id="44478-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="44478-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="44478-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="44478-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="44478-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="44478-109">**Schema file**</span></span> <br/> |<span data-ttu-id="44478-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="44478-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="44478-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="44478-111">**Document parts**</span></span> <br/> |<span data-ttu-id="44478-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="44478-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="44478-113">Definición</span><span class="sxs-lookup"><span data-stu-id="44478-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="44478-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="44478-114">Elements and attributes</span></span>

<span data-ttu-id="44478-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="44478-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="44478-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44478-116">Parent elements</span></span>

|<span data-ttu-id="44478-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="44478-117">**Element**</span></span>|<span data-ttu-id="44478-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="44478-118">**Type**</span></span>|<span data-ttu-id="44478-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44478-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44478-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="44478-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="44478-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="44478-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44478-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="44478-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="44478-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44478-123">Child elements</span></span>

|<span data-ttu-id="44478-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="44478-124">**Element**</span></span>|<span data-ttu-id="44478-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="44478-125">**Type**</span></span>|<span data-ttu-id="44478-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44478-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44478-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="44478-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44478-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="44478-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="44478-129">Contiene una entrada de la tabla de color.</span><span class="sxs-lookup"><span data-stu-id="44478-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="44478-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="44478-130">Attributes</span></span>

<span data-ttu-id="44478-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44478-131">None.</span></span>
  

