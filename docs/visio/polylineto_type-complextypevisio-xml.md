---
title: PolylineTo_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: 71948dc1cab853c00fa993e26acef108def8aa1c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397355"
---
# <a name="polylinetotype-complextype-visio-xml"></a><span data-ttu-id="ad0b9-102">PolylineTo_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ad0b9-102">PolylineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ad0b9-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ad0b9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad0b9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad0b9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad0b9-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad0b9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad0b9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ad0b9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad0b9-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ad0b9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad0b9-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="ad0b9-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad0b9-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ad0b9-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="ad0b9-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ad0b9-110">Elements and attributes</span></span>

<span data-ttu-id="ad0b9-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad0b9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad0b9-112">Child elements</span></span>

|<span data-ttu-id="ad0b9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad0b9-113">**Element**</span></span>|<span data-ttu-id="ad0b9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad0b9-114">**Type**</span></span>|<span data-ttu-id="ad0b9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad0b9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad0b9-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ad0b9-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="ad0b9-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ad0b9-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad0b9-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad0b9-118">Attributes</span></span>

<span data-ttu-id="ad0b9-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-119">None.</span></span>
  

