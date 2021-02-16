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
# <a name="refreshconflict_type-complextype-visio-xml"></a><span data-ttu-id="1ac27-102">RefreshConflict_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1ac27-102">RefreshConflict_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1ac27-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1ac27-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ac27-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ac27-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ac27-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1ac27-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ac27-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1ac27-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ac27-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1ac27-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ac27-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1ac27-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ac27-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1ac27-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1ac27-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1ac27-110">Elements and attributes</span></span>

<span data-ttu-id="1ac27-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1ac27-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ac27-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ac27-112">Child elements</span></span>

<span data-ttu-id="1ac27-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ac27-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ac27-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ac27-114">Attributes</span></span>

|<span data-ttu-id="1ac27-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1ac27-115">**Attribute**</span></span>|<span data-ttu-id="1ac27-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ac27-116">**Type**</span></span>|<span data-ttu-id="1ac27-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1ac27-117">**Required**</span></span>|<span data-ttu-id="1ac27-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ac27-118">**Description**</span></span>|<span data-ttu-id="1ac27-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1ac27-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ac27-120">PageID</span><span class="sxs-lookup"><span data-stu-id="1ac27-120">PageID</span></span>  <br/> |<span data-ttu-id="1ac27-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ac27-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ac27-122">necesario</span><span class="sxs-lookup"><span data-stu-id="1ac27-122">required</span></span>  <br/> ||<span data-ttu-id="1ac27-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1ac27-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1ac27-124">RowID</span><span class="sxs-lookup"><span data-stu-id="1ac27-124">RowID</span></span>  <br/> |<span data-ttu-id="1ac27-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ac27-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ac27-126">necesario</span><span class="sxs-lookup"><span data-stu-id="1ac27-126">required</span></span>  <br/> ||<span data-ttu-id="1ac27-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1ac27-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1ac27-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="1ac27-128">ShapeID</span></span>  <br/> |<span data-ttu-id="1ac27-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ac27-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ac27-130">necesario</span><span class="sxs-lookup"><span data-stu-id="1ac27-130">required</span></span>  <br/> ||<span data-ttu-id="1ac27-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1ac27-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

