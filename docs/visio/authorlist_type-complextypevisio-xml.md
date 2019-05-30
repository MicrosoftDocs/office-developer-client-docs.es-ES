---
title: ComplexType AuthorList_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: 5df48bcc69f0bd4aa818f265d0c7db1986165b3e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537902"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="c3478-102">ComplexType AuthorList_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="c3478-102">AuthorList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c3478-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c3478-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3478-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3478-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c3478-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c3478-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c3478-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c3478-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c3478-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c3478-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c3478-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c3478-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3478-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c3478-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c3478-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c3478-110">Elements and attributes</span></span>

<span data-ttu-id="c3478-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c3478-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c3478-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3478-112">Child elements</span></span>

|<span data-ttu-id="c3478-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c3478-113">**Element**</span></span>|<span data-ttu-id="c3478-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3478-114">**Type**</span></span>|<span data-ttu-id="c3478-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3478-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3478-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="c3478-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3478-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c3478-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c3478-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3478-118">Attributes</span></span>

<span data-ttu-id="c3478-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c3478-119">None.</span></span>
  

