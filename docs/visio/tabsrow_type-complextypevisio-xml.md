---
title: TabsRow_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b9258a0-05fa-b0b0-90ed-dc1c4faa288a
ms.openlocfilehash: fed6c70119007164113ba76296bed5662e331c17
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395325"
---
# <a name="tabsrowtype-complextype-visio-xml"></a><span data-ttu-id="229b0-102">TabsRow_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="229b0-102">TabsRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="229b0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="229b0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="229b0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="229b0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="229b0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="229b0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="229b0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="229b0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="229b0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="229b0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="229b0-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="229b0-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="229b0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="229b0-109">Definition</span></span>

```XML
          <xs:complexType name="TabsRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="229b0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="229b0-110">Elements and attributes</span></span>

<span data-ttu-id="229b0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="229b0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="229b0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="229b0-112">Child elements</span></span>

|<span data-ttu-id="229b0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="229b0-113">**Element**</span></span>|<span data-ttu-id="229b0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="229b0-114">**Type**</span></span>|<span data-ttu-id="229b0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="229b0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="229b0-116">Cell</span><span class="sxs-lookup"><span data-stu-id="229b0-116">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="229b0-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="229b0-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="229b0-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="229b0-118">Attributes</span></span>

<span data-ttu-id="229b0-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="229b0-119">None.</span></span>
  

