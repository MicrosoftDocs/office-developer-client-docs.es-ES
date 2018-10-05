---
title: RowMap_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401002"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="81a5d-102">RowMap_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="81a5d-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="81a5d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="81a5d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81a5d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="81a5d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="81a5d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="81a5d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="81a5d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="81a5d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="81a5d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="81a5d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="81a5d-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="81a5d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81a5d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="81a5d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="81a5d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="81a5d-110">Elements and attributes</span></span>

<span data-ttu-id="81a5d-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="81a5d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="81a5d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="81a5d-112">Child elements</span></span>

<span data-ttu-id="81a5d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="81a5d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81a5d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="81a5d-114">Attributes</span></span>

|<span data-ttu-id="81a5d-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="81a5d-115">**Attribute**</span></span>|<span data-ttu-id="81a5d-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="81a5d-116">**Type**</span></span>|<span data-ttu-id="81a5d-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="81a5d-117">**Required**</span></span>|<span data-ttu-id="81a5d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81a5d-118">**Description**</span></span>|<span data-ttu-id="81a5d-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="81a5d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="81a5d-120">PageID</span><span class="sxs-lookup"><span data-stu-id="81a5d-120">PageID</span></span>  <br/> |<span data-ttu-id="81a5d-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="81a5d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81a5d-122">necesario</span><span class="sxs-lookup"><span data-stu-id="81a5d-122">required</span></span>  <br/> ||<span data-ttu-id="81a5d-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="81a5d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="81a5d-124">RowID</span><span class="sxs-lookup"><span data-stu-id="81a5d-124">RowID</span></span>  <br/> |<span data-ttu-id="81a5d-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="81a5d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81a5d-126">necesario</span><span class="sxs-lookup"><span data-stu-id="81a5d-126">required</span></span>  <br/> ||<span data-ttu-id="81a5d-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="81a5d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="81a5d-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="81a5d-128">ShapeID</span></span>  <br/> |<span data-ttu-id="81a5d-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="81a5d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="81a5d-130">necesario</span><span class="sxs-lookup"><span data-stu-id="81a5d-130">required</span></span>  <br/> ||<span data-ttu-id="81a5d-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="81a5d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

