---
title: RuleInfo_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382571"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="549ed-102">RuleInfo_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="549ed-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="549ed-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="549ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="549ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="549ed-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="549ed-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="549ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="549ed-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="549ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="549ed-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="549ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="549ed-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="549ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="549ed-109">Definición</span><span class="sxs-lookup"><span data-stu-id="549ed-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="549ed-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="549ed-110">Elements and attributes</span></span>

<span data-ttu-id="549ed-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="549ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="549ed-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="549ed-112">Child elements</span></span>

<span data-ttu-id="549ed-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="549ed-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="549ed-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="549ed-114">Attributes</span></span>

|<span data-ttu-id="549ed-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="549ed-115">**Attribute**</span></span>|<span data-ttu-id="549ed-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="549ed-116">**Type**</span></span>|<span data-ttu-id="549ed-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="549ed-117">**Required**</span></span>|<span data-ttu-id="549ed-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="549ed-118">**Description**</span></span>|<span data-ttu-id="549ed-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="549ed-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="549ed-120">Identificador de regla</span><span class="sxs-lookup"><span data-stu-id="549ed-120">RuleID</span></span>  <br/> |<span data-ttu-id="549ed-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="549ed-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="549ed-122">necesario</span><span class="sxs-lookup"><span data-stu-id="549ed-122">required</span></span>  <br/> ||<span data-ttu-id="549ed-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="549ed-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="549ed-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="549ed-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="549ed-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="549ed-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="549ed-126">necesario</span><span class="sxs-lookup"><span data-stu-id="549ed-126">required</span></span>  <br/> ||<span data-ttu-id="549ed-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="549ed-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

