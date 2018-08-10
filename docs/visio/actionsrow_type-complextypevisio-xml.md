---
title: ActionsRow_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32777219-850b-9526-425f-bcb017c45093
ms.openlocfilehash: f8590201e4b7a3c547e267586d3ccdccf727a0aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821503"
---
# <a name="actionsrowtype-complextype-visio-xml"></a><span data-ttu-id="6ea72-102">ActionsRow_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="6ea72-102">ActionsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6ea72-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6ea72-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ea72-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6ea72-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6ea72-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6ea72-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6ea72-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6ea72-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6ea72-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6ea72-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6ea72-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="6ea72-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ea72-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6ea72-109">Definition</span></span>

```XML
          <xs:complexType name="ActionsRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ea72-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6ea72-110">Elements and attributes</span></span>

<span data-ttu-id="6ea72-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6ea72-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6ea72-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ea72-112">Child elements</span></span>

|<span data-ttu-id="6ea72-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ea72-113">**Element**</span></span>|<span data-ttu-id="6ea72-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6ea72-114">**Type**</span></span>|<span data-ttu-id="6ea72-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ea72-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ea72-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6ea72-116">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="6ea72-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6ea72-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6ea72-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ea72-118">Attributes</span></span>

<span data-ttu-id="6ea72-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6ea72-119">None.</span></span>
  

