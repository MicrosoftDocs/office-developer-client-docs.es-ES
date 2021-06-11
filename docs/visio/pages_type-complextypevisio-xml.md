---
title: Pages_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: 4615f365448b96981088352f9f2d6e98255e4101
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538945"
---
# <a name="pages_type-complextype-visio-xml"></a><span data-ttu-id="bd352-102">Pages_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bd352-102">Pages_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bd352-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="bd352-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd352-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd352-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bd352-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bd352-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bd352-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bd352-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bd352-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="bd352-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bd352-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bd352-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd352-109">Definición</span><span class="sxs-lookup"><span data-stu-id="bd352-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bd352-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bd352-110">Elements and attributes</span></span>

<span data-ttu-id="bd352-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="bd352-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bd352-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bd352-112">Child elements</span></span>

|<span data-ttu-id="bd352-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bd352-113">**Element**</span></span>|<span data-ttu-id="bd352-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bd352-114">**Type**</span></span>|<span data-ttu-id="bd352-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd352-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bd352-116">Page</span><span class="sxs-lookup"><span data-stu-id="bd352-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bd352-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="bd352-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bd352-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd352-118">Attributes</span></span>

<span data-ttu-id="bd352-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bd352-119">None.</span></span>
  

