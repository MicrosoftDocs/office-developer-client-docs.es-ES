---
title: RefreshConflict_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec7677f-a761-804c-6a12-731df86481a8
ms.openlocfilehash: 7b52bc87af213e9c26f4bc359adf6cf900b34957
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542831"
---
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="c5205-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c5205-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c5205-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c5205-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5205-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c5205-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c5205-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c5205-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c5205-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c5205-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c5205-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c5205-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c5205-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c5205-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5205-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c5205-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c5205-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c5205-110">Elements and attributes</span></span>

<span data-ttu-id="c5205-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c5205-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c5205-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5205-112">Child elements</span></span>

<span data-ttu-id="c5205-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c5205-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5205-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5205-114">Attributes</span></span>

|<span data-ttu-id="c5205-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c5205-115">**Attribute**</span></span>|<span data-ttu-id="c5205-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c5205-116">**Type**</span></span>|<span data-ttu-id="c5205-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c5205-117">**Required**</span></span>|<span data-ttu-id="c5205-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5205-118">**Description**</span></span>|<span data-ttu-id="c5205-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c5205-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5205-120">PageID</span><span class="sxs-lookup"><span data-stu-id="c5205-120">PageID</span></span>  <br/> |<span data-ttu-id="c5205-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5205-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5205-122">necesario</span><span class="sxs-lookup"><span data-stu-id="c5205-122">required</span></span>  <br/> ||<span data-ttu-id="c5205-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5205-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5205-124">RowID</span><span class="sxs-lookup"><span data-stu-id="c5205-124">RowID</span></span>  <br/> |<span data-ttu-id="c5205-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5205-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5205-126">necesario</span><span class="sxs-lookup"><span data-stu-id="c5205-126">required</span></span>  <br/> ||<span data-ttu-id="c5205-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5205-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5205-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="c5205-128">ShapeID</span></span>  <br/> |<span data-ttu-id="c5205-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5205-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5205-130">necesario</span><span class="sxs-lookup"><span data-stu-id="c5205-130">required</span></span>  <br/> ||<span data-ttu-id="c5205-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5205-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

