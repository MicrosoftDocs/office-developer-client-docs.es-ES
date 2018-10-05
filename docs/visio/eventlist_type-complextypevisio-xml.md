---
title: EventList_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392084"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="1f125-102">EventList_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="1f125-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1f125-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1f125-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f125-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1f125-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1f125-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1f125-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1f125-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1f125-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1f125-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1f125-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1f125-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1f125-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1f125-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1f125-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1f125-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1f125-110">Elements and attributes</span></span>

<span data-ttu-id="1f125-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="1f125-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1f125-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f125-112">Child elements</span></span>

|<span data-ttu-id="1f125-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f125-113">**Element**</span></span>|<span data-ttu-id="1f125-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1f125-114">**Type**</span></span>|<span data-ttu-id="1f125-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1f125-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1f125-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="1f125-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1f125-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="1f125-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1f125-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f125-118">Attributes</span></span>

<span data-ttu-id="1f125-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1f125-119">None.</span></span>
  

