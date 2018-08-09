---
title: Colors_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: 187d51c2102e9d13ffea15c6de2db849ef980fb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821770"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="306ba-102">Colors_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="306ba-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="306ba-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="306ba-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="306ba-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="306ba-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="306ba-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="306ba-105">**Schema file**</span></span> <br/> |<span data-ttu-id="306ba-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="306ba-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="306ba-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="306ba-107">**Extension base**</span></span> <br/> |<span data-ttu-id="306ba-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="306ba-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="306ba-109">Definición</span><span class="sxs-lookup"><span data-stu-id="306ba-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="306ba-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="306ba-110">Elements and attributes</span></span>

<span data-ttu-id="306ba-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="306ba-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="306ba-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="306ba-112">Child elements</span></span>

|<span data-ttu-id="306ba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="306ba-113">**Element**</span></span>|<span data-ttu-id="306ba-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="306ba-114">**Type**</span></span>|<span data-ttu-id="306ba-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="306ba-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="306ba-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="306ba-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="306ba-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="306ba-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="306ba-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="306ba-118">Attributes</span></span>

<span data-ttu-id="306ba-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="306ba-119">None.</span></span>
  

