---
title: fld_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 2b1ecb21090658e1d2b042ac0f7e394d929d43c1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390607"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="66c32-102">fld_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="66c32-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="66c32-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="66c32-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66c32-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="66c32-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="66c32-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="66c32-105">**Schema file**</span></span> <br/> |<span data-ttu-id="66c32-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="66c32-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="66c32-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="66c32-107">**Extension base**</span></span> <br/> |<span data-ttu-id="66c32-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="66c32-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66c32-109">Definición</span><span class="sxs-lookup"><span data-stu-id="66c32-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66c32-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="66c32-110">Elements and attributes</span></span>

<span data-ttu-id="66c32-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="66c32-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="66c32-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66c32-112">Child elements</span></span>

<span data-ttu-id="66c32-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="66c32-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66c32-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="66c32-114">Attributes</span></span>

|<span data-ttu-id="66c32-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="66c32-115">**Attribute**</span></span>|<span data-ttu-id="66c32-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="66c32-116">**Type**</span></span>|<span data-ttu-id="66c32-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="66c32-117">**Required**</span></span>|<span data-ttu-id="66c32-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66c32-118">**Description**</span></span>|<span data-ttu-id="66c32-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="66c32-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66c32-120">IX</span><span class="sxs-lookup"><span data-stu-id="66c32-120">IX</span></span>  <br/> |<span data-ttu-id="66c32-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="66c32-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="66c32-122">necesario</span><span class="sxs-lookup"><span data-stu-id="66c32-122">required</span></span>  <br/> ||<span data-ttu-id="66c32-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="66c32-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

