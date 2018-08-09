---
title: HeaderMargin_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 70b16680446af8973605d24f41b69778a1ec2c2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822279"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="f8c0a-102">HeaderMargin_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f8c0a-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f8c0a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f8c0a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8c0a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f8c0a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f8c0a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f8c0a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f8c0a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f8c0a-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="f8c0a-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f8c0a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f8c0a-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f8c0a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f8c0a-110">Elements and attributes</span></span>

<span data-ttu-id="f8c0a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f8c0a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8c0a-112">Child elements</span></span>

<span data-ttu-id="f8c0a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8c0a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f8c0a-114">Attributes</span></span>

|<span data-ttu-id="f8c0a-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-115">**Attribute**</span></span>|<span data-ttu-id="f8c0a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-116">**Type**</span></span>|<span data-ttu-id="f8c0a-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-117">**Required**</span></span>|<span data-ttu-id="f8c0a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-118">**Description**</span></span>|<span data-ttu-id="f8c0a-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="f8c0a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f8c0a-120">Unidad</span><span class="sxs-lookup"><span data-stu-id="f8c0a-120">Unit</span></span>  <br/> |<span data-ttu-id="f8c0a-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f8c0a-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f8c0a-122">opcional</span><span class="sxs-lookup"><span data-stu-id="f8c0a-122">optional</span></span>  <br/> ||<span data-ttu-id="f8c0a-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-123">Values of the xsd:string type.</span></span>  <br/> |
   

