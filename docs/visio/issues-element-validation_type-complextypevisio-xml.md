---
title: Elemento Issues (Validation_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contiene todos los elementos Issue del documento.
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542943"
---
# <a name="issues-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="721d2-103">Elemento Issues (Validation_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="721d2-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="721d2-104">Contiene todos los elementos Issue del documento.</span><span class="sxs-lookup"><span data-stu-id="721d2-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="721d2-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="721d2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="721d2-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="721d2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="721d2-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="721d2-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="721d2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="721d2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="721d2-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="721d2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="721d2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="721d2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="721d2-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="721d2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="721d2-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="721d2-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="721d2-113">Definición</span><span class="sxs-lookup"><span data-stu-id="721d2-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="721d2-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="721d2-114">Elements and attributes</span></span>

<span data-ttu-id="721d2-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="721d2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="721d2-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="721d2-116">Parent elements</span></span>

|<span data-ttu-id="721d2-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="721d2-117">**Element**</span></span>|<span data-ttu-id="721d2-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="721d2-118">**Type**</span></span>|<span data-ttu-id="721d2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="721d2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="721d2-120">Validation</span><span class="sxs-lookup"><span data-stu-id="721d2-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="721d2-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="721d2-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="721d2-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="721d2-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="721d2-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="721d2-123">Child elements</span></span>

|<span data-ttu-id="721d2-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="721d2-124">**Element**</span></span>|<span data-ttu-id="721d2-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="721d2-125">**Type**</span></span>|<span data-ttu-id="721d2-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="721d2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="721d2-127">Problema</span><span class="sxs-lookup"><span data-stu-id="721d2-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="721d2-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="721d2-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="721d2-129">Representa un único problema de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="721d2-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="721d2-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="721d2-130">Attributes</span></span>

<span data-ttu-id="721d2-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="721d2-131">None.</span></span>
  

