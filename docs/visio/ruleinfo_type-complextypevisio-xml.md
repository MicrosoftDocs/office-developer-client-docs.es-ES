---
title: RuleInfo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360469"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="17aed-102">RuleInfo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="17aed-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="17aed-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="17aed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17aed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17aed-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="17aed-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="17aed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="17aed-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="17aed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="17aed-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="17aed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="17aed-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="17aed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17aed-109">Definición</span><span class="sxs-lookup"><span data-stu-id="17aed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="17aed-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="17aed-110">Elements and attributes</span></span>

<span data-ttu-id="17aed-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="17aed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="17aed-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="17aed-112">Child elements</span></span>

<span data-ttu-id="17aed-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="17aed-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17aed-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="17aed-114">Attributes</span></span>

|<span data-ttu-id="17aed-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="17aed-115">**Attribute**</span></span>|<span data-ttu-id="17aed-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17aed-116">**Type**</span></span>|<span data-ttu-id="17aed-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="17aed-117">**Required**</span></span>|<span data-ttu-id="17aed-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17aed-118">**Description**</span></span>|<span data-ttu-id="17aed-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="17aed-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="17aed-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="17aed-120">RuleID</span></span>  <br/> |<span data-ttu-id="17aed-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17aed-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17aed-122">necesario</span><span class="sxs-lookup"><span data-stu-id="17aed-122">required</span></span>  <br/> ||<span data-ttu-id="17aed-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17aed-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17aed-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="17aed-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="17aed-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17aed-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17aed-126">necesario</span><span class="sxs-lookup"><span data-stu-id="17aed-126">required</span></span>  <br/> ||<span data-ttu-id="17aed-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="17aed-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

