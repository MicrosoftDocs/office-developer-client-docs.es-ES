---
title: ActionTag_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: a30290ee9dbb86c7af75820bd767bb95ce4add21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283061"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="53e8e-102">ActionTag_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="53e8e-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="53e8e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="53e8e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e8e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="53e8e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="53e8e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="53e8e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="53e8e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="53e8e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="53e8e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="53e8e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="53e8e-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="53e8e-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="53e8e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="53e8e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="53e8e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="53e8e-110">Elements and attributes</span></span>

<span data-ttu-id="53e8e-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="53e8e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="53e8e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53e8e-112">Child elements</span></span>

|<span data-ttu-id="53e8e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="53e8e-113">**Element**</span></span>|<span data-ttu-id="53e8e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="53e8e-114">**Type**</span></span>|<span data-ttu-id="53e8e-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53e8e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="53e8e-116">Row</span><span class="sxs-lookup"><span data-stu-id="53e8e-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="53e8e-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="53e8e-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="53e8e-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="53e8e-118">Attributes</span></span>

<span data-ttu-id="53e8e-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53e8e-119">None.</span></span>
  

