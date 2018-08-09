---
title: Hyperlink_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 226af4fee615b0dc6ddc4d92d13aff6dd1fd4b19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822286"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="b5dd0-102">Hyperlink_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b5dd0-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b5dd0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b5dd0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5dd0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b5dd0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b5dd0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b5dd0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b5dd0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b5dd0-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="b5dd0-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5dd0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b5dd0-109">Definition</span></span>

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5dd0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b5dd0-110">Elements and attributes</span></span>

<span data-ttu-id="b5dd0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b5dd0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5dd0-112">Child elements</span></span>

|<span data-ttu-id="b5dd0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-113">**Element**</span></span>|<span data-ttu-id="b5dd0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-114">**Type**</span></span>|<span data-ttu-id="b5dd0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5dd0-116">Row</span><span class="sxs-lookup"><span data-stu-id="b5dd0-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b5dd0-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="b5dd0-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b5dd0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5dd0-118">Attributes</span></span>

<span data-ttu-id="b5dd0-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-119">None.</span></span>
  

