---
title: EllipticalArcTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dc10f727-5243-2fdb-4042-3dfdfcd8504c
ms.openlocfilehash: 98ff424d0037a9b86749480779d89370c4962caa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539901"
---
# <a name="ellipticalarcto_type-complextype-visio-xml"></a><span data-ttu-id="2b661-102">EllipticalArcTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2b661-102">EllipticalArcTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2b661-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2b661-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b661-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2b661-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2b661-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2b661-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2b661-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2b661-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2b661-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2b661-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2b661-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2b661-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b661-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2b661-109">Definition</span></span>

```XML
          <xs:complexType name="EllipticalArcTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="2b661-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2b661-110">Elements and attributes</span></span>

<span data-ttu-id="2b661-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2b661-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2b661-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2b661-112">Child elements</span></span>

|<span data-ttu-id="2b661-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2b661-113">**Element**</span></span>|<span data-ttu-id="2b661-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2b661-114">**Type**</span></span>|<span data-ttu-id="2b661-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b661-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b661-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2b661-116">Cell</span></span>](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[<span data-ttu-id="2b661-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2b661-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2b661-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2b661-118">Attributes</span></span>

<span data-ttu-id="2b661-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2b661-119">None.</span></span>
  

