---
title: Trigger_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 53a9efabe698e6b9c98c0471b97551c8ea2406da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541900"
---
# <a name="trigger_type-complextype-visio-xml"></a><span data-ttu-id="53847-102">Trigger_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="53847-102">Trigger_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="53847-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="53847-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53847-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="53847-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="53847-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="53847-105">**Schema file**</span></span> <br/> |<span data-ttu-id="53847-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="53847-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="53847-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="53847-107">**Extension base**</span></span> <br/> |<span data-ttu-id="53847-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="53847-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="53847-109">Definición</span><span class="sxs-lookup"><span data-stu-id="53847-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="53847-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="53847-110">Elements and attributes</span></span>

<span data-ttu-id="53847-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="53847-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="53847-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53847-112">Child elements</span></span>

|<span data-ttu-id="53847-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53847-113">**Element**</span></span>|<span data-ttu-id="53847-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="53847-114">**Type**</span></span>|<span data-ttu-id="53847-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53847-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="53847-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="53847-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="53847-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="53847-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="53847-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="53847-118">Attributes</span></span>

|<span data-ttu-id="53847-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="53847-119">**Attribute**</span></span>|<span data-ttu-id="53847-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="53847-120">**Type**</span></span>|<span data-ttu-id="53847-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="53847-121">**Required**</span></span>|<span data-ttu-id="53847-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53847-122">**Description**</span></span>|<span data-ttu-id="53847-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="53847-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="53847-124">N</span><span class="sxs-lookup"><span data-stu-id="53847-124">N</span></span>  <br/> |<span data-ttu-id="53847-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="53847-125">xsd:string</span></span>  <br/> |<span data-ttu-id="53847-126">necesario</span><span class="sxs-lookup"><span data-stu-id="53847-126">required</span></span>  <br/> ||<span data-ttu-id="53847-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="53847-127">Values of the xsd:string type.</span></span>  <br/> |
   

