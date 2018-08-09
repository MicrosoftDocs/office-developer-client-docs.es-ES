---
title: IssueTarget_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0dde1d-5748-63ce-b0da-87f545299b38
ms.openlocfilehash: b9e69edc5bd30ede969bc77d43501a4473e9f69e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822378"
---
# <a name="issuetargettype-complextype-visio-xml"></a><span data-ttu-id="f0892-102">IssueTarget_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f0892-102">IssueTarget_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f0892-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f0892-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0892-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f0892-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f0892-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f0892-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f0892-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f0892-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f0892-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f0892-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f0892-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f0892-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0892-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f0892-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f0892-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f0892-110">Elements and attributes</span></span>

<span data-ttu-id="f0892-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f0892-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f0892-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0892-112">Child elements</span></span>

<span data-ttu-id="f0892-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0892-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0892-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0892-114">Attributes</span></span>

|<span data-ttu-id="f0892-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f0892-115">**Attribute**</span></span>|<span data-ttu-id="f0892-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0892-116">**Type**</span></span>|<span data-ttu-id="f0892-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f0892-117">**Required**</span></span>|<span data-ttu-id="f0892-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0892-118">**Description**</span></span>|<span data-ttu-id="f0892-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="f0892-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0892-120">PageID</span><span class="sxs-lookup"><span data-stu-id="f0892-120">PageID</span></span>  <br/> |<span data-ttu-id="f0892-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f0892-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f0892-122">necesario</span><span class="sxs-lookup"><span data-stu-id="f0892-122">required</span></span>  <br/> ||<span data-ttu-id="f0892-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f0892-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f0892-124">ShapeID</span><span class="sxs-lookup"><span data-stu-id="f0892-124">ShapeID</span></span>  <br/> |<span data-ttu-id="f0892-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f0892-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f0892-126">necesario</span><span class="sxs-lookup"><span data-stu-id="f0892-126">required</span></span>  <br/> ||<span data-ttu-id="f0892-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f0892-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

