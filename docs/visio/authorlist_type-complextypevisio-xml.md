---
title: AuthorList_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: e4cee87a5060580e8b7f1efc7970091d56fd310f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821525"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="aed9a-102">AuthorList_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="aed9a-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aed9a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="aed9a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aed9a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aed9a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aed9a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aed9a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aed9a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aed9a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aed9a-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="aed9a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aed9a-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="aed9a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aed9a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="aed9a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="aed9a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="aed9a-110">Elements and attributes</span></span>

<span data-ttu-id="aed9a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="aed9a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aed9a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aed9a-112">Child elements</span></span>

|<span data-ttu-id="aed9a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="aed9a-113">**Element**</span></span>|<span data-ttu-id="aed9a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aed9a-114">**Type**</span></span>|<span data-ttu-id="aed9a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aed9a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aed9a-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="aed9a-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aed9a-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="aed9a-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aed9a-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="aed9a-118">Attributes</span></span>

<span data-ttu-id="aed9a-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aed9a-119">None.</span></span>
  

