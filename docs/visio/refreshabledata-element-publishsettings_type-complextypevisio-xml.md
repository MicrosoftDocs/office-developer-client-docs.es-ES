---
title: Elemento de RefreshableData (PublishSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9a3b9d5a-fcba-eb18-3199-bd5a7f889af8
description: Especifica si un conjunto de registros es actualizable mediante servicios de Visio en Microsoft SharePoint Server 2013.
ms.openlocfilehash: b402e2c9d65bf868c0ac33c782b87857ab6aed75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384877"
---
# <a name="refreshabledata-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="0428a-103">Elemento de RefreshableData (PublishSettings_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="0428a-103">RefreshableData element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0428a-104">Especifica si un conjunto de registros es actualizable mediante servicios de Visio en Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0428a-104">Specifies whether a recordset is refreshable using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0428a-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0428a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0428a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0428a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0428a-107">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="0428a-107">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0428a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0428a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0428a-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0428a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0428a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0428a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0428a-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="0428a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0428a-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="0428a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0428a-113">Definición</span><span class="sxs-lookup"><span data-stu-id="0428a-113">Definition</span></span>

```XML
<xs:element name="RefreshableData" type="RefreshableData_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >

```

## <a name="elements-and-attributes"></a><span data-ttu-id="0428a-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0428a-114">Elements and attributes</span></span>

<span data-ttu-id="0428a-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="0428a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0428a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0428a-116">Parent elements</span></span>

|<span data-ttu-id="0428a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0428a-117">**Element**</span></span>|<span data-ttu-id="0428a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0428a-118">**Type**</span></span>|<span data-ttu-id="0428a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0428a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0428a-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="0428a-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0428a-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="0428a-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0428a-122">Especifica la configuración que se usa cuando se abre el diagrama mediante servicios de Visio.</span><span class="sxs-lookup"><span data-stu-id="0428a-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0428a-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0428a-123">Child elements</span></span>

<span data-ttu-id="0428a-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0428a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0428a-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="0428a-125">Attributes</span></span>

|<span data-ttu-id="0428a-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0428a-126">**Attribute**</span></span>|<span data-ttu-id="0428a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0428a-127">**Type**</span></span>|<span data-ttu-id="0428a-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0428a-128">**Required**</span></span>|<span data-ttu-id="0428a-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0428a-129">**Description**</span></span>|<span data-ttu-id="0428a-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="0428a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0428a-131">ID</span><span class="sxs-lookup"><span data-stu-id="0428a-131">ID</span></span>  <br/> |<span data-ttu-id="0428a-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0428a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0428a-133">necesario</span><span class="sxs-lookup"><span data-stu-id="0428a-133">required</span></span>  <br/> |<span data-ttu-id="0428a-134">El identificador de un objeto recordset.</span><span class="sxs-lookup"><span data-stu-id="0428a-134">The identifier of a recordset.</span></span>  <br/> |<span data-ttu-id="0428a-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0428a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

