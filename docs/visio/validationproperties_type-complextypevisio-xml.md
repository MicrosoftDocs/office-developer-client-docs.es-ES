---
title: ValidationProperties_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389984"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="e33b0-102">ValidationProperties_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e33b0-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e33b0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e33b0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e33b0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e33b0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e33b0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e33b0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e33b0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e33b0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e33b0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e33b0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e33b0-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e33b0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e33b0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e33b0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e33b0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e33b0-110">Elements and attributes</span></span>

<span data-ttu-id="e33b0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e33b0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e33b0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e33b0-112">Child elements</span></span>

<span data-ttu-id="e33b0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e33b0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e33b0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="e33b0-114">Attributes</span></span>

|<span data-ttu-id="e33b0-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e33b0-115">**Attribute**</span></span>|<span data-ttu-id="e33b0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e33b0-116">**Type**</span></span>|<span data-ttu-id="e33b0-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e33b0-117">**Required**</span></span>|<span data-ttu-id="e33b0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e33b0-118">**Description**</span></span>|<span data-ttu-id="e33b0-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="e33b0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e33b0-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="e33b0-120">LastValidated</span></span>  <br/> |<span data-ttu-id="e33b0-121">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="e33b0-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="e33b0-122">necesario</span><span class="sxs-lookup"><span data-stu-id="e33b0-122">required</span></span>  <br/> ||<span data-ttu-id="e33b0-123">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="e33b0-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="e33b0-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="e33b0-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="e33b0-125">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="e33b0-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e33b0-126">necesario</span><span class="sxs-lookup"><span data-stu-id="e33b0-126">required</span></span>  <br/> ||<span data-ttu-id="e33b0-127">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="e33b0-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

