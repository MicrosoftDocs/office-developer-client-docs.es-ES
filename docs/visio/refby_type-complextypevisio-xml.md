---
title: RefBy_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 5042a618420a72284e0ef75c5d624c6f5464e162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822905"
---
# <a name="refbytype-complextype-visio-xml"></a><span data-ttu-id="c3e47-102">RefBy_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="c3e47-102">RefBy_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c3e47-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c3e47-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3e47-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3e47-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c3e47-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c3e47-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c3e47-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c3e47-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c3e47-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="c3e47-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c3e47-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c3e47-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3e47-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c3e47-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c3e47-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c3e47-110">Elements and attributes</span></span>

<span data-ttu-id="c3e47-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="c3e47-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c3e47-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3e47-112">Child elements</span></span>

<span data-ttu-id="c3e47-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3e47-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3e47-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3e47-114">Attributes</span></span>

|<span data-ttu-id="c3e47-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="c3e47-115">**Attribute**</span></span>|<span data-ttu-id="c3e47-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e47-116">**Type**</span></span>|<span data-ttu-id="c3e47-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c3e47-117">**Required**</span></span>|<span data-ttu-id="c3e47-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3e47-118">**Description**</span></span>|<span data-ttu-id="c3e47-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="c3e47-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3e47-120">id.</span><span class="sxs-lookup"><span data-stu-id="c3e47-120">ID</span></span>  <br/> |<span data-ttu-id="c3e47-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3e47-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3e47-122">necesario</span><span class="sxs-lookup"><span data-stu-id="c3e47-122">required</span></span>  <br/> ||<span data-ttu-id="c3e47-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c3e47-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3e47-124">T</span><span class="sxs-lookup"><span data-stu-id="c3e47-124">T</span></span>  <br/> |<span data-ttu-id="c3e47-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c3e47-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c3e47-126">necesario</span><span class="sxs-lookup"><span data-stu-id="c3e47-126">required</span></span>  <br/> ||<span data-ttu-id="c3e47-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="c3e47-127">Values of the xsd:string type.</span></span>  <br/> |
   

