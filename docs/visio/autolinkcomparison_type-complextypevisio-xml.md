---
title: AutoLinkComparison_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: eeb58a0e2f401c0e8a2bcf67147bc300bb8535ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537888"
---
# <a name="autolinkcomparison_type-complextype-visio-xml"></a><span data-ttu-id="7fb8b-102">AutoLinkComparison_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7fb8b-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7fb8b-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="7fb8b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fb8b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7fb8b-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7fb8b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7fb8b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7fb8b-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7fb8b-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7fb8b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7fb8b-109">Definición</span><span class="sxs-lookup"><span data-stu-id="7fb8b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7fb8b-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7fb8b-110">Elements and attributes</span></span>

<span data-ttu-id="7fb8b-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7fb8b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7fb8b-112">Child elements</span></span>

<span data-ttu-id="7fb8b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fb8b-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="7fb8b-114">Attributes</span></span>

|<span data-ttu-id="7fb8b-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-115">**Attribute**</span></span>|<span data-ttu-id="7fb8b-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-116">**Type**</span></span>|<span data-ttu-id="7fb8b-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-117">**Required**</span></span>|<span data-ttu-id="7fb8b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-118">**Description**</span></span>|<span data-ttu-id="7fb8b-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7fb8b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7fb8b-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="7fb8b-120">ColumnName</span></span>  <br/> |<span data-ttu-id="7fb8b-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7fb8b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="7fb8b-122">necesario</span><span class="sxs-lookup"><span data-stu-id="7fb8b-122">required</span></span>  <br/> ||<span data-ttu-id="7fb8b-123">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7fb8b-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="7fb8b-124">ContextType</span></span>  <br/> |<span data-ttu-id="7fb8b-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7fb8b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7fb8b-126">necesario</span><span class="sxs-lookup"><span data-stu-id="7fb8b-126">required</span></span>  <br/> ||<span data-ttu-id="7fb8b-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7fb8b-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="7fb8b-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="7fb8b-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7fb8b-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7fb8b-130">opcional</span><span class="sxs-lookup"><span data-stu-id="7fb8b-130">optional</span></span>  <br/> ||<span data-ttu-id="7fb8b-131">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7fb8b-131">Values of the xsd:string type.</span></span>  <br/> |
   

