---
title: Elemento Colors (VisioDocument_Type complexType) (VISIO XML)
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
# <a name="colors-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="afedc-103">Elemento Colors (VisioDocument_Type complexType) (VISIO XML)</span><span class="sxs-lookup"><span data-stu-id="afedc-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="afedc-104">Contiene la tabla de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="afedc-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afedc-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afedc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afedc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="afedc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="afedc-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="afedc-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="afedc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="afedc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="afedc-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="afedc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="afedc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="afedc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="afedc-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="afedc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="afedc-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="afedc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="afedc-113">Definición</span><span class="sxs-lookup"><span data-stu-id="afedc-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="afedc-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="afedc-114">Elements and attributes</span></span>

<span data-ttu-id="afedc-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="afedc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="afedc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afedc-116">Parent elements</span></span>

|<span data-ttu-id="afedc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afedc-117">**Element**</span></span>|<span data-ttu-id="afedc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="afedc-118">**Type**</span></span>|<span data-ttu-id="afedc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afedc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afedc-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="afedc-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="afedc-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="afedc-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afedc-122">Elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="afedc-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="afedc-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afedc-123">Child elements</span></span>

|<span data-ttu-id="afedc-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afedc-124">**Element**</span></span>|<span data-ttu-id="afedc-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="afedc-125">**Type**</span></span>|<span data-ttu-id="afedc-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afedc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afedc-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="afedc-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="afedc-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="afedc-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afedc-129">Contiene una entrada de tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="afedc-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="afedc-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="afedc-130">Attributes</span></span>

<span data-ttu-id="afedc-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afedc-131">None.</span></span>
  

