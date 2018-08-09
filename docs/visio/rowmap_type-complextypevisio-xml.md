---
title: RowMap_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 18f573a480e3ae057074a219def192f6b1b2829b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823061"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="7b14b-102">RowMap_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="7b14b-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b14b-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="7b14b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b14b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7b14b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b14b-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7b14b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b14b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7b14b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b14b-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="7b14b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b14b-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7b14b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b14b-109">Definición</span><span class="sxs-lookup"><span data-stu-id="7b14b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7b14b-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7b14b-110">Elements and attributes</span></span>

<span data-ttu-id="7b14b-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="7b14b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b14b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7b14b-112">Child elements</span></span>

<span data-ttu-id="7b14b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b14b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b14b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b14b-114">Attributes</span></span>

|<span data-ttu-id="7b14b-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7b14b-115">**Attribute**</span></span>|<span data-ttu-id="7b14b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b14b-116">**Type**</span></span>|<span data-ttu-id="7b14b-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7b14b-117">**Required**</span></span>|<span data-ttu-id="7b14b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b14b-118">**Description**</span></span>|<span data-ttu-id="7b14b-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="7b14b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b14b-120">PageID</span><span class="sxs-lookup"><span data-stu-id="7b14b-120">PageID</span></span>  <br/> |<span data-ttu-id="7b14b-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b14b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b14b-122">necesario</span><span class="sxs-lookup"><span data-stu-id="7b14b-122">required</span></span>  <br/> ||<span data-ttu-id="7b14b-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b14b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b14b-124">RowID</span><span class="sxs-lookup"><span data-stu-id="7b14b-124">RowID</span></span>  <br/> |<span data-ttu-id="7b14b-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b14b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b14b-126">necesario</span><span class="sxs-lookup"><span data-stu-id="7b14b-126">required</span></span>  <br/> ||<span data-ttu-id="7b14b-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b14b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7b14b-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7b14b-128">ShapeID</span></span>  <br/> |<span data-ttu-id="7b14b-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7b14b-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7b14b-130">necesario</span><span class="sxs-lookup"><span data-stu-id="7b14b-130">required</span></span>  <br/> ||<span data-ttu-id="7b14b-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7b14b-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

