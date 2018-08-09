---
title: meteorología elemento (weatherdata) (esquema de ubicación de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica la ubicación de meteorología de informe en.
ms.openlocfilehash: a95e207845a9e54f5cac58b64ce85ec17b59fa22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821303"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="cc838-103">meteorología elemento (weatherdata) (esquema de ubicación de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="cc838-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="cc838-104">Especifica la ubicación de meteorología de informe en.</span><span class="sxs-lookup"><span data-stu-id="cc838-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc838-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc838-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc838-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cc838-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc838-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="cc838-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="cc838-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc838-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="cc838-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc838-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc838-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="cc838-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc838-111">Definición</span><span class="sxs-lookup"><span data-stu-id="cc838-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc838-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cc838-112">Elements and attributes</span></span>

<span data-ttu-id="cc838-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="cc838-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc838-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc838-114">Parent elements</span></span>

|<span data-ttu-id="cc838-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc838-115">**Element**</span></span>|<span data-ttu-id="cc838-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc838-116">**Type**</span></span>|<span data-ttu-id="cc838-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc838-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc838-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="cc838-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="cc838-119">Define el elemento de meteorología.</span><span class="sxs-lookup"><span data-stu-id="cc838-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cc838-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc838-120">Child elements</span></span>

<span data-ttu-id="cc838-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc838-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc838-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc838-122">Attributes</span></span>

|<span data-ttu-id="cc838-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="cc838-123">**Attribute**</span></span>|<span data-ttu-id="cc838-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc838-124">**Type**</span></span>|<span data-ttu-id="cc838-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cc838-125">**Required**</span></span>|<span data-ttu-id="cc838-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc838-126">**Description**</span></span>|<span data-ttu-id="cc838-127">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="cc838-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc838-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="cc838-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="cc838-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc838-129">xs:string</span></span>  <br/> |<span data-ttu-id="cc838-130">necesario</span><span class="sxs-lookup"><span data-stu-id="cc838-130">required</span></span>  <br/> |<span data-ttu-id="cc838-131">Especifica un código que está asociado a la ubicación para distinguir varias ubicaciones con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="cc838-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="cc838-132">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="cc838-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cc838-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="cc838-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="cc838-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc838-134">xs:string</span></span>  <br/> |<span data-ttu-id="cc838-135">necesario</span><span class="sxs-lookup"><span data-stu-id="cc838-135">required</span></span>  <br/> |<span data-ttu-id="cc838-136">Especifica el nombre de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="cc838-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="cc838-137">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="cc838-137">A value of the type xs:string</span></span>  <br/> |
   

