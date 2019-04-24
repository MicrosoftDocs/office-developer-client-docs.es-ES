---
title: Validation_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 6f751db1566e39d919fd0a456d3aab72559ceeba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332798"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="19cf8-102">Validation_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="19cf8-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="19cf8-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="19cf8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19cf8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19cf8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19cf8-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="19cf8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19cf8-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="19cf8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19cf8-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="19cf8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19cf8-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="19cf8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19cf8-109">Definición</span><span class="sxs-lookup"><span data-stu-id="19cf8-109">Definition</span></span>

```XML
          <xs:complexType name="Validation_Type">
          
          <xs:sequence>
    <xs:element name="ValidationProperties"  type="ValidationProperties_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleSets"  type="RuleSets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Issues"  type="Issues_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="19cf8-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="19cf8-110">Elements and attributes</span></span>

<span data-ttu-id="19cf8-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="19cf8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19cf8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19cf8-112">Child elements</span></span>

|<span data-ttu-id="19cf8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="19cf8-113">**Element**</span></span>|<span data-ttu-id="19cf8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="19cf8-114">**Type**</span></span>|<span data-ttu-id="19cf8-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19cf8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19cf8-116">Issues</span><span class="sxs-lookup"><span data-stu-id="19cf8-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19cf8-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="19cf8-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19cf8-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="19cf8-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19cf8-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="19cf8-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19cf8-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="19cf8-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19cf8-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="19cf8-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="19cf8-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="19cf8-122">Attributes</span></span>

<span data-ttu-id="19cf8-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19cf8-123">None.</span></span>
  

