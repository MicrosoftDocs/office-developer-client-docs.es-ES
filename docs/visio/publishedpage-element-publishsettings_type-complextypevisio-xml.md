---
title: Elemento PublishedPage (PublishSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c1eca66b-5840-790a-459f-e06680d11c05
description: Especifica si una página de dibujo se puede ver en el explorador mediante Visio services en Microsoft SharePoint Server 2013.
ms.openlocfilehash: 614c01f12b9a7525620704e5417a106e8703c983
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538378"
---
# <a name="publishedpage-element-publishsettings_type-complextype-visio-xml"></a><span data-ttu-id="4c544-103">Elemento PublishedPage (PublishSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4c544-103">PublishedPage element (PublishSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4c544-104">Especifica si una página de dibujo se puede ver en el explorador mediante Visio services en Microsoft SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4c544-104">Specifies whether a drawing page is viewable in the browser using Visio Services in Microsoft SharePoint Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c544-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c544-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c544-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4c544-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4c544-107">PublishedPage_Type</span><span class="sxs-lookup"><span data-stu-id="4c544-107">PublishedPage_Type</span></span>](publishedpage_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4c544-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4c544-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4c544-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4c544-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4c544-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4c544-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4c544-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="4c544-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4c544-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="4c544-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c544-113">Definición</span><span class="sxs-lookup"><span data-stu-id="4c544-113">Definition</span></span>

```XML
< xs:element name="PublishedPage" type="PublishedPage_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c544-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4c544-114">Elements and attributes</span></span>

<span data-ttu-id="4c544-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="4c544-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4c544-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c544-116">Parent elements</span></span>

|<span data-ttu-id="4c544-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c544-117">**Element**</span></span>|<span data-ttu-id="4c544-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4c544-118">**Type**</span></span>|<span data-ttu-id="4c544-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c544-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c544-120">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="4c544-120">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c544-121">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="4c544-121">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4c544-122">Especifica la configuración que se usa cuando se abre el diagrama mediante Visio Services.</span><span class="sxs-lookup"><span data-stu-id="4c544-122">Specifies the settings that are used when the diagram is opened using Visio Services.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4c544-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c544-123">Child elements</span></span>

<span data-ttu-id="4c544-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c544-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c544-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c544-125">Attributes</span></span>

|<span data-ttu-id="4c544-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4c544-126">**Attribute**</span></span>|<span data-ttu-id="4c544-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4c544-127">**Type**</span></span>|<span data-ttu-id="4c544-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4c544-128">**Required**</span></span>|<span data-ttu-id="4c544-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c544-129">**Description**</span></span>|<span data-ttu-id="4c544-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="4c544-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4c544-131">ID</span><span class="sxs-lookup"><span data-stu-id="4c544-131">ID</span></span>  <br/> |<span data-ttu-id="4c544-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4c544-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4c544-133">necesario</span><span class="sxs-lookup"><span data-stu-id="4c544-133">required</span></span>  <br/> |<span data-ttu-id="4c544-134">Identificador de una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="4c544-134">The identifier of a drawing page.</span></span>  <br/> |<span data-ttu-id="4c544-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4c544-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

