---
title: PageContents_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d611c03f-6a4f-9de2-6714-87131cddce85
ms.openlocfilehash: ab74c646e72a7ebe5fbf5863c196d5b115be9b43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822710"
---
# <a name="pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="64063-102">PageContents_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="64063-102">PageContents_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="64063-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="64063-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64063-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64063-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="64063-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="64063-105">**Schema file**</span></span> <br/> |<span data-ttu-id="64063-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="64063-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="64063-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="64063-107">**Extension base**</span></span> <br/> |<span data-ttu-id="64063-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="64063-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64063-109">Definición</span><span class="sxs-lookup"><span data-stu-id="64063-109">Definition</span></span>

```XML
          <xs:complexType name="PageContents_Type">
          
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Connects"  type="Connects_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="64063-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="64063-110">Elements and attributes</span></span>

<span data-ttu-id="64063-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="64063-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="64063-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64063-112">Child elements</span></span>

|<span data-ttu-id="64063-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="64063-113">**Element**</span></span>|<span data-ttu-id="64063-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64063-114">**Type**</span></span>|<span data-ttu-id="64063-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64063-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64063-116">Se conecta</span><span class="sxs-lookup"><span data-stu-id="64063-116">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64063-117">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="64063-117">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="64063-118">Shapes</span><span class="sxs-lookup"><span data-stu-id="64063-118">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64063-119">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="64063-119">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="64063-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="64063-120">Attributes</span></span>

<span data-ttu-id="64063-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="64063-121">None.</span></span>
  

