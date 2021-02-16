---
title: Windows_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: b8d8ed39637bdd692b2ba113525f40a3f91ffc9c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538441"
---
# <a name="windows_type-complextype-visio-xml"></a><span data-ttu-id="5d243-102">Windows_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5d243-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="5d243-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5d243-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d243-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5d243-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5d243-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5d243-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5d243-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5d243-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5d243-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="5d243-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5d243-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5d243-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d243-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5d243-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5d243-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5d243-110">Elements and attributes</span></span>

<span data-ttu-id="5d243-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5d243-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5d243-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5d243-112">Child elements</span></span>

|<span data-ttu-id="5d243-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5d243-113">**Element**</span></span>|<span data-ttu-id="5d243-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d243-114">**Type**</span></span>|<span data-ttu-id="5d243-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d243-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d243-116">Window</span><span class="sxs-lookup"><span data-stu-id="5d243-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d243-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="5d243-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5d243-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="5d243-118">Attributes</span></span>

|<span data-ttu-id="5d243-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5d243-119">**Attribute**</span></span>|<span data-ttu-id="5d243-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5d243-120">**Type**</span></span>|<span data-ttu-id="5d243-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5d243-121">**Required**</span></span>|<span data-ttu-id="5d243-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d243-122">**Description**</span></span>|<span data-ttu-id="5d243-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="5d243-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5d243-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="5d243-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="5d243-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5d243-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5d243-126">opcional</span><span class="sxs-lookup"><span data-stu-id="5d243-126">optional</span></span>  <br/> ||<span data-ttu-id="5d243-127">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5d243-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5d243-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="5d243-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="5d243-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5d243-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5d243-130">opcional</span><span class="sxs-lookup"><span data-stu-id="5d243-130">optional</span></span>  <br/> ||<span data-ttu-id="5d243-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5d243-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

