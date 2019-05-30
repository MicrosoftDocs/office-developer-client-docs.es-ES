---
title: ComplexType ValidationProperties_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: d83a1ce8e7ad89155726200de2950da755e5d3db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538518"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="a7285-102">ComplexType ValidationProperties_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="a7285-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a7285-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a7285-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7285-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a7285-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a7285-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a7285-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a7285-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a7285-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a7285-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a7285-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a7285-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a7285-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7285-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a7285-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a7285-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a7285-110">Elements and attributes</span></span>

<span data-ttu-id="a7285-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a7285-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a7285-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a7285-112">Child elements</span></span>

<span data-ttu-id="a7285-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a7285-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7285-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7285-114">Attributes</span></span>

|<span data-ttu-id="a7285-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a7285-115">**Attribute**</span></span>|<span data-ttu-id="a7285-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a7285-116">**Type**</span></span>|<span data-ttu-id="a7285-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a7285-117">**Required**</span></span>|<span data-ttu-id="a7285-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7285-118">**Description**</span></span>|<span data-ttu-id="a7285-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a7285-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a7285-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="a7285-120">LastValidated</span></span>  <br/> |<span data-ttu-id="a7285-121">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="a7285-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="a7285-122">necesario</span><span class="sxs-lookup"><span data-stu-id="a7285-122">required</span></span>  <br/> ||<span data-ttu-id="a7285-123">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="a7285-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="a7285-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="a7285-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="a7285-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a7285-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a7285-126">necesario</span><span class="sxs-lookup"><span data-stu-id="a7285-126">required</span></span>  <br/> ||<span data-ttu-id="a7285-127">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a7285-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

