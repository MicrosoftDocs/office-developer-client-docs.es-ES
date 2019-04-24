---
title: Solutions_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: bf43b971399ec69c6f73cbfaaa6cade8c583d3c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334429"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="9e488-102">Solutions_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9e488-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9e488-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9e488-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e488-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9e488-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9e488-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9e488-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9e488-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9e488-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9e488-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9e488-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9e488-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9e488-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9e488-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9e488-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9e488-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9e488-110">Elements and attributes</span></span>

<span data-ttu-id="9e488-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9e488-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9e488-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9e488-112">Child elements</span></span>

|<span data-ttu-id="9e488-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9e488-113">**Element**</span></span>|<span data-ttu-id="9e488-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9e488-114">**Type**</span></span>|<span data-ttu-id="9e488-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e488-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9e488-116">Solution</span><span class="sxs-lookup"><span data-stu-id="9e488-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9e488-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="9e488-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9e488-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9e488-118">Attributes</span></span>

<span data-ttu-id="9e488-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9e488-119">None.</span></span>
  

