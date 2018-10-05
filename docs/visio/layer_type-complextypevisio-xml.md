---
title: Layer_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f92ac1cc-fad2-dab9-5507-838c006ed633
ms.openlocfilehash: 9e6e477e97a0c8f1be1a89bd14262bb4c2a0d7dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396709"
---
# <a name="layertype-complextype-visio-xml"></a><span data-ttu-id="2222f-102">Layer_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="2222f-102">Layer_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2222f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2222f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2222f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2222f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2222f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2222f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2222f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2222f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2222f-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2222f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2222f-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="2222f-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2222f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2222f-109">Definition</span></span>

```XML
          <xs:complexType name="Layer_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LayerRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2222f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2222f-110">Elements and attributes</span></span>

<span data-ttu-id="2222f-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="2222f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2222f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2222f-112">Child elements</span></span>

|<span data-ttu-id="2222f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2222f-113">**Element**</span></span>|<span data-ttu-id="2222f-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2222f-114">**Type**</span></span>|<span data-ttu-id="2222f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2222f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2222f-116">Row</span><span class="sxs-lookup"><span data-stu-id="2222f-116">Row</span></span>](row-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2222f-117">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="2222f-117">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2222f-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2222f-118">Attributes</span></span>

<span data-ttu-id="2222f-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2222f-119">None.</span></span>
  

