---
title: RelCubBezTo_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 004dc563-d089-230f-0055-038b72eebbed
ms.openlocfilehash: 5dec2bde6b2ac704d9107bf195282bb3f53e61e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822959"
---
# <a name="relcubbeztotype-complextype-visio-xml"></a><span data-ttu-id="a6ec6-102">RelCubBezTo_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a6ec6-102">RelCubBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a6ec6-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a6ec6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6ec6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a6ec6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a6ec6-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a6ec6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a6ec6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a6ec6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a6ec6-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="a6ec6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a6ec6-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="a6ec6-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a6ec6-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a6ec6-109">Definition</span></span>

```XML
          <xs:complexType name="RelCubBezTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="a6ec6-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a6ec6-110">Elements and attributes</span></span>

<span data-ttu-id="a6ec6-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a6ec6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a6ec6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6ec6-112">Child elements</span></span>

|<span data-ttu-id="a6ec6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6ec6-113">**Element**</span></span>|<span data-ttu-id="a6ec6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a6ec6-114">**Type**</span></span>|<span data-ttu-id="a6ec6-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6ec6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a6ec6-116">Cell</span><span class="sxs-lookup"><span data-stu-id="a6ec6-116">Cell</span></span>](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="a6ec6-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a6ec6-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a6ec6-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6ec6-118">Attributes</span></span>

<span data-ttu-id="a6ec6-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6ec6-119">None.</span></span>
  

