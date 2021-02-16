---
title: RelMoveTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3759d7cc-061b-0c0b-c372-b7d60effbfd0
ms.openlocfilehash: 0b8c81b389244fe45b99c3fadde5c110c60d0393
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542761"
---
# <a name="relmoveto_type-complextype-visio-xml"></a><span data-ttu-id="890de-102">RelMoveTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="890de-102">RelMoveTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="890de-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="890de-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="890de-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="890de-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="890de-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="890de-105">**Schema file**</span></span> <br/> |<span data-ttu-id="890de-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="890de-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="890de-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="890de-107">**Extension base**</span></span> <br/> |<span data-ttu-id="890de-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="890de-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="890de-109">Definición</span><span class="sxs-lookup"><span data-stu-id="890de-109">Definition</span></span>

```XML
          <xs:complexType name="RelMoveTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="890de-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="890de-110">Elements and attributes</span></span>

<span data-ttu-id="890de-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="890de-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="890de-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="890de-112">Child elements</span></span>

|<span data-ttu-id="890de-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="890de-113">**Element**</span></span>|<span data-ttu-id="890de-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="890de-114">**Type**</span></span>|<span data-ttu-id="890de-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="890de-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="890de-116">Cell</span><span class="sxs-lookup"><span data-stu-id="890de-116">Cell</span></span>](cell-element-relmoveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="890de-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="890de-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="890de-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="890de-118">Attributes</span></span>

<span data-ttu-id="890de-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="890de-119">None.</span></span>
  

