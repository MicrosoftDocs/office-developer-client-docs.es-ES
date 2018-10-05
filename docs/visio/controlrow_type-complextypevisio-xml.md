---
title: ControlRow_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f9ee251-e685-e56c-3c8a-cb727ad62064
ms.openlocfilehash: 7cd09b4644cc72648bf880a3c187fa59274e6e02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391804"
---
# <a name="controlrowtype-complextype-visio-xml"></a><span data-ttu-id="db2f3-102">ControlRow_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="db2f3-102">ControlRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="db2f3-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="db2f3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db2f3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db2f3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="db2f3-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="db2f3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="db2f3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="db2f3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="db2f3-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="db2f3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="db2f3-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="db2f3-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db2f3-109">Definición</span><span class="sxs-lookup"><span data-stu-id="db2f3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="db2f3-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="db2f3-110">Elements and attributes</span></span>

<span data-ttu-id="db2f3-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="db2f3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="db2f3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="db2f3-112">Child elements</span></span>

|<span data-ttu-id="db2f3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="db2f3-113">**Element**</span></span>|<span data-ttu-id="db2f3-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="db2f3-114">**Type**</span></span>|<span data-ttu-id="db2f3-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db2f3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db2f3-116">Cell</span><span class="sxs-lookup"><span data-stu-id="db2f3-116">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="db2f3-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="db2f3-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="db2f3-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="db2f3-118">Attributes</span></span>

<span data-ttu-id="db2f3-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="db2f3-119">None.</span></span>
  

