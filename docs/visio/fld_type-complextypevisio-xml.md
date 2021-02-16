---
title: fld_Type complexType (VISIO XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 5651a0b0a2d09e3fbbdb0d1dbf66f1be3d374c12
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539603"
---
# <a name="fld_type-complextype-visio-xml"></a><span data-ttu-id="1016a-102">fld_Type complexType (VISIO XML)</span><span class="sxs-lookup"><span data-stu-id="1016a-102">fld_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1016a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="1016a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1016a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1016a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1016a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1016a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1016a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1016a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1016a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="1016a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1016a-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1016a-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1016a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="1016a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1016a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1016a-110">Elements and attributes</span></span>

<span data-ttu-id="1016a-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1016a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1016a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1016a-112">Child elements</span></span>

<span data-ttu-id="1016a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1016a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1016a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="1016a-114">Attributes</span></span>

|<span data-ttu-id="1016a-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1016a-115">**Attribute**</span></span>|<span data-ttu-id="1016a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1016a-116">**Type**</span></span>|<span data-ttu-id="1016a-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1016a-117">**Required**</span></span>|<span data-ttu-id="1016a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1016a-118">**Description**</span></span>|<span data-ttu-id="1016a-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1016a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1016a-120">IX</span><span class="sxs-lookup"><span data-stu-id="1016a-120">IX</span></span>  <br/> |<span data-ttu-id="1016a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1016a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1016a-122">necesario</span><span class="sxs-lookup"><span data-stu-id="1016a-122">required</span></span>  <br/> ||<span data-ttu-id="1016a-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1016a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

