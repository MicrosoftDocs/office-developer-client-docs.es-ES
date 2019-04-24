---
title: LineGradient_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 5918e306479b907760fb539c3e476708d28de5e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359292"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="ca48a-102">LineGradient_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ca48a-102">LineGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ca48a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ca48a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca48a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ca48a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ca48a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ca48a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ca48a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="ca48a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ca48a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ca48a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ca48a-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="ca48a-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca48a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ca48a-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca48a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ca48a-110">Elements and attributes</span></span>

<span data-ttu-id="ca48a-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ca48a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ca48a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ca48a-112">Child elements</span></span>

|<span data-ttu-id="ca48a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ca48a-113">**Element**</span></span>|<span data-ttu-id="ca48a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ca48a-114">**Type**</span></span>|<span data-ttu-id="ca48a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca48a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca48a-116">Row</span><span class="sxs-lookup"><span data-stu-id="ca48a-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="ca48a-117">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="ca48a-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ca48a-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="ca48a-118">Attributes</span></span>

<span data-ttu-id="ca48a-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ca48a-119">None.</span></span>
  

