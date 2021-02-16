---
title: RowMap_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: 8564f5a063ac2365de50919168df0b84e8ae100a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538777"
---
# <a name="rowmap_type-complextype-visio-xml"></a><span data-ttu-id="d5194-102">RowMap_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d5194-102">RowMap_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d5194-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d5194-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5194-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5194-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5194-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d5194-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5194-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5194-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5194-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d5194-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5194-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d5194-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5194-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d5194-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d5194-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d5194-110">Elements and attributes</span></span>

<span data-ttu-id="d5194-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d5194-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5194-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5194-112">Child elements</span></span>

<span data-ttu-id="d5194-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5194-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5194-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5194-114">Attributes</span></span>

|<span data-ttu-id="d5194-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d5194-115">**Attribute**</span></span>|<span data-ttu-id="d5194-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d5194-116">**Type**</span></span>|<span data-ttu-id="d5194-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d5194-117">**Required**</span></span>|<span data-ttu-id="d5194-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d5194-118">**Description**</span></span>|<span data-ttu-id="d5194-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="d5194-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5194-120">PageID</span><span class="sxs-lookup"><span data-stu-id="d5194-120">PageID</span></span>  <br/> |<span data-ttu-id="d5194-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5194-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5194-122">necesario</span><span class="sxs-lookup"><span data-stu-id="d5194-122">required</span></span>  <br/> ||<span data-ttu-id="d5194-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5194-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5194-124">RowID</span><span class="sxs-lookup"><span data-stu-id="d5194-124">RowID</span></span>  <br/> |<span data-ttu-id="d5194-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5194-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5194-126">necesario</span><span class="sxs-lookup"><span data-stu-id="d5194-126">required</span></span>  <br/> ||<span data-ttu-id="d5194-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5194-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5194-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="d5194-128">ShapeID</span></span>  <br/> |<span data-ttu-id="d5194-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5194-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5194-130">necesario</span><span class="sxs-lookup"><span data-stu-id="d5194-130">required</span></span>  <br/> ||<span data-ttu-id="d5194-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5194-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

