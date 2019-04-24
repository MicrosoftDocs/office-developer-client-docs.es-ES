---
title: Trigger_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280861"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="a296e-102">Trigger_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a296e-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a296e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a296e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a296e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a296e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a296e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a296e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a296e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a296e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a296e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a296e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a296e-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a296e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a296e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a296e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a296e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a296e-110">Elements and attributes</span></span>

<span data-ttu-id="a296e-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a296e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a296e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a296e-112">Child elements</span></span>

|<span data-ttu-id="a296e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a296e-113">**Element**</span></span>|<span data-ttu-id="a296e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a296e-114">**Type**</span></span>|<span data-ttu-id="a296e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a296e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a296e-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="a296e-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a296e-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a296e-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a296e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="a296e-118">Attributes</span></span>

|<span data-ttu-id="a296e-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a296e-119">**Attribute**</span></span>|<span data-ttu-id="a296e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a296e-120">**Type**</span></span>|<span data-ttu-id="a296e-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a296e-121">**Required**</span></span>|<span data-ttu-id="a296e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a296e-122">**Description**</span></span>|<span data-ttu-id="a296e-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a296e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a296e-124">N</span><span class="sxs-lookup"><span data-stu-id="a296e-124">N</span></span>  <br/> |<span data-ttu-id="a296e-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a296e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="a296e-126">necesario</span><span class="sxs-lookup"><span data-stu-id="a296e-126">required</span></span>  <br/> ||<span data-ttu-id="a296e-127">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a296e-127">Values of the xsd:string type.</span></span>  <br/> |
   

