---
title: Solutions_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: b68955d2ed161d1ec0952b4a1b9d657fe0de81fc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540234"
---
# <a name="solutions_type-complextype-visio-xml"></a><span data-ttu-id="8f491-102">Solutions_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8f491-102">Solutions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8f491-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="8f491-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f491-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8f491-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8f491-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8f491-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8f491-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8f491-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8f491-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="8f491-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8f491-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8f491-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f491-109">Definición</span><span class="sxs-lookup"><span data-stu-id="8f491-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8f491-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8f491-110">Elements and attributes</span></span>

<span data-ttu-id="8f491-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8f491-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8f491-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f491-112">Child elements</span></span>

|<span data-ttu-id="8f491-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8f491-113">**Element**</span></span>|<span data-ttu-id="8f491-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8f491-114">**Type**</span></span>|<span data-ttu-id="8f491-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f491-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f491-116">Solution</span><span class="sxs-lookup"><span data-stu-id="8f491-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f491-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="8f491-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8f491-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f491-118">Attributes</span></span>

<span data-ttu-id="8f491-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8f491-119">None.</span></span>
  

