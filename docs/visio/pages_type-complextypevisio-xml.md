---
title: Pages_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400162"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="16d74-102">Pages_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="16d74-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="16d74-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="16d74-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16d74-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="16d74-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="16d74-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="16d74-105">**Schema file**</span></span> <br/> |<span data-ttu-id="16d74-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="16d74-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="16d74-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="16d74-107">**Extension base**</span></span> <br/> |<span data-ttu-id="16d74-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="16d74-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="16d74-109">Definición</span><span class="sxs-lookup"><span data-stu-id="16d74-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="16d74-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="16d74-110">Elements and attributes</span></span>

<span data-ttu-id="16d74-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="16d74-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="16d74-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="16d74-112">Child elements</span></span>

|<span data-ttu-id="16d74-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="16d74-113">**Element**</span></span>|<span data-ttu-id="16d74-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16d74-114">**Type**</span></span>|<span data-ttu-id="16d74-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16d74-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16d74-116">Page</span><span class="sxs-lookup"><span data-stu-id="16d74-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="16d74-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="16d74-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="16d74-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="16d74-118">Attributes</span></span>

<span data-ttu-id="16d74-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="16d74-119">None.</span></span>
  

