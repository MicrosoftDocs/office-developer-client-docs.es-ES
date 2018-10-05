---
title: FooterMargin_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398937"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="f31e0-102">FooterMargin_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f31e0-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f31e0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="f31e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f31e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f31e0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f31e0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f31e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f31e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f31e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f31e0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="f31e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f31e0-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="f31e0-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f31e0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="f31e0-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f31e0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f31e0-110">Elements and attributes</span></span>

<span data-ttu-id="f31e0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f31e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f31e0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f31e0-112">Child elements</span></span>

<span data-ttu-id="f31e0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f31e0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f31e0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f31e0-114">Attributes</span></span>

|<span data-ttu-id="f31e0-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f31e0-115">**Attribute**</span></span>|<span data-ttu-id="f31e0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f31e0-116">**Type**</span></span>|<span data-ttu-id="f31e0-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f31e0-117">**Required**</span></span>|<span data-ttu-id="f31e0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f31e0-118">**Description**</span></span>|<span data-ttu-id="f31e0-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="f31e0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f31e0-120">Unidad</span><span class="sxs-lookup"><span data-stu-id="f31e0-120">Unit</span></span>  <br/> |<span data-ttu-id="f31e0-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f31e0-121">xsd:string</span></span>  <br/> |<span data-ttu-id="f31e0-122">opcional</span><span class="sxs-lookup"><span data-stu-id="f31e0-122">optional</span></span>  <br/> ||<span data-ttu-id="f31e0-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="f31e0-123">Values of the xsd:string type.</span></span>  <br/> |
   

