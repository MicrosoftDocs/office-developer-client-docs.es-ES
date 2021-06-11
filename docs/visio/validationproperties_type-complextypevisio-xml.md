---
title: ValidationProperties_Type complexType (Visio XML)
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
# <a name="validationproperties_type-complextype-visio-xml"></a><span data-ttu-id="5d7db-102">ValidationProperties_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5d7db-102">ValidationProperties_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5d7db-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5d7db-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d7db-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5d7db-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5d7db-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5d7db-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5d7db-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5d7db-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5d7db-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="5d7db-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5d7db-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5d7db-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d7db-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5d7db-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5d7db-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5d7db-110">Elements and attributes</span></span>

<span data-ttu-id="5d7db-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5d7db-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5d7db-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d7db-112">Child elements</span></span>

<span data-ttu-id="5d7db-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5d7db-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d7db-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d7db-114">Attributes</span></span>

|<span data-ttu-id="5d7db-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5d7db-115">**Attribute**</span></span>|<span data-ttu-id="5d7db-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d7db-116">**Type**</span></span>|<span data-ttu-id="5d7db-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5d7db-117">**Required**</span></span>|<span data-ttu-id="5d7db-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d7db-118">**Description**</span></span>|<span data-ttu-id="5d7db-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="5d7db-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5d7db-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="5d7db-120">LastValidated</span></span>  <br/> |<span data-ttu-id="5d7db-121">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="5d7db-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="5d7db-122">necesario</span><span class="sxs-lookup"><span data-stu-id="5d7db-122">required</span></span>  <br/> ||<span data-ttu-id="5d7db-123">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="5d7db-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="5d7db-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="5d7db-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="5d7db-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5d7db-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5d7db-126">necesario</span><span class="sxs-lookup"><span data-stu-id="5d7db-126">required</span></span>  <br/> ||<span data-ttu-id="5d7db-127">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="5d7db-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

