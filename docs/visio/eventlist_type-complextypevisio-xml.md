---
title: EventList_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: bcee61ba9347dc77dd704d0221a9362843bf9858
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540766"
---
# <a name="eventlist_type-complextype-visio-xml"></a><span data-ttu-id="d4b82-102">EventList_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d4b82-102">EventList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d4b82-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d4b82-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4b82-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d4b82-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d4b82-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d4b82-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d4b82-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d4b82-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d4b82-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d4b82-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d4b82-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d4b82-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d4b82-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d4b82-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d4b82-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d4b82-110">Elements and attributes</span></span>

<span data-ttu-id="d4b82-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d4b82-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d4b82-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d4b82-112">Child elements</span></span>

|<span data-ttu-id="d4b82-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d4b82-113">**Element**</span></span>|<span data-ttu-id="d4b82-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d4b82-114">**Type**</span></span>|<span data-ttu-id="d4b82-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4b82-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d4b82-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="d4b82-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4b82-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="d4b82-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d4b82-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4b82-118">Attributes</span></span>

<span data-ttu-id="d4b82-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d4b82-119">None.</span></span>
  

