---
title: ScratchRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: 74f106f34596ca4ff2c200e0127155f4df54da28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327002"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="b01b9-102">ScratchRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b01b9-102">ScratchRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b01b9-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b01b9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b01b9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b01b9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b01b9-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b01b9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b01b9-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b01b9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b01b9-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b01b9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b01b9-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="b01b9-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b01b9-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b01b9-109">Definition</span></span>

```XML
          <xs:complexType name="ScratchRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="b01b9-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b01b9-110">Elements and attributes</span></span>

<span data-ttu-id="b01b9-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b01b9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b01b9-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b01b9-112">Child elements</span></span>

|<span data-ttu-id="b01b9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b01b9-113">**Element**</span></span>|<span data-ttu-id="b01b9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b01b9-114">**Type**</span></span>|<span data-ttu-id="b01b9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b01b9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b01b9-116">Cell</span><span class="sxs-lookup"><span data-stu-id="b01b9-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b01b9-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b01b9-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b01b9-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b01b9-118">Attributes</span></span>

<span data-ttu-id="b01b9-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b01b9-119">None.</span></span>
  

