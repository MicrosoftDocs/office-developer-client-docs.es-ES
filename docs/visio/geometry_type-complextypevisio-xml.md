---
title: Geometry_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 882540e92f9635d6e99716fd8bbbe369c42a6bec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822230"
---
# <a name="geometrytype-complextype-visio-xml"></a><span data-ttu-id="da708-102">Geometry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="da708-102">Geometry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="da708-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="da708-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da708-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="da708-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="da708-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="da708-105">**Schema file**</span></span> <br/> |<span data-ttu-id="da708-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="da708-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="da708-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="da708-107">**Extension base**</span></span> <br/> |<span data-ttu-id="da708-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="da708-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="da708-109">Definición</span><span class="sxs-lookup"><span data-stu-id="da708-109">Definition</span></span>

```XML
          <xs:complexType name="Geometry_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="GeometryRow_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="da708-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="da708-110">Elements and attributes</span></span>

<span data-ttu-id="da708-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="da708-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="da708-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da708-112">Child elements</span></span>

|<span data-ttu-id="da708-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="da708-113">**Element**</span></span>|<span data-ttu-id="da708-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="da708-114">**Type**</span></span>|<span data-ttu-id="da708-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da708-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="da708-116">Cell</span><span class="sxs-lookup"><span data-stu-id="da708-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="da708-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="da708-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="da708-118">Row</span><span class="sxs-lookup"><span data-stu-id="da708-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="da708-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="da708-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="da708-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="da708-120">Attributes</span></span>

<span data-ttu-id="da708-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="da708-121">None.</span></span>
  

