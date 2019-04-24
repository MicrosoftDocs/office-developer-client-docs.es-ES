---
title: RowMap_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355737"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="9f0bb-102">RowMap_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9f0bb-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9f0bb-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9f0bb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f0bb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9f0bb-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9f0bb-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9f0bb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9f0bb-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9f0bb-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9f0bb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f0bb-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9f0bb-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
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

## <a name="elements-and-attributes"></a><span data-ttu-id="9f0bb-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9f0bb-110">Elements and attributes</span></span>

<span data-ttu-id="9f0bb-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9f0bb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9f0bb-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f0bb-112">Child elements</span></span>

<span data-ttu-id="9f0bb-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9f0bb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9f0bb-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f0bb-114">Attributes</span></span>

|<span data-ttu-id="9f0bb-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-115">**Attribute**</span></span>|<span data-ttu-id="9f0bb-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-116">**Type**</span></span>|<span data-ttu-id="9f0bb-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-117">**Required**</span></span>|<span data-ttu-id="9f0bb-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-118">**Description**</span></span>|<span data-ttu-id="9f0bb-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9f0bb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9f0bb-120">PageID</span><span class="sxs-lookup"><span data-stu-id="9f0bb-120">PageID</span></span>  <br/> |<span data-ttu-id="9f0bb-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f0bb-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f0bb-122">necesario</span><span class="sxs-lookup"><span data-stu-id="9f0bb-122">required</span></span>  <br/> ||<span data-ttu-id="9f0bb-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9f0bb-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f0bb-124">Pseudocolumna</span><span class="sxs-lookup"><span data-stu-id="9f0bb-124">RowID</span></span>  <br/> |<span data-ttu-id="9f0bb-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f0bb-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f0bb-126">necesario</span><span class="sxs-lookup"><span data-stu-id="9f0bb-126">required</span></span>  <br/> ||<span data-ttu-id="9f0bb-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9f0bb-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9f0bb-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="9f0bb-128">ShapeID</span></span>  <br/> |<span data-ttu-id="9f0bb-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9f0bb-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9f0bb-130">necesario</span><span class="sxs-lookup"><span data-stu-id="9f0bb-130">required</span></span>  <br/> ||<span data-ttu-id="9f0bb-131">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9f0bb-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

