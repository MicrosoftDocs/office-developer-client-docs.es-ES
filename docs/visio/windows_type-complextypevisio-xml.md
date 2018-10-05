---
title: Windows_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386561"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="2968d-102">Windows_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="2968d-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2968d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2968d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2968d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2968d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2968d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2968d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2968d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2968d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2968d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2968d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2968d-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2968d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2968d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2968d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2968d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2968d-110">Elements and attributes</span></span>

<span data-ttu-id="2968d-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="2968d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2968d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2968d-112">Child elements</span></span>

|<span data-ttu-id="2968d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2968d-113">**Element**</span></span>|<span data-ttu-id="2968d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2968d-114">**Type**</span></span>|<span data-ttu-id="2968d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2968d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2968d-116">Window</span><span class="sxs-lookup"><span data-stu-id="2968d-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2968d-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="2968d-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2968d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2968d-118">Attributes</span></span>

|<span data-ttu-id="2968d-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2968d-119">**Attribute**</span></span>|<span data-ttu-id="2968d-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2968d-120">**Type**</span></span>|<span data-ttu-id="2968d-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2968d-121">**Required**</span></span>|<span data-ttu-id="2968d-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2968d-122">**Description**</span></span>|<span data-ttu-id="2968d-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="2968d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2968d-124">Propiedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="2968d-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="2968d-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2968d-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2968d-126">opcional</span><span class="sxs-lookup"><span data-stu-id="2968d-126">optional</span></span>  <br/> ||<span data-ttu-id="2968d-127">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2968d-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2968d-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="2968d-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="2968d-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="2968d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2968d-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2968d-130">optional</span></span>  <br/> ||<span data-ttu-id="2968d-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="2968d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

