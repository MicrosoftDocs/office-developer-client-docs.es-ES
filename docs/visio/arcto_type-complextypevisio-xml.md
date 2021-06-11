---
title: ArcTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c30c80eb-6327-ebc3-7ea4-8b2fc7525cc0
ms.openlocfilehash: 7fb07f7424e78ffa7b9efec190b839fd7713884a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539701"
---
# <a name="arcto_type-complextype-visio-xml"></a><span data-ttu-id="02755-102">ArcTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="02755-102">ArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="02755-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="02755-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02755-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02755-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="02755-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="02755-105">**Schema file**</span></span> <br/> |<span data-ttu-id="02755-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="02755-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="02755-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="02755-107">**Extension base**</span></span> <br/> |<span data-ttu-id="02755-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="02755-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02755-109">Definición</span><span class="sxs-lookup"><span data-stu-id="02755-109">Definition</span></span>

```XML
          <xs:complexType name="ArcTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="02755-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="02755-110">Elements and attributes</span></span>

<span data-ttu-id="02755-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="02755-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="02755-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02755-112">Child elements</span></span>

|<span data-ttu-id="02755-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="02755-113">**Element**</span></span>|<span data-ttu-id="02755-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="02755-114">**Type**</span></span>|<span data-ttu-id="02755-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02755-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02755-116">Cell</span><span class="sxs-lookup"><span data-stu-id="02755-116">Cell</span></span>](cell-element-arcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="02755-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="02755-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="02755-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="02755-118">Attributes</span></span>

<span data-ttu-id="02755-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02755-119">None.</span></span>
  

