---
title: ValidationProperties_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355982"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="07c1e-102">ValidationProperties_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="07c1e-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="07c1e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="07c1e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07c1e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="07c1e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="07c1e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="07c1e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="07c1e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="07c1e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="07c1e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="07c1e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="07c1e-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="07c1e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="07c1e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="07c1e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="07c1e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="07c1e-110">Elements and attributes</span></span>

<span data-ttu-id="07c1e-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="07c1e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="07c1e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07c1e-112">Child elements</span></span>

<span data-ttu-id="07c1e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="07c1e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07c1e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="07c1e-114">Attributes</span></span>

|<span data-ttu-id="07c1e-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="07c1e-115">**Attribute**</span></span>|<span data-ttu-id="07c1e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="07c1e-116">**Type**</span></span>|<span data-ttu-id="07c1e-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="07c1e-117">**Required**</span></span>|<span data-ttu-id="07c1e-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07c1e-118">**Description**</span></span>|<span data-ttu-id="07c1e-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="07c1e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="07c1e-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="07c1e-120">LastValidated</span></span>  <br/> |<span data-ttu-id="07c1e-121">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="07c1e-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="07c1e-122">necesario</span><span class="sxs-lookup"><span data-stu-id="07c1e-122">required</span></span>  <br/> ||<span data-ttu-id="07c1e-123">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="07c1e-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="07c1e-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="07c1e-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="07c1e-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="07c1e-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="07c1e-126">necesario</span><span class="sxs-lookup"><span data-stu-id="07c1e-126">required</span></span>  <br/> ||<span data-ttu-id="07c1e-127">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="07c1e-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

