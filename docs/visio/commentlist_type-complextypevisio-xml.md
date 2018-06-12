---
title: CommentList_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 640ba8825ffdfaa92c7a7ce43fb6bfb92e19ce12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821792"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="10472-102">CommentList_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="10472-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="10472-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="10472-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10472-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10472-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="10472-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="10472-105">**Schema file**</span></span> <br/> |<span data-ttu-id="10472-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="10472-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="10472-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="10472-107">**Extension base**</span></span> <br/> |<span data-ttu-id="10472-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="10472-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10472-109">Definición</span><span class="sxs-lookup"><span data-stu-id="10472-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10472-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="10472-110">Elements and attributes</span></span>

<span data-ttu-id="10472-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="10472-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="10472-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="10472-112">Child elements</span></span>

|<span data-ttu-id="10472-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="10472-113">**Element**</span></span>|<span data-ttu-id="10472-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="10472-114">**Type**</span></span>|<span data-ttu-id="10472-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10472-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10472-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="10472-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10472-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="10472-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="10472-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="10472-118">Attributes</span></span>

<span data-ttu-id="10472-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="10472-119">None.</span></span>
  

