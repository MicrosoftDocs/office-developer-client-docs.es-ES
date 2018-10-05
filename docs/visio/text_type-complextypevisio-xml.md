---
title: Text_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc6b37c3-7f55-fe18-a9b7-884ea87b3f46
ms.openlocfilehash: fe74af493983122c113e48ae5c0bb3b5b037ccef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384790"
---
# <a name="texttype-complextype-visio-xml"></a><span data-ttu-id="864a2-102">Text_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="864a2-102">Text_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="864a2-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="864a2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="864a2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="864a2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="864a2-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="864a2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="864a2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="864a2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="864a2-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="864a2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="864a2-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="864a2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="864a2-109">Definición</span><span class="sxs-lookup"><span data-stu-id="864a2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="864a2-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="864a2-110">Elements and attributes</span></span>

<span data-ttu-id="864a2-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="864a2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="864a2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="864a2-112">Child elements</span></span>

|<span data-ttu-id="864a2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="864a2-113">**Element**</span></span>|<span data-ttu-id="864a2-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="864a2-114">**Type**</span></span>|<span data-ttu-id="864a2-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="864a2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="864a2-116">CP</span><span class="sxs-lookup"><span data-stu-id="864a2-116">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="864a2-117">cp_Type</span><span class="sxs-lookup"><span data-stu-id="864a2-117">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="864a2-118">fld</span><span class="sxs-lookup"><span data-stu-id="864a2-118">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="864a2-119">fld_Type</span><span class="sxs-lookup"><span data-stu-id="864a2-119">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="864a2-120">PP</span><span class="sxs-lookup"><span data-stu-id="864a2-120">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="864a2-121">pp_Type</span><span class="sxs-lookup"><span data-stu-id="864a2-121">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="864a2-122">TP</span><span class="sxs-lookup"><span data-stu-id="864a2-122">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="864a2-123">tp_Type</span><span class="sxs-lookup"><span data-stu-id="864a2-123">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="864a2-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="864a2-124">Attributes</span></span>

<span data-ttu-id="864a2-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="864a2-125">None.</span></span>
  

