---
title: Elemento de problemas (Validation_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contiene todos los elementos de problema para el documento.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400582"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="11cf9-103">Elemento de problemas (Validation_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="11cf9-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="11cf9-104">Contiene todos los elementos de problema para el documento.</span><span class="sxs-lookup"><span data-stu-id="11cf9-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11cf9-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="11cf9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11cf9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="11cf9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="11cf9-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="11cf9-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="11cf9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11cf9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="11cf9-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="11cf9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="11cf9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="11cf9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="11cf9-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="11cf9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="11cf9-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="11cf9-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11cf9-113">Definición</span><span class="sxs-lookup"><span data-stu-id="11cf9-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11cf9-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="11cf9-114">Elements and attributes</span></span>

<span data-ttu-id="11cf9-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="11cf9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="11cf9-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="11cf9-116">Parent elements</span></span>

|<span data-ttu-id="11cf9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="11cf9-117">**Element**</span></span>|<span data-ttu-id="11cf9-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="11cf9-118">**Type**</span></span>|<span data-ttu-id="11cf9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11cf9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11cf9-120">Validación</span><span class="sxs-lookup"><span data-stu-id="11cf9-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="11cf9-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="11cf9-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="11cf9-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="11cf9-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="11cf9-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11cf9-123">Child elements</span></span>

|<span data-ttu-id="11cf9-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="11cf9-124">**Element**</span></span>|<span data-ttu-id="11cf9-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="11cf9-125">**Type**</span></span>|<span data-ttu-id="11cf9-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11cf9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="11cf9-127">Problema</span><span class="sxs-lookup"><span data-stu-id="11cf9-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="11cf9-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="11cf9-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="11cf9-129">Representa un problema de validación único en el documento.</span><span class="sxs-lookup"><span data-stu-id="11cf9-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="11cf9-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="11cf9-130">Attributes</span></span>

<span data-ttu-id="11cf9-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="11cf9-131">None.</span></span>
  

