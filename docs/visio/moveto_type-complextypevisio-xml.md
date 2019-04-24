---
title: MoveTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: f3c3ba2bfc789661f57c3d21634b5c876bc11f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283747"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="ed380-102">MoveTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ed380-102">MoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ed380-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ed380-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed380-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ed380-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ed380-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ed380-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ed380-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ed380-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ed380-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ed380-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ed380-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="ed380-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ed380-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ed380-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ed380-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ed380-110">Elements and attributes</span></span>

<span data-ttu-id="ed380-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ed380-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ed380-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed380-112">Child elements</span></span>

|<span data-ttu-id="ed380-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed380-113">**Element**</span></span>|<span data-ttu-id="ed380-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ed380-114">**Type**</span></span>|<span data-ttu-id="ed380-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed380-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ed380-116">Cell</span><span class="sxs-lookup"><span data-stu-id="ed380-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="ed380-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="ed380-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ed380-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed380-118">Attributes</span></span>

<span data-ttu-id="ed380-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed380-119">None.</span></span>
  

