---
title: RuleInfo_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0a0ac32729b83a5d648b2826bffe5a9df4d9fc0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823070"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="f332e-102">RuleInfo_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f332e-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f332e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f332e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f332e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f332e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f332e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f332e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f332e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f332e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f332e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f332e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f332e-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f332e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f332e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f332e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f332e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f332e-110">Elements and attributes</span></span>

<span data-ttu-id="f332e-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f332e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f332e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f332e-112">Child elements</span></span>

<span data-ttu-id="f332e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f332e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f332e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f332e-114">Attributes</span></span>

|<span data-ttu-id="f332e-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f332e-115">**Attribute**</span></span>|<span data-ttu-id="f332e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f332e-116">**Type**</span></span>|<span data-ttu-id="f332e-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f332e-117">**Required**</span></span>|<span data-ttu-id="f332e-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f332e-118">**Description**</span></span>|<span data-ttu-id="f332e-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="f332e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f332e-120">Identificador de regla</span><span class="sxs-lookup"><span data-stu-id="f332e-120">RuleID</span></span>  <br/> |<span data-ttu-id="f332e-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f332e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f332e-122">necesario</span><span class="sxs-lookup"><span data-stu-id="f332e-122">required</span></span>  <br/> ||<span data-ttu-id="f332e-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f332e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f332e-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="f332e-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="f332e-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f332e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f332e-126">necesario</span><span class="sxs-lookup"><span data-stu-id="f332e-126">required</span></span>  <br/> ||<span data-ttu-id="f332e-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f332e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

