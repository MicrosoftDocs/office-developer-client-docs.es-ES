---
title: Solutions_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: 69c5bf92bb9f72e9969f9687b42b9d583eb2a523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823299"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="0ae4e-102">Solutions_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0ae4e-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0ae4e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0ae4e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ae4e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0ae4e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0ae4e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0ae4e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0ae4e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0ae4e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0ae4e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0ae4e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0ae4e-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0ae4e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ae4e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0ae4e-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ae4e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0ae4e-110">Elements and attributes</span></span>

<span data-ttu-id="0ae4e-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0ae4e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0ae4e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ae4e-112">Child elements</span></span>

|<span data-ttu-id="0ae4e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ae4e-113">**Element**</span></span>|<span data-ttu-id="0ae4e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ae4e-114">**Type**</span></span>|<span data-ttu-id="0ae4e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ae4e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ae4e-116">Solution</span><span class="sxs-lookup"><span data-stu-id="0ae4e-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ae4e-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="0ae4e-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0ae4e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ae4e-118">Attributes</span></span>

<span data-ttu-id="0ae4e-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ae4e-119">None.</span></span>
  

