---
title: ParagraphRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32bb67e1-8db8-fe28-f173-028a20bb136c
ms.openlocfilehash: 64001e12b3e65e3259c3ebe381b2825fb80ad7b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338482"
---
# <a name="paragraphrowtype-complextype-visio-xml"></a><span data-ttu-id="8ff94-102">ParagraphRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="8ff94-102">ParagraphRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8ff94-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="8ff94-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ff94-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8ff94-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8ff94-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8ff94-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8ff94-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="8ff94-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8ff94-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="8ff94-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8ff94-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="8ff94-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ff94-109">Definición</span><span class="sxs-lookup"><span data-stu-id="8ff94-109">Definition</span></span>

```XML
          <xs:complexType name="ParagraphRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ff94-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8ff94-110">Elements and attributes</span></span>

<span data-ttu-id="8ff94-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8ff94-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8ff94-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ff94-112">Child elements</span></span>

|<span data-ttu-id="8ff94-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8ff94-113">**Element**</span></span>|<span data-ttu-id="8ff94-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8ff94-114">**Type**</span></span>|<span data-ttu-id="8ff94-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ff94-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ff94-116">Cell</span><span class="sxs-lookup"><span data-stu-id="8ff94-116">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8ff94-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8ff94-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8ff94-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ff94-118">Attributes</span></span>

<span data-ttu-id="8ff94-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8ff94-119">None.</span></span>
  

