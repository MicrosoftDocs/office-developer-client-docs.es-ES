---
title: Trigger_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 38ba2800a32f4f1b4809a5e542fd6b79794bf369
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823439"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="5d537-102">Trigger_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5d537-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5d537-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5d537-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d537-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5d537-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5d537-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5d537-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5d537-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5d537-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5d537-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="5d537-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5d537-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5d537-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d537-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5d537-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5d537-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5d537-110">Elements and attributes</span></span>

<span data-ttu-id="5d537-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5d537-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5d537-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d537-112">Child elements</span></span>

|<span data-ttu-id="5d537-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5d537-113">**Element**</span></span>|<span data-ttu-id="5d537-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d537-114">**Type**</span></span>|<span data-ttu-id="5d537-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d537-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d537-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="5d537-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d537-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="5d537-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5d537-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d537-118">Attributes</span></span>

|<span data-ttu-id="5d537-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5d537-119">**Attribute**</span></span>|<span data-ttu-id="5d537-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d537-120">**Type**</span></span>|<span data-ttu-id="5d537-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5d537-121">**Required**</span></span>|<span data-ttu-id="5d537-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d537-122">**Description**</span></span>|<span data-ttu-id="5d537-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="5d537-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5d537-124">N</span><span class="sxs-lookup"><span data-stu-id="5d537-124">N</span></span>  <br/> |<span data-ttu-id="5d537-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5d537-125">xsd:string</span></span>  <br/> |<span data-ttu-id="5d537-126">necesario</span><span class="sxs-lookup"><span data-stu-id="5d537-126">required</span></span>  <br/> ||<span data-ttu-id="5d537-127">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="5d537-127">Values of the xsd:string type.</span></span>  <br/> |
   

