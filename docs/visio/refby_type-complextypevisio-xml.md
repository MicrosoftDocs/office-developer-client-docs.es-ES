---
title: RefBy_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538280"
---
# <a name="refby_type-complextype-visio-xml"></a><span data-ttu-id="c5fe8-102">RefBy_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c5fe8-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c5fe8-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c5fe8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5fe8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c5fe8-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c5fe8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c5fe8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c5fe8-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c5fe8-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c5fe8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5fe8-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c5fe8-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5fe8-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c5fe8-110">Elements and attributes</span></span>

<span data-ttu-id="c5fe8-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c5fe8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5fe8-112">Child elements</span></span>

<span data-ttu-id="c5fe8-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5fe8-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5fe8-114">Attributes</span></span>

|<span data-ttu-id="c5fe8-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-115">**Attribute**</span></span>|<span data-ttu-id="c5fe8-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-116">**Type**</span></span>|<span data-ttu-id="c5fe8-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-117">**Required**</span></span>|<span data-ttu-id="c5fe8-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-118">**Description**</span></span>|<span data-ttu-id="c5fe8-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c5fe8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5fe8-120">ID</span><span class="sxs-lookup"><span data-stu-id="c5fe8-120">ID</span></span>  <br/> |<span data-ttu-id="c5fe8-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5fe8-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5fe8-122">necesario</span><span class="sxs-lookup"><span data-stu-id="c5fe8-122">required</span></span>  <br/> ||<span data-ttu-id="c5fe8-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5fe8-124">T</span><span class="sxs-lookup"><span data-stu-id="c5fe8-124">T</span></span>  <br/> |<span data-ttu-id="c5fe8-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5fe8-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c5fe8-126">necesario</span><span class="sxs-lookup"><span data-stu-id="c5fe8-126">required</span></span>  <br/> ||<span data-ttu-id="c5fe8-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c5fe8-127">Values of the xsd:string type.</span></span>  <br/> |
   

