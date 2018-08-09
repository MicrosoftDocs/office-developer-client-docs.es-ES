---
title: ColorEntry_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: 58a0abdd4f7f8c2014ec8c6763441840a07b93db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821771"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="062ca-102">ColorEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="062ca-102">ColorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="062ca-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="062ca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="062ca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="062ca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="062ca-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="062ca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="062ca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="062ca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="062ca-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="062ca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="062ca-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="062ca-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="062ca-109">Definición</span><span class="sxs-lookup"><span data-stu-id="062ca-109">Definition</span></span>

```XML
      <xs:complexType name="ColorEntry_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RGB"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="062ca-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="062ca-110">Elements and attributes</span></span>

<span data-ttu-id="062ca-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="062ca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="062ca-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="062ca-112">Child elements</span></span>

<span data-ttu-id="062ca-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="062ca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="062ca-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="062ca-114">Attributes</span></span>

|<span data-ttu-id="062ca-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="062ca-115">**Attribute**</span></span>|<span data-ttu-id="062ca-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="062ca-116">**Type**</span></span>|<span data-ttu-id="062ca-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="062ca-117">**Required**</span></span>|<span data-ttu-id="062ca-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="062ca-118">**Description**</span></span>|<span data-ttu-id="062ca-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="062ca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="062ca-120">IX</span><span class="sxs-lookup"><span data-stu-id="062ca-120">IX</span></span>  <br/> |<span data-ttu-id="062ca-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="062ca-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="062ca-122">necesario</span><span class="sxs-lookup"><span data-stu-id="062ca-122">required</span></span>  <br/> ||<span data-ttu-id="062ca-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="062ca-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="062ca-124">RGB</span><span class="sxs-lookup"><span data-stu-id="062ca-124">RGB</span></span>  <br/> |<span data-ttu-id="062ca-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="062ca-125">xsd:string</span></span>  <br/> |<span data-ttu-id="062ca-126">necesario</span><span class="sxs-lookup"><span data-stu-id="062ca-126">required</span></span>  <br/> ||<span data-ttu-id="062ca-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="062ca-127">Values of the xsd:string type.</span></span>  <br/> |
   

