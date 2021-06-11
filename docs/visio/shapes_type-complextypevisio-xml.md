---
title: Shapes_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 798af3d68df6c430fffb318e5e19c83aea441ca0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542089"
---
# <a name="shapes_type-complextype-visio-xml"></a><span data-ttu-id="f1119-102">Shapes_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f1119-102">Shapes_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f1119-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f1119-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1119-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f1119-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f1119-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f1119-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f1119-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f1119-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f1119-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f1119-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f1119-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f1119-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1119-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f1119-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f1119-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f1119-110">Elements and attributes</span></span>

<span data-ttu-id="f1119-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f1119-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f1119-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1119-112">Child elements</span></span>

|<span data-ttu-id="f1119-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f1119-113">**Element**</span></span>|<span data-ttu-id="f1119-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f1119-114">**Type**</span></span>|<span data-ttu-id="f1119-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1119-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1119-116">Shape</span><span class="sxs-lookup"><span data-stu-id="f1119-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1119-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f1119-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f1119-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1119-118">Attributes</span></span>

<span data-ttu-id="f1119-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1119-119">None.</span></span>
  

