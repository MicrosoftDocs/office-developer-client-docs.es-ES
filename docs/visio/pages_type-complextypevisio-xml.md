---
title: Pages_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: 45a59c41e0f2bdb2c1b260a1803c7ac14a84a6ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822756"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="d0bfa-102">Pages_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="d0bfa-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d0bfa-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d0bfa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0bfa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0bfa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d0bfa-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d0bfa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d0bfa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d0bfa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d0bfa-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d0bfa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d0bfa-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d0bfa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0bfa-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d0bfa-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0bfa-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d0bfa-110">Elements and attributes</span></span>

<span data-ttu-id="d0bfa-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="d0bfa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d0bfa-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0bfa-112">Child elements</span></span>

|<span data-ttu-id="d0bfa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0bfa-113">**Element**</span></span>|<span data-ttu-id="d0bfa-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d0bfa-114">**Type**</span></span>|<span data-ttu-id="d0bfa-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0bfa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0bfa-116">Page</span><span class="sxs-lookup"><span data-stu-id="d0bfa-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0bfa-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="d0bfa-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d0bfa-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0bfa-118">Attributes</span></span>

<span data-ttu-id="d0bfa-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0bfa-119">None.</span></span>
  

