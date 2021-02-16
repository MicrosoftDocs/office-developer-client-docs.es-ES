---
title: Elemento DataConnections (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contiene los elementos DataConnection del documento.
ms.openlocfilehash: 5d45d1dcd76524c2144336235e8277cd51f8a138
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539185"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="1baf8-103">Elemento DataConnections (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="1baf8-103">DataConnections element (Visio XML)</span></span>

<span data-ttu-id="1baf8-104">Contiene los **elementos DataConnection** del documento.</span><span class="sxs-lookup"><span data-stu-id="1baf8-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1baf8-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1baf8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1baf8-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1baf8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1baf8-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="1baf8-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1baf8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1baf8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1baf8-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1baf8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1baf8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1baf8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1baf8-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1baf8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1baf8-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="1baf8-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1baf8-113">Definición</span><span class="sxs-lookup"><span data-stu-id="1baf8-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1baf8-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1baf8-114">Elements and attributes</span></span>

<span data-ttu-id="1baf8-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1baf8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1baf8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1baf8-116">Parent elements</span></span>

<span data-ttu-id="1baf8-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1baf8-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1baf8-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1baf8-118">Child elements</span></span>

|<span data-ttu-id="1baf8-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1baf8-119">**Element**</span></span>|<span data-ttu-id="1baf8-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1baf8-120">**Type**</span></span>|<span data-ttu-id="1baf8-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1baf8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1baf8-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="1baf8-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1baf8-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="1baf8-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1baf8-124">Abstrae la comunicación entre uno o varios **elementos DataRecordset** y un origen de datos que no es XML.</span><span class="sxs-lookup"><span data-stu-id="1baf8-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1baf8-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1baf8-125">Attributes</span></span>

|<span data-ttu-id="1baf8-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="1baf8-126">**Attribute**</span></span>|<span data-ttu-id="1baf8-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1baf8-127">**Type**</span></span>|<span data-ttu-id="1baf8-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1baf8-128">**Required**</span></span>|<span data-ttu-id="1baf8-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1baf8-129">**Description**</span></span>|<span data-ttu-id="1baf8-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="1baf8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1baf8-131">NextID</span><span class="sxs-lookup"><span data-stu-id="1baf8-131">NextID</span></span>  <br/> |<span data-ttu-id="1baf8-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1baf8-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1baf8-133">necesario</span><span class="sxs-lookup"><span data-stu-id="1baf8-133">required</span></span>  <br/> |<span data-ttu-id="1baf8-134">El siguiente identificador disponible para las nuevas conexiones.</span><span class="sxs-lookup"><span data-stu-id="1baf8-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="1baf8-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1baf8-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

