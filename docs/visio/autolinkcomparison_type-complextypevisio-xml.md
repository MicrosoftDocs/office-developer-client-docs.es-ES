---
title: AutoLinkComparison_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: bb1b07a59fbe3fc706bc67db58e67c5b0ec14033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821542"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="f4f63-102">AutoLinkComparison_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f4f63-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f4f63-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f4f63-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4f63-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f4f63-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f4f63-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f4f63-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f4f63-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f4f63-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f4f63-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f4f63-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f4f63-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f4f63-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4f63-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f4f63-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4f63-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f4f63-110">Elements and attributes</span></span>

<span data-ttu-id="f4f63-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f4f63-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f4f63-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4f63-112">Child elements</span></span>

<span data-ttu-id="f4f63-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4f63-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4f63-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4f63-114">Attributes</span></span>

|<span data-ttu-id="f4f63-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f4f63-115">**Attribute**</span></span>|<span data-ttu-id="f4f63-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4f63-116">**Type**</span></span>|<span data-ttu-id="f4f63-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f4f63-117">**Required**</span></span>|<span data-ttu-id="f4f63-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4f63-118">**Description**</span></span>|<span data-ttu-id="f4f63-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="f4f63-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f4f63-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="f4f63-120">ColumnName</span></span>  <br/> |<span data-ttu-id="f4f63-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f4f63-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f4f63-122">necesario</span><span class="sxs-lookup"><span data-stu-id="f4f63-122">required</span></span>  <br/> ||<span data-ttu-id="f4f63-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f4f63-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f4f63-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="f4f63-124">ContextType</span></span>  <br/> |<span data-ttu-id="f4f63-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f4f63-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f4f63-126">necesario</span><span class="sxs-lookup"><span data-stu-id="f4f63-126">required</span></span>  <br/> ||<span data-ttu-id="f4f63-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f4f63-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f4f63-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="f4f63-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="f4f63-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f4f63-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f4f63-130">opcional</span><span class="sxs-lookup"><span data-stu-id="f4f63-130">optional</span></span>  <br/> ||<span data-ttu-id="f4f63-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f4f63-131">Values of the xsd:string type.</span></span>  <br/> |
   

