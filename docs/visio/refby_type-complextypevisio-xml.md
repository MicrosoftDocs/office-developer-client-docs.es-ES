---
title: RefBy_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383488"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="68e6c-102">RefBy_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="68e6c-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="68e6c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="68e6c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68e6c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68e6c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="68e6c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="68e6c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="68e6c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="68e6c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="68e6c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="68e6c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="68e6c-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="68e6c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68e6c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="68e6c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="68e6c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="68e6c-110">Elements and attributes</span></span>

<span data-ttu-id="68e6c-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="68e6c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="68e6c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="68e6c-112">Child elements</span></span>

<span data-ttu-id="68e6c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="68e6c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68e6c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="68e6c-114">Attributes</span></span>

|<span data-ttu-id="68e6c-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="68e6c-115">**Attribute**</span></span>|<span data-ttu-id="68e6c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="68e6c-116">**Type**</span></span>|<span data-ttu-id="68e6c-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="68e6c-117">**Required**</span></span>|<span data-ttu-id="68e6c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68e6c-118">**Description**</span></span>|<span data-ttu-id="68e6c-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="68e6c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68e6c-120">ID</span><span class="sxs-lookup"><span data-stu-id="68e6c-120">ID</span></span>  <br/> |<span data-ttu-id="68e6c-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="68e6c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="68e6c-122">necesario</span><span class="sxs-lookup"><span data-stu-id="68e6c-122">required</span></span>  <br/> ||<span data-ttu-id="68e6c-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="68e6c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="68e6c-124">T</span><span class="sxs-lookup"><span data-stu-id="68e6c-124">T</span></span>  <br/> |<span data-ttu-id="68e6c-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="68e6c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="68e6c-126">necesario</span><span class="sxs-lookup"><span data-stu-id="68e6c-126">required</span></span>  <br/> ||<span data-ttu-id="68e6c-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="68e6c-127">Values of the xsd:string type.</span></span>  <br/> |
   

