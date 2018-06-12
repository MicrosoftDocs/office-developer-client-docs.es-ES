---
title: RelQuadBezTo_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 558c7315-5025-484b-446e-333890bc1c3a
ms.openlocfilehash: 6cc7d2fa98e387f01900241fd65142163a35aeb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822948"
---
# <a name="relquadbeztotype-complextype-visio-xml"></a><span data-ttu-id="bcc8f-102">RelQuadBezTo_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="bcc8f-102">RelQuadBezTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bcc8f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="bcc8f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcc8f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bcc8f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bcc8f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bcc8f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bcc8f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bcc8f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bcc8f-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="bcc8f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bcc8f-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="bcc8f-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bcc8f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="bcc8f-109">Definition</span></span>

```XML
          <xs:complexType name="RelQuadBezTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="bcc8f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bcc8f-110">Elements and attributes</span></span>

<span data-ttu-id="bcc8f-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="bcc8f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bcc8f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bcc8f-112">Child elements</span></span>

|<span data-ttu-id="bcc8f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bcc8f-113">**Element**</span></span>|<span data-ttu-id="bcc8f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bcc8f-114">**Type**</span></span>|<span data-ttu-id="bcc8f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcc8f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bcc8f-116">Cell</span><span class="sxs-lookup"><span data-stu-id="bcc8f-116">Cell</span></span>](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[<span data-ttu-id="bcc8f-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bcc8f-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bcc8f-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="bcc8f-118">Attributes</span></span>

<span data-ttu-id="bcc8f-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bcc8f-119">None.</span></span>
  

