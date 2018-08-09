---
title: Ellipse_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67dc78e-6639-e32f-4909-945001659d30
ms.openlocfilehash: 84be003154bd8810dc3443a355feee0ec4cec19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822084"
---
# <a name="ellipsetype-complextype-visio-xml"></a><span data-ttu-id="25892-102">Ellipse_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="25892-102">Ellipse_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="25892-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="25892-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25892-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="25892-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="25892-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="25892-105">**Schema file**</span></span> <br/> |<span data-ttu-id="25892-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="25892-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="25892-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="25892-107">**Extension base**</span></span> <br/> |<span data-ttu-id="25892-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="25892-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="25892-109">Definición</span><span class="sxs-lookup"><span data-stu-id="25892-109">Definition</span></span>

```XML
          <xs:complexType name="Ellipse_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="25892-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="25892-110">Elements and attributes</span></span>

<span data-ttu-id="25892-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="25892-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="25892-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25892-112">Child elements</span></span>

|<span data-ttu-id="25892-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="25892-113">**Element**</span></span>|<span data-ttu-id="25892-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="25892-114">**Type**</span></span>|<span data-ttu-id="25892-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25892-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="25892-116">Cell</span><span class="sxs-lookup"><span data-stu-id="25892-116">Cell</span></span>](cell-element-ellipse-rowvisio-xml.md) <br/> |[<span data-ttu-id="25892-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="25892-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="25892-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="25892-118">Attributes</span></span>

<span data-ttu-id="25892-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25892-119">None.</span></span>
  

