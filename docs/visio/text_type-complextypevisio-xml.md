---
title: Text_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: cfacc84cb8b38acfbda3c37c669dd9714d899098
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541382"
---
# <a name="text_type-complextype-visio-xml"></a><span data-ttu-id="a1f3b-102">Text_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a1f3b-102">Text_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a1f3b-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a1f3b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1f3b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a1f3b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a1f3b-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a1f3b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a1f3b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a1f3b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a1f3b-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a1f3b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a1f3b-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a1f3b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1f3b-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a1f3b-109">Definition</span></span>

```XML
          <xs:complexType name="Text_Type">
          
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="cp"  type="cp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="pp"  type="pp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="tp"  type="tp_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="fld"  type="fld_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a1f3b-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a1f3b-110">Elements and attributes</span></span>

<span data-ttu-id="a1f3b-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a1f3b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a1f3b-112">Child elements</span></span>

|<span data-ttu-id="a1f3b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a1f3b-113">**Element**</span></span>|<span data-ttu-id="a1f3b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a1f3b-114">**Type**</span></span>|<span data-ttu-id="a1f3b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1f3b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1f3b-116">cp</span><span class="sxs-lookup"><span data-stu-id="a1f3b-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1f3b-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="a1f3b-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a1f3b-118">fld</span><span class="sxs-lookup"><span data-stu-id="a1f3b-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1f3b-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="a1f3b-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a1f3b-120">pp</span><span class="sxs-lookup"><span data-stu-id="a1f3b-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1f3b-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="a1f3b-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a1f3b-122">tp</span><span class="sxs-lookup"><span data-stu-id="a1f3b-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1f3b-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="a1f3b-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a1f3b-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="a1f3b-124">Attributes</span></span>

<span data-ttu-id="a1f3b-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1f3b-125">None.</span></span>
  

