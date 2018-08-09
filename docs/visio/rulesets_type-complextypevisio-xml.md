---
title: RuleSets_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 795864810c5d79f6328339009ddc84410caa4e62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823082"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="b8224-102">RuleSets_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b8224-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b8224-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b8224-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8224-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b8224-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b8224-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b8224-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b8224-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b8224-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b8224-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b8224-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b8224-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b8224-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8224-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b8224-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSets_Type">
          
          <xs:sequence>
    <xs:element name="RuleSet"  type="RuleSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b8224-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b8224-110">Elements and attributes</span></span>

<span data-ttu-id="b8224-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b8224-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b8224-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8224-112">Child elements</span></span>

|<span data-ttu-id="b8224-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8224-113">**Element**</span></span>|<span data-ttu-id="b8224-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b8224-114">**Type**</span></span>|<span data-ttu-id="b8224-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8224-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8224-116">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="b8224-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8224-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="b8224-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b8224-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8224-118">Attributes</span></span>

<span data-ttu-id="b8224-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8224-119">None.</span></span>
  

