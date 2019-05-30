---
title: ComplexType Validation_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 7c7b3c8b1a5fdb52ee835c87e18941b902b51734
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538532"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="6636d-102">ComplexType Validation_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="6636d-102">Validation_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6636d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6636d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6636d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6636d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6636d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6636d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6636d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6636d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6636d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6636d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6636d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6636d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6636d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6636d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6636d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6636d-110">Elements and attributes</span></span>

<span data-ttu-id="6636d-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6636d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6636d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6636d-112">Child elements</span></span>

|<span data-ttu-id="6636d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6636d-113">**Element**</span></span>|<span data-ttu-id="6636d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6636d-114">**Type**</span></span>|<span data-ttu-id="6636d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6636d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6636d-116">Issues</span><span class="sxs-lookup"><span data-stu-id="6636d-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6636d-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="6636d-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6636d-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="6636d-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6636d-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="6636d-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6636d-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="6636d-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6636d-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="6636d-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6636d-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="6636d-122">Attributes</span></span>

<span data-ttu-id="6636d-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6636d-123">None.</span></span>
  

