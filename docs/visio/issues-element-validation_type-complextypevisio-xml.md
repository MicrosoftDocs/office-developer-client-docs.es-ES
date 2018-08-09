---
title: Elemento de problemas (Validation_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contiene todos los elementos de problema para el documento.
ms.openlocfilehash: 9205bf014c81aa699b8bc4a2a7412c5ce59c5fd0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822376"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="a542b-103">Elemento de problemas (Validation_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a542b-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a542b-104">Contiene todos los elementos de problema para el documento.</span><span class="sxs-lookup"><span data-stu-id="a542b-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a542b-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a542b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a542b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a542b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a542b-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="a542b-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a542b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a542b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a542b-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a542b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a542b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a542b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a542b-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a542b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a542b-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="a542b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a542b-113">Definición</span><span class="sxs-lookup"><span data-stu-id="a542b-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a542b-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a542b-114">Elements and attributes</span></span>

<span data-ttu-id="a542b-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a542b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a542b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a542b-116">Parent elements</span></span>

|<span data-ttu-id="a542b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a542b-117">**Element**</span></span>|<span data-ttu-id="a542b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a542b-118">**Type**</span></span>|<span data-ttu-id="a542b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a542b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a542b-120">Validación</span><span class="sxs-lookup"><span data-stu-id="a542b-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="a542b-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="a542b-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a542b-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="a542b-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a542b-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a542b-123">Child elements</span></span>

|<span data-ttu-id="a542b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a542b-124">**Element**</span></span>|<span data-ttu-id="a542b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a542b-125">**Type**</span></span>|<span data-ttu-id="a542b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a542b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a542b-127">Problema</span><span class="sxs-lookup"><span data-stu-id="a542b-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a542b-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="a542b-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a542b-129">Representa un problema de validación único en el documento.</span><span class="sxs-lookup"><span data-stu-id="a542b-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a542b-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="a542b-130">Attributes</span></span>

<span data-ttu-id="a542b-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a542b-131">None.</span></span>
  

