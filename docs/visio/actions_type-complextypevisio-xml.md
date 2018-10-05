---
title: Actions_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 158a0dfa31c2da3ac9e530c07edd075b4fabbd75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389564"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="0d0d6-102">Actions_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0d0d6-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0d0d6-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0d0d6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d0d6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d0d6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d0d6-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0d0d6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d0d6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0d0d6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d0d6-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0d0d6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d0d6-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0d0d6-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d0d6-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0d0d6-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d0d6-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0d0d6-110">Elements and attributes</span></span>

<span data-ttu-id="0d0d6-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0d0d6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d0d6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d0d6-112">Child elements</span></span>

|<span data-ttu-id="0d0d6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d0d6-113">**Element**</span></span>|<span data-ttu-id="0d0d6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0d0d6-114">**Type**</span></span>|<span data-ttu-id="0d0d6-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d0d6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d0d6-116">Row</span><span class="sxs-lookup"><span data-stu-id="0d0d6-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0d0d6-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="0d0d6-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0d0d6-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d0d6-118">Attributes</span></span>

<span data-ttu-id="0d0d6-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d0d6-119">None.</span></span>
  

