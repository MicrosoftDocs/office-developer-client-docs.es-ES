---
title: LineTo_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 15859b84-5486-bb8c-e67e-5d0baaf59ee5
ms.openlocfilehash: 2291d7967ff08cc7a7d949d7a40feb178f16b497
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358978"
---
# <a name="linetotype-complextype-visio-xml"></a><span data-ttu-id="c8759-102">LineTo_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="c8759-102">LineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c8759-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c8759-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8759-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c8759-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c8759-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c8759-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c8759-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c8759-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c8759-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c8759-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c8759-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="c8759-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8759-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c8759-109">Definition</span></span>

```XML
          <xs:complexType name="LineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="c8759-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c8759-110">Elements and attributes</span></span>

<span data-ttu-id="c8759-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c8759-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c8759-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8759-112">Child elements</span></span>

|<span data-ttu-id="c8759-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8759-113">**Element**</span></span>|<span data-ttu-id="c8759-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8759-114">**Type**</span></span>|<span data-ttu-id="c8759-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8759-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8759-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c8759-116">Cell</span></span>](cell-element-lineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="c8759-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c8759-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c8759-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8759-118">Attributes</span></span>

<span data-ttu-id="c8759-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c8759-119">None.</span></span>
  

