---
title: LayerRow_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c8015f59-06a7-54c5-2df6-bc9e4d19f17b
ms.openlocfilehash: 2382c7fbe244d031d3aa2004b9887e6495b0f7a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822449"
---
# <a name="layerrowtype-complextype-visio-xml"></a><span data-ttu-id="be049-102">LayerRow_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="be049-102">LayerRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="be049-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="be049-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be049-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="be049-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="be049-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="be049-105">**Schema file**</span></span> <br/> |<span data-ttu-id="be049-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="be049-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="be049-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="be049-107">**Extension base**</span></span> <br/> |<span data-ttu-id="be049-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="be049-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be049-109">Definición</span><span class="sxs-lookup"><span data-stu-id="be049-109">Definition</span></span>

```XML
          <xs:complexType name="LayerRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be049-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="be049-110">Elements and attributes</span></span>

<span data-ttu-id="be049-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="be049-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="be049-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="be049-112">Child elements</span></span>

|<span data-ttu-id="be049-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="be049-113">**Element**</span></span>|<span data-ttu-id="be049-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="be049-114">**Type**</span></span>|<span data-ttu-id="be049-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be049-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be049-116">Cell</span><span class="sxs-lookup"><span data-stu-id="be049-116">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="be049-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="be049-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="be049-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="be049-118">Attributes</span></span>

<span data-ttu-id="be049-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="be049-119">None.</span></span>
  

