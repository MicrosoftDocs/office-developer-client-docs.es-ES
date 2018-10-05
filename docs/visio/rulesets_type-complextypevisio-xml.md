---
title: RuleSets_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 41172a4f15b0d9038fd0ffb0c0a7d8c3d4078798
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385924"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="87919-102">RuleSets_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="87919-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="87919-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="87919-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87919-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87919-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="87919-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="87919-105">**Schema file**</span></span> <br/> |<span data-ttu-id="87919-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="87919-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="87919-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="87919-107">**Extension base**</span></span> <br/> |<span data-ttu-id="87919-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="87919-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87919-109">Definición</span><span class="sxs-lookup"><span data-stu-id="87919-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="87919-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="87919-110">Elements and attributes</span></span>

<span data-ttu-id="87919-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="87919-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="87919-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87919-112">Child elements</span></span>

|<span data-ttu-id="87919-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="87919-113">**Element**</span></span>|<span data-ttu-id="87919-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87919-114">**Type**</span></span>|<span data-ttu-id="87919-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87919-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87919-116">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="87919-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87919-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="87919-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="87919-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="87919-118">Attributes</span></span>

<span data-ttu-id="87919-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87919-119">None.</span></span>
  

