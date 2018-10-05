---
title: Colors_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: e447ceb6fc0e6b79ec6e62b5f3b73a32cec589d9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400918"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="e5a59-102">Colors_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e5a59-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e5a59-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e5a59-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5a59-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e5a59-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5a59-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e5a59-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5a59-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e5a59-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5a59-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e5a59-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5a59-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e5a59-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5a59-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e5a59-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e5a59-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e5a59-110">Elements and attributes</span></span>

<span data-ttu-id="e5a59-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e5a59-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5a59-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e5a59-112">Child elements</span></span>

|<span data-ttu-id="e5a59-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5a59-113">**Element**</span></span>|<span data-ttu-id="e5a59-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e5a59-114">**Type**</span></span>|<span data-ttu-id="e5a59-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5a59-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5a59-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="e5a59-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e5a59-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="e5a59-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e5a59-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="e5a59-118">Attributes</span></span>

<span data-ttu-id="e5a59-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e5a59-119">None.</span></span>
  

