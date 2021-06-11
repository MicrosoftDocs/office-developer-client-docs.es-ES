---
title: Elemento Colors (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contiene la tabla de colores del documento.
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540178"
---
# <a name="colors-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="37bdf-103">Elemento Colors (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="37bdf-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="37bdf-104">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="37bdf-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37bdf-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="37bdf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37bdf-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="37bdf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="37bdf-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="37bdf-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="37bdf-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="37bdf-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="37bdf-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="37bdf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="37bdf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="37bdf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="37bdf-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="37bdf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="37bdf-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="37bdf-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37bdf-113">Definición</span><span class="sxs-lookup"><span data-stu-id="37bdf-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="37bdf-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="37bdf-114">Elements and attributes</span></span>

<span data-ttu-id="37bdf-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="37bdf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="37bdf-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="37bdf-116">Parent elements</span></span>

|<span data-ttu-id="37bdf-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37bdf-117">**Element**</span></span>|<span data-ttu-id="37bdf-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="37bdf-118">**Type**</span></span>|<span data-ttu-id="37bdf-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37bdf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37bdf-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="37bdf-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="37bdf-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="37bdf-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37bdf-122">Elemento raíz de un documento Visio Microsoft.</span><span class="sxs-lookup"><span data-stu-id="37bdf-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="37bdf-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="37bdf-123">Child elements</span></span>

|<span data-ttu-id="37bdf-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="37bdf-124">**Element**</span></span>|<span data-ttu-id="37bdf-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="37bdf-125">**Type**</span></span>|<span data-ttu-id="37bdf-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37bdf-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37bdf-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="37bdf-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37bdf-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="37bdf-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="37bdf-129">Contiene una entrada de tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="37bdf-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="37bdf-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="37bdf-130">Attributes</span></span>

<span data-ttu-id="37bdf-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="37bdf-131">None.</span></span>
  

