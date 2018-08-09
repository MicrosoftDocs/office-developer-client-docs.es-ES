---
title: MoveTo_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: ea88f86ad9e38692408730b49ee2f3d6cbc35a54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822664"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="1a76e-102">MoveTo_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="1a76e-102">MoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1a76e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1a76e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a76e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1a76e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1a76e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1a76e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1a76e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1a76e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1a76e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1a76e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1a76e-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="1a76e-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a76e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1a76e-109">Definition</span></span>

```XML
          <xs:complexType name="MoveTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1a76e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1a76e-110">Elements and attributes</span></span>

<span data-ttu-id="1a76e-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="1a76e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1a76e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1a76e-112">Child elements</span></span>

|<span data-ttu-id="1a76e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a76e-113">**Element**</span></span>|<span data-ttu-id="1a76e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1a76e-114">**Type**</span></span>|<span data-ttu-id="1a76e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a76e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1a76e-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1a76e-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="1a76e-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1a76e-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1a76e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a76e-118">Attributes</span></span>

<span data-ttu-id="1a76e-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1a76e-119">None.</span></span>
  

