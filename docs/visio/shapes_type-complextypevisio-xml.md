---
title: Shapes_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 7d028939ad6c99ecf4160b95764c86779c399c8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344516"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="6fa4b-102">Shapes_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6fa4b-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6fa4b-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6fa4b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fa4b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6fa4b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6fa4b-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6fa4b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6fa4b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6fa4b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6fa4b-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6fa4b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6fa4b-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6fa4b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6fa4b-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6fa4b-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6fa4b-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6fa4b-110">Elements and attributes</span></span>

<span data-ttu-id="6fa4b-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6fa4b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6fa4b-112">Child elements</span></span>

|<span data-ttu-id="6fa4b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6fa4b-113">**Element**</span></span>|<span data-ttu-id="6fa4b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6fa4b-114">**Type**</span></span>|<span data-ttu-id="6fa4b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6fa4b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6fa4b-116">Shape</span><span class="sxs-lookup"><span data-stu-id="6fa4b-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fa4b-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6fa4b-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6fa4b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="6fa4b-118">Attributes</span></span>

<span data-ttu-id="6fa4b-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-119">None.</span></span>
  

