---
title: AutoLinkComparison_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338601"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="2e1e0-102">AutoLinkComparison_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2e1e0-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2e1e0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2e1e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e1e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2e1e0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2e1e0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2e1e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2e1e0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2e1e0-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2e1e0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2e1e0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2e1e0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2e1e0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2e1e0-110">Elements and attributes</span></span>

<span data-ttu-id="2e1e0-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2e1e0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e1e0-112">Child elements</span></span>

<span data-ttu-id="2e1e0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e1e0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e1e0-114">Attributes</span></span>

|<span data-ttu-id="2e1e0-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-115">**Attribute**</span></span>|<span data-ttu-id="2e1e0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-116">**Type**</span></span>|<span data-ttu-id="2e1e0-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-117">**Required**</span></span>|<span data-ttu-id="2e1e0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-118">**Description**</span></span>|<span data-ttu-id="2e1e0-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2e1e0-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="2e1e0-120">ColumnName</span></span>  <br/> |<span data-ttu-id="2e1e0-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2e1e0-121">xsd:string</span></span>  <br/> |<span data-ttu-id="2e1e0-122">necesario</span><span class="sxs-lookup"><span data-stu-id="2e1e0-122">required</span></span>  <br/> ||<span data-ttu-id="2e1e0-123">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e1e0-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="2e1e0-124">ContextType</span></span>  <br/> |<span data-ttu-id="2e1e0-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2e1e0-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2e1e0-126">necesario</span><span class="sxs-lookup"><span data-stu-id="2e1e0-126">required</span></span>  <br/> ||<span data-ttu-id="2e1e0-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2e1e0-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="2e1e0-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="2e1e0-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2e1e0-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2e1e0-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2e1e0-130">optional</span></span>  <br/> ||<span data-ttu-id="2e1e0-131">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-131">Values of the xsd:string type.</span></span>  <br/> |
   

