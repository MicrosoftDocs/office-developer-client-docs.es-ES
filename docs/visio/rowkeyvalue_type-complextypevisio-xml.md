---
title: RowKeyValue_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: dcd4c972aac1e86fa7a66766a756ebef2cca7c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823056"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="bf34a-102">RowKeyValue_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="bf34a-102">RowKeyValue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bf34a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="bf34a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf34a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bf34a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bf34a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bf34a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bf34a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bf34a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bf34a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="bf34a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bf34a-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bf34a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf34a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="bf34a-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bf34a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bf34a-110">Elements and attributes</span></span>

<span data-ttu-id="bf34a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="bf34a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bf34a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf34a-112">Child elements</span></span>

<span data-ttu-id="bf34a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bf34a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf34a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf34a-114">Attributes</span></span>

|<span data-ttu-id="bf34a-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="bf34a-115">**Attribute**</span></span>|<span data-ttu-id="bf34a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bf34a-116">**Type**</span></span>|<span data-ttu-id="bf34a-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="bf34a-117">**Required**</span></span>|<span data-ttu-id="bf34a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bf34a-118">**Description**</span></span>|<span data-ttu-id="bf34a-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="bf34a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bf34a-120">RowID</span><span class="sxs-lookup"><span data-stu-id="bf34a-120">RowID</span></span>  <br/> |<span data-ttu-id="bf34a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bf34a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bf34a-122">necesario</span><span class="sxs-lookup"><span data-stu-id="bf34a-122">required</span></span>  <br/> ||<span data-ttu-id="bf34a-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bf34a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bf34a-124">Value</span><span class="sxs-lookup"><span data-stu-id="bf34a-124">Value</span></span>  <br/> |<span data-ttu-id="bf34a-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bf34a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="bf34a-126">necesario</span><span class="sxs-lookup"><span data-stu-id="bf34a-126">required</span></span>  <br/> ||<span data-ttu-id="bf34a-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="bf34a-127">Values of the xsd:string type.</span></span>  <br/> |
   

