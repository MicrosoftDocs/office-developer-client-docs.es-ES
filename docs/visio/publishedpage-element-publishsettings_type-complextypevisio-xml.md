---
title: Elemento de PublishedPage (PublishSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Especifica si una página de dibujo está visible en el explorador con los servicios de Visio en Microsoft SharePoint Server 2013.
ms.openlocfilehash: 313cabbdd59930df67c807ee3c89df1a6e8c17a2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390985"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="e58bd-103">Elemento de PublishedPage (PublishSettings_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e58bd-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e58bd-104">Especifica si una página de dibujo está visible en el explorador con los servicios de Visio en Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e58bd-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e58bd-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e58bd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e58bd-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e58bd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e58bd-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="e58bd-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e58bd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e58bd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e58bd-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e58bd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e58bd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e58bd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e58bd-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e58bd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e58bd-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="e58bd-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e58bd-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e58bd-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e58bd-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e58bd-114">Elements and attributes</span></span>

<span data-ttu-id="e58bd-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e58bd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e58bd-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e58bd-116">Parent elements</span></span>

|<span data-ttu-id="e58bd-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e58bd-117">**Element**</span></span>|<span data-ttu-id="e58bd-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e58bd-118">**Type**</span></span>|<span data-ttu-id="e58bd-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e58bd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e58bd-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="e58bd-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e58bd-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e58bd-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e58bd-122">Especifica la configuración que se usa cuando se abre el diagrama mediante servicios de Visio.</span><span class="sxs-lookup"><span data-stu-id="e58bd-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e58bd-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e58bd-123">Child elements</span></span>

<span data-ttu-id="e58bd-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e58bd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e58bd-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="e58bd-125">Attributes</span></span>

|<span data-ttu-id="e58bd-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e58bd-126">**Attribute**</span></span>|<span data-ttu-id="e58bd-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e58bd-127">**Type**</span></span>|<span data-ttu-id="e58bd-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e58bd-128">**Required**</span></span>|<span data-ttu-id="e58bd-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e58bd-129">**Description**</span></span>|<span data-ttu-id="e58bd-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="e58bd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e58bd-131">ID</span><span class="sxs-lookup"><span data-stu-id="e58bd-131">ID</span></span>  <br/> |<span data-ttu-id="e58bd-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e58bd-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e58bd-133">necesario</span><span class="sxs-lookup"><span data-stu-id="e58bd-133">required</span></span>  <br/> |<span data-ttu-id="e58bd-134">El identificador de una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="e58bd-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="e58bd-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e58bd-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

