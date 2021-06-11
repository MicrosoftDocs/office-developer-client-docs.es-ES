---
title: RelLineTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e5504166-653d-15d2-75eb-9b36f376b788
ms.openlocfilehash: 8681bf819a36a8c41171d558fb48b73fc1aeb87b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542712"
---
# <a name="rellineto_type-complextype-visio-xml"></a><span data-ttu-id="1d7dd-102">RelLineTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1d7dd-102">RelLineTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1d7dd-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1d7dd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d7dd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1d7dd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1d7dd-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1d7dd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1d7dd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1d7dd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1d7dd-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1d7dd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1d7dd-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="1d7dd-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d7dd-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1d7dd-109">Definition</span></span>

```XML
          <xs:complexType name="RelLineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="1d7dd-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1d7dd-110">Elements and attributes</span></span>

<span data-ttu-id="1d7dd-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1d7dd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1d7dd-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d7dd-112">Child elements</span></span>

|<span data-ttu-id="1d7dd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d7dd-113">**Element**</span></span>|<span data-ttu-id="1d7dd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1d7dd-114">**Type**</span></span>|<span data-ttu-id="1d7dd-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d7dd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d7dd-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1d7dd-116">Cell</span></span>](cell-element-rellineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="1d7dd-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1d7dd-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1d7dd-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d7dd-118">Attributes</span></span>

<span data-ttu-id="1d7dd-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d7dd-119">None.</span></span>
  

