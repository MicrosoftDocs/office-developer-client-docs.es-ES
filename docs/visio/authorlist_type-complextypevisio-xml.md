---
title: AuthorList_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 80a0dd01b3628bc44ed469ff7c236753d7677f51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338748"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="cc1f9-102">AuthorList_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cc1f9-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cc1f9-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cc1f9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc1f9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc1f9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc1f9-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc1f9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc1f9-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="cc1f9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc1f9-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="cc1f9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc1f9-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cc1f9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc1f9-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cc1f9-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc1f9-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cc1f9-110">Elements and attributes</span></span>

<span data-ttu-id="cc1f9-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cc1f9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc1f9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc1f9-112">Child elements</span></span>

|<span data-ttu-id="cc1f9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc1f9-113">**Element**</span></span>|<span data-ttu-id="cc1f9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc1f9-114">**Type**</span></span>|<span data-ttu-id="cc1f9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc1f9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc1f9-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="cc1f9-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc1f9-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="cc1f9-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cc1f9-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc1f9-118">Attributes</span></span>

<span data-ttu-id="cc1f9-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc1f9-119">None.</span></span>
  

