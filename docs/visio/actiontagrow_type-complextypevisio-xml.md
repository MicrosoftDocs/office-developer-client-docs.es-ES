---
title: ActionTagRow_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d42c212-b068-84fa-e271-bbe1fae52a48
ms.openlocfilehash: 8caef77494efa99df8f681deb1268dfee95f03cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346560"
---
# <a name="actiontagrowtype-complextype-visio-xml"></a><span data-ttu-id="6211d-102">ActionTagRow_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="6211d-102">ActionTagRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6211d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="6211d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6211d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6211d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6211d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6211d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6211d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6211d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6211d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="6211d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6211d-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="6211d-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6211d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="6211d-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTagRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="6211d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6211d-110">Elements and attributes</span></span>

<span data-ttu-id="6211d-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6211d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6211d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6211d-112">Child elements</span></span>

|<span data-ttu-id="6211d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6211d-113">**Element**</span></span>|<span data-ttu-id="6211d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6211d-114">**Type**</span></span>|<span data-ttu-id="6211d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6211d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6211d-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6211d-116">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6211d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6211d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6211d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="6211d-118">Attributes</span></span>

<span data-ttu-id="6211d-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6211d-119">None.</span></span>
  

