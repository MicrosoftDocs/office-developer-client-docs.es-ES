---
title: FooterMargin_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f2cfa7c9d27940308c95318f8a743a4bdd6cb45f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822192"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="a005e-102">FooterMargin_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a005e-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a005e-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a005e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a005e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a005e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a005e-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a005e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a005e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a005e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a005e-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a005e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a005e-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="a005e-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a005e-109">Definición</span><span class="sxs-lookup"><span data-stu-id="a005e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a005e-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a005e-110">Elements and attributes</span></span>

<span data-ttu-id="a005e-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a005e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a005e-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a005e-112">Child elements</span></span>

<span data-ttu-id="a005e-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a005e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a005e-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="a005e-114">Attributes</span></span>

|<span data-ttu-id="a005e-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a005e-115">**Attribute**</span></span>|<span data-ttu-id="a005e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a005e-116">**Type**</span></span>|<span data-ttu-id="a005e-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a005e-117">**Required**</span></span>|<span data-ttu-id="a005e-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a005e-118">**Description**</span></span>|<span data-ttu-id="a005e-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="a005e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a005e-120">Unidad</span><span class="sxs-lookup"><span data-stu-id="a005e-120">Unit</span></span>  <br/> |<span data-ttu-id="a005e-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a005e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a005e-122">opcional</span><span class="sxs-lookup"><span data-stu-id="a005e-122">optional</span></span>  <br/> ||<span data-ttu-id="a005e-123">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="a005e-123">Values of the xsd:string type.</span></span>  <br/> |
   

