---
title: FooterMargin_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346049"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="d3ade-102">FooterMargin_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d3ade-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d3ade-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d3ade-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3ade-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d3ade-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d3ade-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d3ade-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d3ade-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="d3ade-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d3ade-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d3ade-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d3ade-108">xsd: Double</span><span class="sxs-lookup"><span data-stu-id="d3ade-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d3ade-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d3ade-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d3ade-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d3ade-110">Elements and attributes</span></span>

<span data-ttu-id="d3ade-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d3ade-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d3ade-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d3ade-112">Child elements</span></span>

<span data-ttu-id="d3ade-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d3ade-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3ade-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3ade-114">Attributes</span></span>

|<span data-ttu-id="d3ade-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d3ade-115">**Attribute**</span></span>|<span data-ttu-id="d3ade-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d3ade-116">**Type**</span></span>|<span data-ttu-id="d3ade-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d3ade-117">**Required**</span></span>|<span data-ttu-id="d3ade-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d3ade-118">**Description**</span></span>|<span data-ttu-id="d3ade-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="d3ade-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d3ade-120">Unit</span><span class="sxs-lookup"><span data-stu-id="d3ade-120">Unit</span></span>  <br/> |<span data-ttu-id="d3ade-121">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d3ade-121">xsd:string</span></span>  <br/> |<span data-ttu-id="d3ade-122">opcional</span><span class="sxs-lookup"><span data-stu-id="d3ade-122">optional</span></span>  <br/> ||<span data-ttu-id="d3ade-123">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="d3ade-123">Values of the xsd:string type.</span></span>  <br/> |
   

