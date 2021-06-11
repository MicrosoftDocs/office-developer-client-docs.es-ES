---
title: Paragraph_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: fd7c5233b89bc92ed449d3d8d2767daa23ea8071
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540598"
---
# <a name="paragraph_type-complextype-visio-xml"></a><span data-ttu-id="08df5-102">Paragraph_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="08df5-102">Paragraph_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="08df5-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="08df5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08df5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08df5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="08df5-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="08df5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="08df5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="08df5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="08df5-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="08df5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="08df5-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="08df5-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08df5-109">Definición</span><span class="sxs-lookup"><span data-stu-id="08df5-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08df5-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="08df5-110">Elements and attributes</span></span>

<span data-ttu-id="08df5-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="08df5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="08df5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08df5-112">Child elements</span></span>

|<span data-ttu-id="08df5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08df5-113">**Element**</span></span>|<span data-ttu-id="08df5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08df5-114">**Type**</span></span>|<span data-ttu-id="08df5-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08df5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08df5-116">Row</span><span class="sxs-lookup"><span data-stu-id="08df5-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="08df5-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="08df5-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="08df5-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="08df5-118">Attributes</span></span>

<span data-ttu-id="08df5-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08df5-119">None.</span></span>
  

