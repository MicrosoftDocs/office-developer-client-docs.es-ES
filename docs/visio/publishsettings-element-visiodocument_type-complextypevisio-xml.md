---
title: Elemento de PublishSettings (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Especifica la configuración que se usa cuando se abre el diagrama con los servicios de Visio en Microsoft SharePoint Server 2013.
ms.openlocfilehash: f2554facc47de23104f65b26ae19cfc71821bd37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822885"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="42e0b-103">Elemento de PublishSettings (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="42e0b-103">PublishSettings element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="42e0b-104">Especifica la configuración que se usa cuando se abre el diagrama con los servicios de Visio en Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="42e0b-104">Specifies the settings that are used when the diagram is opened using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42e0b-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="42e0b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42e0b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="42e0b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="42e0b-107">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="42e0b-107">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="42e0b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="42e0b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="42e0b-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="42e0b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="42e0b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="42e0b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="42e0b-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="42e0b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="42e0b-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="42e0b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="42e0b-113">Definición</span><span class="sxs-lookup"><span data-stu-id="42e0b-113">Definition</span></span>

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="42e0b-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="42e0b-114">Elements and attributes</span></span>

<span data-ttu-id="42e0b-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="42e0b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="42e0b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="42e0b-116">Parent elements</span></span>

|<span data-ttu-id="42e0b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="42e0b-117">**Element**</span></span>|<span data-ttu-id="42e0b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="42e0b-118">**Type**</span></span>|<span data-ttu-id="42e0b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42e0b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="42e0b-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="42e0b-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="42e0b-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="42e0b-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="42e0b-122">Especifica las propiedades de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="42e0b-122">Specifies properties of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="42e0b-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="42e0b-123">Child elements</span></span>

|<span data-ttu-id="42e0b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="42e0b-124">**Element**</span></span>|<span data-ttu-id="42e0b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="42e0b-125">**Type**</span></span>|<span data-ttu-id="42e0b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42e0b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="42e0b-127">PublishedPage</span><span class="sxs-lookup"><span data-stu-id="42e0b-127">PublishedPage</span></span>](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="42e0b-128">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="42e0b-128">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="42e0b-129">Especifica si una página de dibujo está visible en el explorador con los servicios de Visio.</span><span class="sxs-lookup"><span data-stu-id="42e0b-129">Specifies whether a drawing page is viewable in the browser using Visio Services.</span></span>  <br/> |
|[<span data-ttu-id="42e0b-130">RefreshableData</span><span class="sxs-lookup"><span data-stu-id="42e0b-130">RefreshableData</span></span>](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="42e0b-131">RefreshableData_Type</span><span class="sxs-lookup"><span data-stu-id="42e0b-131">RefreshableData_Type</span></span>](refreshabledata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="42e0b-132">Especifica si un conjunto de registros es actualizable mediante servicios de Visio.</span><span class="sxs-lookup"><span data-stu-id="42e0b-132">Specifies whether a recordset is refreshable using Visio Services.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="42e0b-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="42e0b-133">Attributes</span></span>

<span data-ttu-id="42e0b-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42e0b-134">None.</span></span>
  

