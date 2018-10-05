---
title: PageContents_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: 70f28182d8c82b9283e793856f7944c9a4823bc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383432"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="e18c5-102">PageContents_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e18c5-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e18c5-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e18c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e18c5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e18c5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e18c5-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e18c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e18c5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e18c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e18c5-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e18c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e18c5-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e18c5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e18c5-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e18c5-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e18c5-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e18c5-110">Elements and attributes</span></span>

<span data-ttu-id="e18c5-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e18c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e18c5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e18c5-112">Child elements</span></span>

|<span data-ttu-id="e18c5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e18c5-113">**Element**</span></span>|<span data-ttu-id="e18c5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e18c5-114">**Type**</span></span>|<span data-ttu-id="e18c5-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e18c5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e18c5-116">Connects</span><span class="sxs-lookup"><span data-stu-id="e18c5-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e18c5-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="e18c5-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e18c5-118">Shapes</span><span class="sxs-lookup"><span data-stu-id="e18c5-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e18c5-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e18c5-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e18c5-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="e18c5-120">Attributes</span></span>

<span data-ttu-id="e18c5-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e18c5-121">None.</span></span>
  

