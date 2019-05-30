---
title: ComplexType Colors_Type (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: bddcb93451bfb6d1b519720040a9e3875dc2ec5c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540143"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="9f9fe-102">ComplexType Colors_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="9f9fe-102">Colors_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9f9fe-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9f9fe-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f9fe-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9f9fe-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9f9fe-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9f9fe-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9f9fe-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9f9fe-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9f9fe-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9f9fe-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9f9fe-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9f9fe-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9f9fe-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9f9fe-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9f9fe-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9f9fe-110">Elements and attributes</span></span>

<span data-ttu-id="9f9fe-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9f9fe-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9f9fe-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9f9fe-112">Child elements</span></span>

|<span data-ttu-id="9f9fe-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9f9fe-113">**Element**</span></span>|<span data-ttu-id="9f9fe-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9f9fe-114">**Type**</span></span>|<span data-ttu-id="9f9fe-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9f9fe-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9f9fe-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="9f9fe-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9f9fe-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="9f9fe-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9f9fe-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f9fe-118">Attributes</span></span>

<span data-ttu-id="9f9fe-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9f9fe-119">None.</span></span>
  

