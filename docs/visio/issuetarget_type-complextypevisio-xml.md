---
title: IssueTarget_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: d7b8309bb6dac9648d379c89687dc89165f44edf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314927"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="1e3c7-102">IssueTarget_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1e3c7-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1e3c7-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1e3c7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e3c7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e3c7-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e3c7-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="1e3c7-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e3c7-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e3c7-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1e3c7-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e3c7-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1e3c7-109">Definition</span></span>

```XML
      <xs:complexType name="IssueTarget_Type">
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1e3c7-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1e3c7-110">Elements and attributes</span></span>

<span data-ttu-id="1e3c7-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1e3c7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e3c7-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1e3c7-112">Child elements</span></span>

<span data-ttu-id="1e3c7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1e3c7-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e3c7-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="1e3c7-114">Attributes</span></span>

|<span data-ttu-id="1e3c7-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-115">**Attribute**</span></span>|<span data-ttu-id="1e3c7-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-116">**Type**</span></span>|<span data-ttu-id="1e3c7-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-117">**Required**</span></span>|<span data-ttu-id="1e3c7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-118">**Description**</span></span>|<span data-ttu-id="1e3c7-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1e3c7-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e3c7-120">PageID</span><span class="sxs-lookup"><span data-stu-id="1e3c7-120">PageID</span></span>  <br/> |<span data-ttu-id="1e3c7-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1e3c7-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1e3c7-122">necesario</span><span class="sxs-lookup"><span data-stu-id="1e3c7-122">required</span></span>  <br/> ||<span data-ttu-id="1e3c7-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1e3c7-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1e3c7-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="1e3c7-124">ShapeID</span></span>  <br/> |<span data-ttu-id="1e3c7-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1e3c7-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1e3c7-126">necesario</span><span class="sxs-lookup"><span data-stu-id="1e3c7-126">required</span></span>  <br/> ||<span data-ttu-id="1e3c7-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1e3c7-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

