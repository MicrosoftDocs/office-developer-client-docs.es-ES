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
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="0052e-102">Windows_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0052e-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0052e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0052e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0052e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0052e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0052e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0052e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0052e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0052e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0052e-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="0052e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0052e-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0052e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0052e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0052e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0052e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0052e-110">Elements and attributes</span></span>

<span data-ttu-id="0052e-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0052e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0052e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0052e-112">Child elements</span></span>

|<span data-ttu-id="0052e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0052e-113">**Element**</span></span>|<span data-ttu-id="0052e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0052e-114">**Type**</span></span>|<span data-ttu-id="0052e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0052e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0052e-116">Window</span><span class="sxs-lookup"><span data-stu-id="0052e-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0052e-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="0052e-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0052e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0052e-118">Attributes</span></span>

|<span data-ttu-id="0052e-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0052e-119">**Attribute**</span></span>|<span data-ttu-id="0052e-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0052e-120">**Type**</span></span>|<span data-ttu-id="0052e-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0052e-121">**Required**</span></span>|<span data-ttu-id="0052e-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0052e-122">**Description**</span></span>|<span data-ttu-id="0052e-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0052e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0052e-124">Propiedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="0052e-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="0052e-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0052e-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0052e-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0052e-126">optional</span></span>  <br/> ||<span data-ttu-id="0052e-127">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0052e-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0052e-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="0052e-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="0052e-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0052e-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0052e-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0052e-130">optional</span></span>  <br/> ||<span data-ttu-id="0052e-131">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0052e-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

