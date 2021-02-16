---
title: LineGradientRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: 9c39ddd971f3089bb8b87026616c455e6a0524eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541144"
---
# <a name="linegradientrow_type-complextype-visio-xml"></a><span data-ttu-id="85245-102">LineGradientRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="85245-102">LineGradientRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="85245-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="85245-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85245-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85245-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85245-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85245-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85245-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="85245-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85245-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="85245-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85245-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="85245-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85245-109">Definición</span><span class="sxs-lookup"><span data-stu-id="85245-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="85245-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="85245-110">Elements and attributes</span></span>

<span data-ttu-id="85245-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="85245-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85245-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85245-112">Child elements</span></span>

|<span data-ttu-id="85245-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85245-113">**Element**</span></span>|<span data-ttu-id="85245-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85245-114">**Type**</span></span>|<span data-ttu-id="85245-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85245-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85245-116">Cell</span><span class="sxs-lookup"><span data-stu-id="85245-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="85245-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="85245-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85245-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="85245-118">Attributes</span></span>

<span data-ttu-id="85245-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="85245-119">None.</span></span>
  

