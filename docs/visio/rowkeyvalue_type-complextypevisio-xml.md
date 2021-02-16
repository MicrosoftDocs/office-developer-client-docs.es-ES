---
title: RowKeyValue_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: e629a3a38927b7497d8d4f50299dc6be1b51c37b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541725"
---
# <a name="rowkeyvalue_type-complextype-visio-xml"></a><span data-ttu-id="9587c-102">RowKeyValue_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9587c-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9587c-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="9587c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9587c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9587c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9587c-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9587c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9587c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9587c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9587c-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="9587c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9587c-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9587c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9587c-109">Definición</span><span class="sxs-lookup"><span data-stu-id="9587c-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9587c-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9587c-110">Elements and attributes</span></span>

<span data-ttu-id="9587c-111">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9587c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9587c-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9587c-112">Child elements</span></span>

<span data-ttu-id="9587c-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9587c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9587c-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="9587c-114">Attributes</span></span>

|<span data-ttu-id="9587c-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9587c-115">**Attribute**</span></span>|<span data-ttu-id="9587c-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9587c-116">**Type**</span></span>|<span data-ttu-id="9587c-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9587c-117">**Required**</span></span>|<span data-ttu-id="9587c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9587c-118">**Description**</span></span>|<span data-ttu-id="9587c-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9587c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9587c-120">RowID</span><span class="sxs-lookup"><span data-stu-id="9587c-120">RowID</span></span>  <br/> |<span data-ttu-id="9587c-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9587c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9587c-122">necesario</span><span class="sxs-lookup"><span data-stu-id="9587c-122">required</span></span>  <br/> ||<span data-ttu-id="9587c-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9587c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9587c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9587c-124">Value</span></span>  <br/> |<span data-ttu-id="9587c-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9587c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9587c-126">necesario</span><span class="sxs-lookup"><span data-stu-id="9587c-126">required</span></span>  <br/> ||<span data-ttu-id="9587c-127">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9587c-127">Values of the xsd:string type.</span></span>  <br/> |
   

