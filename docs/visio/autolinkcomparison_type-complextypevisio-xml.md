---
title: AutoLinkComparison_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389753"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="24010-102">AutoLinkComparison_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="24010-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="24010-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="24010-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24010-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="24010-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="24010-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="24010-105">**Schema file**</span></span> <br/> |<span data-ttu-id="24010-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="24010-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="24010-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="24010-107">**Extension base**</span></span> <br/> |<span data-ttu-id="24010-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="24010-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="24010-109">Definición</span><span class="sxs-lookup"><span data-stu-id="24010-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="24010-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="24010-110">Elements and attributes</span></span>

<span data-ttu-id="24010-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="24010-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="24010-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="24010-112">Child elements</span></span>

<span data-ttu-id="24010-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24010-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24010-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="24010-114">Attributes</span></span>

|<span data-ttu-id="24010-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="24010-115">**Attribute**</span></span>|<span data-ttu-id="24010-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="24010-116">**Type**</span></span>|<span data-ttu-id="24010-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="24010-117">**Required**</span></span>|<span data-ttu-id="24010-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="24010-118">**Description**</span></span>|<span data-ttu-id="24010-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="24010-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="24010-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="24010-120">ColumnName</span></span>  <br/> |<span data-ttu-id="24010-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="24010-121">xsd:string</span></span>  <br/> |<span data-ttu-id="24010-122">necesario</span><span class="sxs-lookup"><span data-stu-id="24010-122">required</span></span>  <br/> ||<span data-ttu-id="24010-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="24010-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="24010-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="24010-124">ContextType</span></span>  <br/> |<span data-ttu-id="24010-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="24010-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="24010-126">necesario</span><span class="sxs-lookup"><span data-stu-id="24010-126">required</span></span>  <br/> ||<span data-ttu-id="24010-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="24010-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="24010-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="24010-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="24010-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="24010-129">xsd:string</span></span>  <br/> |<span data-ttu-id="24010-130">opcional</span><span class="sxs-lookup"><span data-stu-id="24010-130">optional</span></span>  <br/> ||<span data-ttu-id="24010-131">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="24010-131">Values of the xsd:string type.</span></span>  <br/> |
   

