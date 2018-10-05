---
title: Elemento DataConnections ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contiene los elementos de DataConnection para el documento.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395031"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="2cdc2-103">Elemento DataConnections ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="2cdc2-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="2cdc2-104">Contiene los elementos de **DataConnection** para el documento.</span><span class="sxs-lookup"><span data-stu-id="2cdc2-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2cdc2-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2cdc2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cdc2-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2cdc2-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="2cdc2-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2cdc2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2cdc2-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2cdc2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2cdc2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2cdc2-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2cdc2-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="2cdc2-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2cdc2-113">Definición</span><span class="sxs-lookup"><span data-stu-id="2cdc2-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2cdc2-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2cdc2-114">Elements and attributes</span></span>

<span data-ttu-id="2cdc2-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="2cdc2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2cdc2-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2cdc2-116">Parent elements</span></span>

<span data-ttu-id="2cdc2-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2cdc2-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2cdc2-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2cdc2-118">Child elements</span></span>

|<span data-ttu-id="2cdc2-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-119">**Element**</span></span>|<span data-ttu-id="2cdc2-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-120">**Type**</span></span>|<span data-ttu-id="2cdc2-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2cdc2-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="2cdc2-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2cdc2-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="2cdc2-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2cdc2-124">Resume la comunicación entre uno o varios elementos de **DataRecordset** y un origen de datos no XML.</span><span class="sxs-lookup"><span data-stu-id="2cdc2-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2cdc2-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="2cdc2-125">Attributes</span></span>

|<span data-ttu-id="2cdc2-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-126">**Attribute**</span></span>|<span data-ttu-id="2cdc2-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-127">**Type**</span></span>|<span data-ttu-id="2cdc2-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-128">**Required**</span></span>|<span data-ttu-id="2cdc2-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-129">**Description**</span></span>|<span data-ttu-id="2cdc2-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="2cdc2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2cdc2-131">NextID</span><span class="sxs-lookup"><span data-stu-id="2cdc2-131">NextID</span></span>  <br/> |<span data-ttu-id="2cdc2-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2cdc2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2cdc2-133">necesario</span><span class="sxs-lookup"><span data-stu-id="2cdc2-133">required</span></span>  <br/> |<span data-ttu-id="2cdc2-134">El siguiente identificador disponible para nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="2cdc2-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="2cdc2-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2cdc2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

