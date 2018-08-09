---
title: Shapes_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 707f20823d0413e0b064b2a367da803419889ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823177"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="47898-102">Shapes_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="47898-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="47898-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="47898-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47898-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="47898-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47898-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="47898-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47898-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47898-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47898-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="47898-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47898-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="47898-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47898-109">Definición</span><span class="sxs-lookup"><span data-stu-id="47898-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="47898-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="47898-110">Elements and attributes</span></span>

<span data-ttu-id="47898-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="47898-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47898-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="47898-112">Child elements</span></span>

|<span data-ttu-id="47898-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="47898-113">**Element**</span></span>|<span data-ttu-id="47898-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="47898-114">**Type**</span></span>|<span data-ttu-id="47898-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="47898-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47898-116">Shape</span><span class="sxs-lookup"><span data-stu-id="47898-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="47898-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="47898-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="47898-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="47898-118">Attributes</span></span>

<span data-ttu-id="47898-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47898-119">None.</span></span>
  

