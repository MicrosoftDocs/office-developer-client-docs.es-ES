---
title: Elemento de PublishedPage (PublishSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Especifica si una página de dibujo está visible en el explorador con los servicios de Visio en Microsoft SharePoint Server 2013.
ms.openlocfilehash: 5cdbb03aaac3393c16c6ed0169842153374f668e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822882"
---
# <a name="publishedpage-element-publishsettingstype-complextype-visio-xml"></a><span data-ttu-id="4677e-103">Elemento de PublishedPage (PublishSettings_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="4677e-103">PublishedPage element (PublishSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4677e-104">Especifica si una página de dibujo está visible en el explorador con los servicios de Visio en Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4677e-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4677e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4677e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4677e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4677e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4677e-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="4677e-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4677e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4677e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4677e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4677e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4677e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4677e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4677e-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="4677e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4677e-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="4677e-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4677e-113">Definición</span><span class="sxs-lookup"><span data-stu-id="4677e-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4677e-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4677e-114">Elements and attributes</span></span>

<span data-ttu-id="4677e-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="4677e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4677e-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4677e-116">Parent elements</span></span>

|<span data-ttu-id="4677e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4677e-117">**Element**</span></span>|<span data-ttu-id="4677e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4677e-118">**Type**</span></span>|<span data-ttu-id="4677e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4677e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4677e-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="4677e-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4677e-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4677e-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4677e-122">Especifica la configuración que se usa cuando se abre el diagrama mediante servicios de Visio.</span><span class="sxs-lookup"><span data-stu-id="4677e-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4677e-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4677e-123">Child elements</span></span>

<span data-ttu-id="4677e-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4677e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4677e-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="4677e-125">Attributes</span></span>

|<span data-ttu-id="4677e-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4677e-126">**Attribute**</span></span>|<span data-ttu-id="4677e-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4677e-127">**Type**</span></span>|<span data-ttu-id="4677e-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4677e-128">**Required**</span></span>|<span data-ttu-id="4677e-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4677e-129">**Description**</span></span>|<span data-ttu-id="4677e-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="4677e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4677e-131">ID</span><span class="sxs-lookup"><span data-stu-id="4677e-131">ID</span></span>  <br/> |<span data-ttu-id="4677e-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4677e-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4677e-133">necesario</span><span class="sxs-lookup"><span data-stu-id="4677e-133">required</span></span>  <br/> |<span data-ttu-id="4677e-134">El identificador de una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="4677e-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="4677e-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4677e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

