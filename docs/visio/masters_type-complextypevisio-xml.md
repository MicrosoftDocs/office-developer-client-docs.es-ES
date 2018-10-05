---
title: Masters_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398496"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="5b2dc-102">Masters_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="5b2dc-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5b2dc-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5b2dc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b2dc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b2dc-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5b2dc-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5b2dc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5b2dc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5b2dc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5b2dc-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="5b2dc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5b2dc-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5b2dc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b2dc-109">Definición</span><span class="sxs-lookup"><span data-stu-id="5b2dc-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b2dc-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5b2dc-110">Elements and attributes</span></span>

<span data-ttu-id="5b2dc-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="5b2dc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5b2dc-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b2dc-112">Child elements</span></span>

|<span data-ttu-id="5b2dc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b2dc-113">**Element**</span></span>|<span data-ttu-id="5b2dc-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5b2dc-114">**Type**</span></span>|<span data-ttu-id="5b2dc-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b2dc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b2dc-116">Master</span><span class="sxs-lookup"><span data-stu-id="5b2dc-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b2dc-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="5b2dc-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5b2dc-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="5b2dc-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b2dc-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="5b2dc-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5b2dc-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b2dc-120">Attributes</span></span>

<span data-ttu-id="5b2dc-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b2dc-121">None.</span></span>
  

