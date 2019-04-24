---
title: RefBy_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: ebfc84b2e7eb88078b3b8010f0a7001e90a9cb31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348324"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="27f89-102">RefBy_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="27f89-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="27f89-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="27f89-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27f89-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="27f89-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="27f89-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="27f89-105">**Schema file**</span></span> <br/> |<span data-ttu-id="27f89-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="27f89-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="27f89-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="27f89-107">**Extension base**</span></span> <br/> |<span data-ttu-id="27f89-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="27f89-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27f89-109">Definición</span><span class="sxs-lookup"><span data-stu-id="27f89-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="27f89-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="27f89-110">Elements and attributes</span></span>

<span data-ttu-id="27f89-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="27f89-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="27f89-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="27f89-112">Child elements</span></span>

<span data-ttu-id="27f89-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="27f89-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27f89-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="27f89-114">Attributes</span></span>

|<span data-ttu-id="27f89-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="27f89-115">**Attribute**</span></span>|<span data-ttu-id="27f89-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="27f89-116">**Type**</span></span>|<span data-ttu-id="27f89-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="27f89-117">**Required**</span></span>|<span data-ttu-id="27f89-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="27f89-118">**Description**</span></span>|<span data-ttu-id="27f89-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="27f89-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27f89-120">ID</span><span class="sxs-lookup"><span data-stu-id="27f89-120">ID</span></span>  <br/> |<span data-ttu-id="27f89-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="27f89-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="27f89-122">necesario</span><span class="sxs-lookup"><span data-stu-id="27f89-122">required</span></span>  <br/> ||<span data-ttu-id="27f89-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="27f89-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="27f89-124">T</span><span class="sxs-lookup"><span data-stu-id="27f89-124">T</span></span>  <br/> |<span data-ttu-id="27f89-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="27f89-125">xsd:string</span></span>  <br/> |<span data-ttu-id="27f89-126">necesario</span><span class="sxs-lookup"><span data-stu-id="27f89-126">required</span></span>  <br/> ||<span data-ttu-id="27f89-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="27f89-127">Values of the xsd:string type.</span></span>  <br/> |
   

