---
title: Extensions_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 7760e1b22a7d573d8f61cf08ed54789f601e9339
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351089"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="f236a-102">Extensions_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f236a-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f236a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f236a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f236a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f236a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f236a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f236a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f236a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f236a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f236a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f236a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f236a-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f236a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f236a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f236a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f236a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f236a-110">Elements and attributes</span></span>

<span data-ttu-id="f236a-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f236a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f236a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f236a-112">Child elements</span></span>

|<span data-ttu-id="f236a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f236a-113">**Element**</span></span>|<span data-ttu-id="f236a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f236a-114">**Type**</span></span>|<span data-ttu-id="f236a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f236a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f236a-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="f236a-116">CellDef</span></span> <br/> |[<span data-ttu-id="f236a-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="f236a-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="f236a-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="f236a-118">FunctionDef</span></span> <br/> |[<span data-ttu-id="f236a-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="f236a-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="f236a-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="f236a-120">SectionDef</span></span> <br/> |[<span data-ttu-id="f236a-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="f236a-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f236a-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="f236a-122">Attributes</span></span>

<span data-ttu-id="f236a-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f236a-123">None.</span></span>
  

