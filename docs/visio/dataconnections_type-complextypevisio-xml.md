---
title: DataConnections_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 83a3c944-9582-bf80-ec2a-7a752da03cd3
ms.openlocfilehash: 57781566bd94a057faaae719d02b13154ad6de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821917"
---
# <a name="dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="807c1-102">DataConnections_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="807c1-102">DataConnections_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="807c1-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="807c1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="807c1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="807c1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="807c1-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="807c1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="807c1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="807c1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="807c1-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="807c1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="807c1-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="807c1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="807c1-109">Definición</span><span class="sxs-lookup"><span data-stu-id="807c1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="807c1-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="807c1-110">Elements and attributes</span></span>

<span data-ttu-id="807c1-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="807c1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="807c1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="807c1-112">Child elements</span></span>

|<span data-ttu-id="807c1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="807c1-113">**Element**</span></span>|<span data-ttu-id="807c1-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="807c1-114">**Type**</span></span>|<span data-ttu-id="807c1-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="807c1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="807c1-116">DataConnection</span><span class="sxs-lookup"><span data-stu-id="807c1-116">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="807c1-117">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="807c1-117">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="807c1-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="807c1-118">Attributes</span></span>

|<span data-ttu-id="807c1-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="807c1-119">**Attribute**</span></span>|<span data-ttu-id="807c1-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="807c1-120">**Type**</span></span>|<span data-ttu-id="807c1-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="807c1-121">**Required**</span></span>|<span data-ttu-id="807c1-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="807c1-122">**Description**</span></span>|<span data-ttu-id="807c1-123">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="807c1-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="807c1-124">NextID</span><span class="sxs-lookup"><span data-stu-id="807c1-124">NextID</span></span>  <br/> |<span data-ttu-id="807c1-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="807c1-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="807c1-126">necesario</span><span class="sxs-lookup"><span data-stu-id="807c1-126">required</span></span>  <br/> ||<span data-ttu-id="807c1-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="807c1-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

