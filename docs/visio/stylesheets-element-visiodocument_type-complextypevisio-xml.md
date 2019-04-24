---
title: Elemento StyleSheets (VisioDocument_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Contiene una colección de elementos StyleSheet para el documento.
ms.openlocfilehash: 4aae3bcbecec34d961f2d14fd6d3865e7cd332f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329788"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="e904f-103">Elemento StyleSheets (VisioDocument_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="e904f-103">StyleSheets element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e904f-104">Contiene una colección de elementos StyleSheet para el documento.</span><span class="sxs-lookup"><span data-stu-id="e904f-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e904f-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e904f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e904f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e904f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e904f-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="e904f-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e904f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e904f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e904f-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e904f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e904f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e904f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e904f-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e904f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e904f-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="e904f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e904f-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e904f-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e904f-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e904f-114">Elements and attributes</span></span>

<span data-ttu-id="e904f-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e904f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e904f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e904f-116">Parent elements</span></span>

|<span data-ttu-id="e904f-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e904f-117">**Element**</span></span>|<span data-ttu-id="e904f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e904f-118">**Type**</span></span>|<span data-ttu-id="e904f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e904f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e904f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="e904f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="e904f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="e904f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e904f-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="e904f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e904f-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e904f-123">Child elements</span></span>

|<span data-ttu-id="e904f-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e904f-124">**Element**</span></span>|<span data-ttu-id="e904f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e904f-125">**Type**</span></span>|<span data-ttu-id="e904f-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e904f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e904f-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="e904f-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e904f-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e904f-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e904f-129">Representa un estilo definido en un documento.</span><span class="sxs-lookup"><span data-stu-id="e904f-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e904f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="e904f-130">Attributes</span></span>

<span data-ttu-id="e904f-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e904f-131">None.</span></span>
  

