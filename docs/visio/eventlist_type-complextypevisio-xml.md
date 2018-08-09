---
title: EventList_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 7bbb8d1074d869a9171a188118c920260b3a903d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822089"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="31391-102">EventList_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="31391-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="31391-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="31391-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31391-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="31391-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="31391-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="31391-105">**Schema file**</span></span> <br/> |<span data-ttu-id="31391-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="31391-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="31391-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="31391-107">**Extension base**</span></span> <br/> |<span data-ttu-id="31391-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="31391-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31391-109">Definición</span><span class="sxs-lookup"><span data-stu-id="31391-109">Definition</span></span>

```XML
          <xs:complexType name="EventList_Type">
          
          <xs:sequence>
    <xs:element name="EventItem"  type="EventItem_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="31391-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="31391-110">Elements and attributes</span></span>

<span data-ttu-id="31391-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="31391-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="31391-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31391-112">Child elements</span></span>

|<span data-ttu-id="31391-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="31391-113">**Element**</span></span>|<span data-ttu-id="31391-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="31391-114">**Type**</span></span>|<span data-ttu-id="31391-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31391-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31391-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="31391-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="31391-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="31391-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="31391-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="31391-118">Attributes</span></span>

<span data-ttu-id="31391-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31391-119">None.</span></span>
  

