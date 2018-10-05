---
title: DataConnections_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 2bbea48e1d5340c5a68bbafbef9a900a98357385
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397390"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="89e44-102">DataConnections_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="89e44-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="89e44-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="89e44-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89e44-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="89e44-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="89e44-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="89e44-105">**Schema file**</span></span> <br/> |<span data-ttu-id="89e44-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="89e44-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="89e44-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="89e44-107">**Extension base**</span></span> <br/> |<span data-ttu-id="89e44-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="89e44-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="89e44-109">Definición</span><span class="sxs-lookup"><span data-stu-id="89e44-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="89e44-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="89e44-110">Elements and attributes</span></span>

<span data-ttu-id="89e44-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="89e44-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="89e44-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89e44-112">Child elements</span></span>

|<span data-ttu-id="89e44-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="89e44-113">**Element**</span></span>|<span data-ttu-id="89e44-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="89e44-114">**Type**</span></span>|<span data-ttu-id="89e44-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89e44-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="89e44-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="89e44-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="89e44-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="89e44-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="89e44-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="89e44-118">Attributes</span></span>

|<span data-ttu-id="89e44-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="89e44-119">**Attribute**</span></span>|<span data-ttu-id="89e44-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="89e44-120">**Type**</span></span>|<span data-ttu-id="89e44-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="89e44-121">**Required**</span></span>|<span data-ttu-id="89e44-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89e44-122">**Description**</span></span>|<span data-ttu-id="89e44-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="89e44-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="89e44-124">NextID</span><span class="sxs-lookup"><span data-stu-id="89e44-124">NextID</span></span>  <br/> |<span data-ttu-id="89e44-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="89e44-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="89e44-126">necesario</span><span class="sxs-lookup"><span data-stu-id="89e44-126">required</span></span>  <br/> ||<span data-ttu-id="89e44-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="89e44-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

