---
title: elemento Weather (elemento datos) (esquema de ubicación de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica la ubicación en la que se va a notificar el tiempo.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539015"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="7162e-103">elemento Weather (elemento datos) (esquema de ubicación de tiempo de Outlook)</span><span class="sxs-lookup"><span data-stu-id="7162e-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="7162e-104">Especifica la ubicación en la que se va a notificar el tiempo.</span><span class="sxs-lookup"><span data-stu-id="7162e-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7162e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7162e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7162e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7162e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7162e-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="7162e-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="7162e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7162e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="7162e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7162e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7162e-110">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="7162e-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7162e-111">Definición</span><span class="sxs-lookup"><span data-stu-id="7162e-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="7162e-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7162e-112">Elements and attributes</span></span>

<span data-ttu-id="7162e-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7162e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7162e-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7162e-114">Parent elements</span></span>

|<span data-ttu-id="7162e-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7162e-115">**Element**</span></span>|<span data-ttu-id="7162e-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7162e-116">**Type**</span></span>|<span data-ttu-id="7162e-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7162e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7162e-118">datos</span><span class="sxs-lookup"><span data-stu-id="7162e-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="7162e-119">Define el elemento Weather.</span><span class="sxs-lookup"><span data-stu-id="7162e-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7162e-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7162e-120">Child elements</span></span>

<span data-ttu-id="7162e-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7162e-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7162e-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="7162e-122">Attributes</span></span>

|<span data-ttu-id="7162e-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7162e-123">**Attribute**</span></span>|<span data-ttu-id="7162e-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7162e-124">**Type**</span></span>|<span data-ttu-id="7162e-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7162e-125">**Required**</span></span>|<span data-ttu-id="7162e-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7162e-126">**Description**</span></span>|<span data-ttu-id="7162e-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7162e-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7162e-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="7162e-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="7162e-129">XS: String</span><span class="sxs-lookup"><span data-stu-id="7162e-129">xs:string</span></span>  <br/> |<span data-ttu-id="7162e-130">necesario</span><span class="sxs-lookup"><span data-stu-id="7162e-130">required</span></span>  <br/> |<span data-ttu-id="7162e-131">Especifica un código que está asociado con la ubicación para distinguir varias ubicaciones con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="7162e-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="7162e-132">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7162e-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7162e-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="7162e-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="7162e-134">XS: String</span><span class="sxs-lookup"><span data-stu-id="7162e-134">xs:string</span></span>  <br/> |<span data-ttu-id="7162e-135">necesario</span><span class="sxs-lookup"><span data-stu-id="7162e-135">required</span></span>  <br/> |<span data-ttu-id="7162e-136">Especifica el nombre de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="7162e-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="7162e-137">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7162e-137">A value of the type xs:string</span></span>  <br/> |
   

