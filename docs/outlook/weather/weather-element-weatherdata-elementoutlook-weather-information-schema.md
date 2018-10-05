---
title: meteorología elemento (weatherdata) (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica las condiciones del tiempo de una ubicación.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390663"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="9d8ac-103">meteorología elemento (weatherdata) (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="9d8ac-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="9d8ac-104">Especifica las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d8ac-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d8ac-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d8ac-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9d8ac-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="9d8ac-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="9d8ac-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="9d8ac-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9d8ac-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="9d8ac-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9d8ac-111">Definición</span><span class="sxs-lookup"><span data-stu-id="9d8ac-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="9d8ac-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9d8ac-112">Elements and attributes</span></span>

<span data-ttu-id="9d8ac-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9d8ac-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d8ac-114">Parent elements</span></span>

|<span data-ttu-id="9d8ac-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-115">**Element**</span></span>|<span data-ttu-id="9d8ac-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-116">**Type**</span></span>|<span data-ttu-id="9d8ac-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d8ac-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="9d8ac-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="9d8ac-119">Define el elemento de meteorología.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d8ac-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d8ac-120">Child elements</span></span>

|<span data-ttu-id="9d8ac-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-121">**Element**</span></span>|<span data-ttu-id="9d8ac-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-122">**Type**</span></span>|<span data-ttu-id="9d8ac-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9d8ac-124">actual</span><span class="sxs-lookup"><span data-stu-id="9d8ac-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="9d8ac-125">currentType</span><span class="sxs-lookup"><span data-stu-id="9d8ac-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="9d8ac-126">Especifica las condiciones del tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="9d8ac-127">previsión</span><span class="sxs-lookup"><span data-stu-id="9d8ac-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="9d8ac-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="9d8ac-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="9d8ac-129">Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9d8ac-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d8ac-130">Attributes</span></span>

|<span data-ttu-id="9d8ac-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-131">**Attribute**</span></span>|<span data-ttu-id="9d8ac-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-132">**Type**</span></span>|<span data-ttu-id="9d8ac-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-133">**Required**</span></span>|<span data-ttu-id="9d8ac-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-134">**Description**</span></span>|<span data-ttu-id="9d8ac-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="9d8ac-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9d8ac-136">atribución</span><span class="sxs-lookup"><span data-stu-id="9d8ac-136">attribution</span></span>  <br/> |<span data-ttu-id="9d8ac-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d8ac-137">xs:string</span></span>  <br/> |<span data-ttu-id="9d8ac-138">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-138">required</span></span>  <br/> |<span data-ttu-id="9d8ac-139">Especifica el origen de la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="9d8ac-140">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="9d8ac-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9d8ac-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="9d8ac-141">degreetype</span></span>  <br/> |<span data-ttu-id="9d8ac-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d8ac-142">xs:string</span></span>  <br/> |<span data-ttu-id="9d8ac-143">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-143">required</span></span>  <br/> |<span data-ttu-id="9d8ac-144">Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="9d8ac-145">C, F</span><span class="sxs-lookup"><span data-stu-id="9d8ac-145">C, F</span></span>  <br/> |
|<span data-ttu-id="9d8ac-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="9d8ac-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="9d8ac-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d8ac-147">xs:string</span></span>  <br/> |<span data-ttu-id="9d8ac-148">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-148">required</span></span>  <br/> |<span data-ttu-id="9d8ac-149">Especifica la dirección URL de la imagen de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="9d8ac-150">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="9d8ac-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9d8ac-151">zona horaria</span><span class="sxs-lookup"><span data-stu-id="9d8ac-151">timezone</span></span>  <br/> |<span data-ttu-id="9d8ac-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9d8ac-152">xs:integer</span></span>  <br/> |<span data-ttu-id="9d8ac-153">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-153">required</span></span>  <br/> |<span data-ttu-id="9d8ac-154">Especifica el desplazamiento de GMT.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="9d8ac-155">Un valor comprendido entre -11 y 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="9d8ac-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="9d8ac-156">url</span><span class="sxs-lookup"><span data-stu-id="9d8ac-156">url</span></span>  <br/> |<span data-ttu-id="9d8ac-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d8ac-157">xs:string</span></span>  <br/> |<span data-ttu-id="9d8ac-158">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-158">required</span></span>  <br/> |<span data-ttu-id="9d8ac-159">Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="9d8ac-160">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="9d8ac-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9d8ac-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="9d8ac-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="9d8ac-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d8ac-162">xs:string</span></span>  <br/> |<span data-ttu-id="9d8ac-163">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-163">required</span></span>  <br/> |<span data-ttu-id="9d8ac-164">Especifica el código que está asociado con la ubicación que se usa para distinguir múltiples ubicación que tienen el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="9d8ac-165">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="9d8ac-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9d8ac-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="9d8ac-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="9d8ac-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="9d8ac-167">xs:string</span></span>  <br/> |<span data-ttu-id="9d8ac-168">necesario</span><span class="sxs-lookup"><span data-stu-id="9d8ac-168">required</span></span>  <br/> |<span data-ttu-id="9d8ac-169">Especifica el nombre de la ubicación que aparece en el control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="9d8ac-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="9d8ac-170">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="9d8ac-170">A value of the type xs:string</span></span>  <br/> |
   

