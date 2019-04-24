---
title: RefreshConflict_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 25c83a8168744820fa8b570dc37bda0547ab4ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346483"
---
# <a name="refreshconflicttype-complextype-visio-xml"></a><span data-ttu-id="7d701-102">RefreshConflict_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7d701-102">RefreshConflict_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7d701-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="7d701-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d701-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7d701-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7d701-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7d701-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7d701-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7d701-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7d701-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="7d701-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7d701-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d701-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d701-109">Definición</span><span class="sxs-lookup"><span data-stu-id="7d701-109">Definition</span></span>

```XML
      <xs:complexType name="RefreshConflict_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7d701-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7d701-110">Elements and attributes</span></span>

<span data-ttu-id="7d701-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7d701-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d701-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d701-112">Child elements</span></span>

<span data-ttu-id="7d701-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7d701-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d701-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d701-114">Attributes</span></span>

|<span data-ttu-id="7d701-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7d701-115">**Attribute**</span></span>|<span data-ttu-id="7d701-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d701-116">**Type**</span></span>|<span data-ttu-id="7d701-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7d701-117">**Required**</span></span>|<span data-ttu-id="7d701-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d701-118">**Description**</span></span>|<span data-ttu-id="7d701-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7d701-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d701-120">PageID</span><span class="sxs-lookup"><span data-stu-id="7d701-120">PageID</span></span>  <br/> |<span data-ttu-id="7d701-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d701-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d701-122">necesario</span><span class="sxs-lookup"><span data-stu-id="7d701-122">required</span></span>  <br/> ||<span data-ttu-id="7d701-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d701-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d701-124">Pseudocolumna</span><span class="sxs-lookup"><span data-stu-id="7d701-124">RowID</span></span>  <br/> |<span data-ttu-id="7d701-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d701-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d701-126">necesario</span><span class="sxs-lookup"><span data-stu-id="7d701-126">required</span></span>  <br/> ||<span data-ttu-id="7d701-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d701-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7d701-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="7d701-128">ShapeID</span></span>  <br/> |<span data-ttu-id="7d701-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7d701-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7d701-130">necesario</span><span class="sxs-lookup"><span data-stu-id="7d701-130">required</span></span>  <br/> ||<span data-ttu-id="7d701-131">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7d701-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

