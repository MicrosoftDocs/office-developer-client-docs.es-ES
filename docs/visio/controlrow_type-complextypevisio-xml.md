---
title: ControlRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f9ee251-e685-e56c-3c8a-cb727ad62064
ms.openlocfilehash: a6bd54f425e211716ce7dc9a7206a3d079383d5d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538672"
---
# <a name="controlrow_type-complextype-visio-xml"></a><span data-ttu-id="b4df5-102">ControlRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="b4df5-102">ControlRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b4df5-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b4df5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4df5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4df5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b4df5-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b4df5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b4df5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b4df5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b4df5-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b4df5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b4df5-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="b4df5-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4df5-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b4df5-109">Definition</span></span>

```XML
          <xs:complexType name="ControlRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="b4df5-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b4df5-110">Elements and attributes</span></span>

<span data-ttu-id="b4df5-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b4df5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b4df5-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4df5-112">Child elements</span></span>

|<span data-ttu-id="b4df5-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b4df5-113">**Element**</span></span>|<span data-ttu-id="b4df5-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4df5-114">**Type**</span></span>|<span data-ttu-id="b4df5-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4df5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4df5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="b4df5-116">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="b4df5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b4df5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b4df5-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4df5-118">Attributes</span></span>

<span data-ttu-id="b4df5-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4df5-119">None.</span></span>
  

