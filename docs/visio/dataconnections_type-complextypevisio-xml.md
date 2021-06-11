---
title: DataConnections_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 712632a74b0ffad6d0c9ca8745d67018518d87de
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542460"
---
# <a name="dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="c8f5d-102">DataConnections_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c8f5d-102">DataConnections_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c8f5d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="c8f5d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8f5d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c8f5d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c8f5d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c8f5d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c8f5d-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c8f5d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c8f5d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8f5d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c8f5d-109">Definition</span></span>

```XML
          <xs:complexType name="DataConnections_Type">
          
          <xs:sequence>
    <xs:element name="DataConnection"  type="DataConnection_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c8f5d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c8f5d-110">Elements and attributes</span></span>

<span data-ttu-id="c8f5d-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c8f5d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c8f5d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8f5d-112">Child elements</span></span>

|<span data-ttu-id="c8f5d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-113">**Element**</span></span>|<span data-ttu-id="c8f5d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-114">**Type**</span></span>|<span data-ttu-id="c8f5d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8f5d-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="c8f5d-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8f5d-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="c8f5d-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c8f5d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8f5d-118">Attributes</span></span>

|<span data-ttu-id="c8f5d-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-119">**Attribute**</span></span>|<span data-ttu-id="c8f5d-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-120">**Type**</span></span>|<span data-ttu-id="c8f5d-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-121">**Required**</span></span>|<span data-ttu-id="c8f5d-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-122">**Description**</span></span>|<span data-ttu-id="c8f5d-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c8f5d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c8f5d-124">NextID</span><span class="sxs-lookup"><span data-stu-id="c8f5d-124">NextID</span></span>  <br/> |<span data-ttu-id="c8f5d-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c8f5d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c8f5d-126">necesario</span><span class="sxs-lookup"><span data-stu-id="c8f5d-126">required</span></span>  <br/> ||<span data-ttu-id="c8f5d-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c8f5d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

