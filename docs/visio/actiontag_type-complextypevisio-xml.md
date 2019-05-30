---
title: ComplexType ActionTag_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: 864f4f9b5069fa3968ceb8d3a8db1589113d931a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541417"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="74d36-102">ComplexType ActionTag_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="74d36-102">ActionTag_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="74d36-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="74d36-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74d36-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="74d36-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="74d36-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="74d36-105">**Schema file**</span></span> <br/> |<span data-ttu-id="74d36-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="74d36-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="74d36-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="74d36-107">**Extension base**</span></span> <br/> |<span data-ttu-id="74d36-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="74d36-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="74d36-109">Definición</span><span class="sxs-lookup"><span data-stu-id="74d36-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="74d36-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="74d36-110">Elements and attributes</span></span>

<span data-ttu-id="74d36-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="74d36-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="74d36-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="74d36-112">Child elements</span></span>

|<span data-ttu-id="74d36-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="74d36-113">**Element**</span></span>|<span data-ttu-id="74d36-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="74d36-114">**Type**</span></span>|<span data-ttu-id="74d36-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74d36-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="74d36-116">Row</span><span class="sxs-lookup"><span data-stu-id="74d36-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="74d36-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="74d36-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="74d36-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="74d36-118">Attributes</span></span>

<span data-ttu-id="74d36-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="74d36-119">None.</span></span>
  

