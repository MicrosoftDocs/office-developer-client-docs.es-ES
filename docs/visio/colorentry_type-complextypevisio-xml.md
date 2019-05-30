---
title: ComplexType ColorEntry_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d56b6110-634d-02d8-cf11-7902a2aaaf49
ms.openlocfilehash: f5ada3fef8d50c2e53f63c797601980f88349868
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540150"
---
# <a name="colorentrytype-complextype-visio-xml"></a><span data-ttu-id="6870d-102">ComplexType ColorEntry_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="6870d-102">ColorEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6870d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6870d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6870d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6870d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6870d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6870d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6870d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6870d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6870d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6870d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6870d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6870d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6870d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6870d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6870d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6870d-110">Elements and attributes</span></span>

<span data-ttu-id="6870d-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6870d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6870d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6870d-112">Child elements</span></span>

<span data-ttu-id="6870d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6870d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6870d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6870d-114">Attributes</span></span>

|<span data-ttu-id="6870d-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6870d-115">**Attribute**</span></span>|<span data-ttu-id="6870d-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6870d-116">**Type**</span></span>|<span data-ttu-id="6870d-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6870d-117">**Required**</span></span>|<span data-ttu-id="6870d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6870d-118">**Description**</span></span>|<span data-ttu-id="6870d-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="6870d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6870d-120">IX</span><span class="sxs-lookup"><span data-stu-id="6870d-120">IX</span></span>  <br/> |<span data-ttu-id="6870d-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6870d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6870d-122">necesario</span><span class="sxs-lookup"><span data-stu-id="6870d-122">required</span></span>  <br/> ||<span data-ttu-id="6870d-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6870d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6870d-124">RGB</span><span class="sxs-lookup"><span data-stu-id="6870d-124">RGB</span></span>  <br/> |<span data-ttu-id="6870d-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6870d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="6870d-126">necesario</span><span class="sxs-lookup"><span data-stu-id="6870d-126">required</span></span>  <br/> ||<span data-ttu-id="6870d-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6870d-127">Values of the xsd:string type.</span></span>  <br/> |
   

