---
title: Extensions_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 1da1418e2256f7750ac2e963bac0f78321233c99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822108"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="79034-102">Extensions_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="79034-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="79034-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="79034-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79034-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="79034-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="79034-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="79034-105">**Schema file**</span></span> <br/> |<span data-ttu-id="79034-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="79034-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="79034-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="79034-107">**Extension base**</span></span> <br/> |<span data-ttu-id="79034-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="79034-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="79034-109">Definición</span><span class="sxs-lookup"><span data-stu-id="79034-109">Definition</span></span>

```XML
          <xs:complexType name="Extensions_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="FunctionDef"  type="FunctionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="SectionDef"  type="SectionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="79034-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="79034-110">Elements and attributes</span></span>

<span data-ttu-id="79034-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="79034-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="79034-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="79034-112">Child elements</span></span>

|<span data-ttu-id="79034-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="79034-113">**Element**</span></span>|<span data-ttu-id="79034-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="79034-114">**Type**</span></span>|<span data-ttu-id="79034-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79034-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79034-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="79034-116">CellDef</span></span>](http://msdn.microsoft.com/library/8fb193f0-5c88-6891-1cda-f1df486aabfc%28Office.15%29.aspx) <br/> |[<span data-ttu-id="79034-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="79034-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="79034-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="79034-118">FunctionDef</span></span>](http://msdn.microsoft.com/library/dad99181-c14c-cce7-3883-106fe05f20a6%28Office.15%29.aspx) <br/> |[<span data-ttu-id="79034-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="79034-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="79034-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="79034-120">SectionDef</span></span>](http://msdn.microsoft.com/library/751da480-f387-4c68-6699-8948271c23ac%28Office.15%29.aspx) <br/> |[<span data-ttu-id="79034-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="79034-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="79034-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="79034-122">Attributes</span></span>

<span data-ttu-id="79034-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="79034-123">None.</span></span>
  
