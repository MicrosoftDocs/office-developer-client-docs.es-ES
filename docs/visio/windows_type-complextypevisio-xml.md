---
title: Windows_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 33a2acaad76543115c480b5e9a32ddba8fb0d66a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823546"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="d27a9-102">Windows_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="d27a9-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d27a9-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d27a9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d27a9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d27a9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d27a9-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d27a9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d27a9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d27a9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d27a9-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d27a9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d27a9-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d27a9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d27a9-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d27a9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d27a9-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d27a9-110">Elements and attributes</span></span>

<span data-ttu-id="d27a9-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="d27a9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d27a9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d27a9-112">Child elements</span></span>

|<span data-ttu-id="d27a9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d27a9-113">**Element**</span></span>|<span data-ttu-id="d27a9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d27a9-114">**Type**</span></span>|<span data-ttu-id="d27a9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d27a9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d27a9-116">Window</span><span class="sxs-lookup"><span data-stu-id="d27a9-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d27a9-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="d27a9-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d27a9-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d27a9-118">Attributes</span></span>

|<span data-ttu-id="d27a9-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d27a9-119">**Attribute**</span></span>|<span data-ttu-id="d27a9-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d27a9-120">**Type**</span></span>|<span data-ttu-id="d27a9-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d27a9-121">**Required**</span></span>|<span data-ttu-id="d27a9-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d27a9-122">**Description**</span></span>|<span data-ttu-id="d27a9-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="d27a9-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d27a9-124">Propiedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="d27a9-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="d27a9-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d27a9-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d27a9-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d27a9-126">optional</span></span>  <br/> ||<span data-ttu-id="d27a9-127">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d27a9-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d27a9-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="d27a9-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="d27a9-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d27a9-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d27a9-130">opcional</span><span class="sxs-lookup"><span data-stu-id="d27a9-130">optional</span></span>  <br/> ||<span data-ttu-id="d27a9-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d27a9-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

