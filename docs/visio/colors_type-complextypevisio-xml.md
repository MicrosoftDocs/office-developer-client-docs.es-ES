---
title: Colors_Type complexType (Visio XML)
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
# <a name="colors_type-complextype-visio-xml"></a><span data-ttu-id="926e8-102">Colors_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="926e8-102">Colors_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="926e8-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="926e8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="926e8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="926e8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="926e8-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="926e8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="926e8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="926e8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="926e8-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="926e8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="926e8-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="926e8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="926e8-109">Definición</span><span class="sxs-lookup"><span data-stu-id="926e8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="926e8-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="926e8-110">Elements and attributes</span></span>

<span data-ttu-id="926e8-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="926e8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="926e8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="926e8-112">Child elements</span></span>

|<span data-ttu-id="926e8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="926e8-113">**Element**</span></span>|<span data-ttu-id="926e8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="926e8-114">**Type**</span></span>|<span data-ttu-id="926e8-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="926e8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="926e8-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="926e8-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="926e8-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="926e8-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="926e8-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="926e8-118">Attributes</span></span>

<span data-ttu-id="926e8-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="926e8-119">None.</span></span>
  

