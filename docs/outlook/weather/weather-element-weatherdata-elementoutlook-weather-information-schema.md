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
ms.openlocfilehash: c19db6657860dd35f90832aef0614f4fb88d87b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821300"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="6c093-103">meteorología elemento (weatherdata) (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="6c093-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="6c093-104">Especifica las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="6c093-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c093-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6c093-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c093-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6c093-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6c093-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="6c093-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="6c093-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c093-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="6c093-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6c093-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6c093-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="6c093-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c093-111">Definición</span><span class="sxs-lookup"><span data-stu-id="6c093-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="6c093-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6c093-112">Elements and attributes</span></span>

<span data-ttu-id="6c093-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6c093-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6c093-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6c093-114">Parent elements</span></span>

|<span data-ttu-id="6c093-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c093-115">**Element**</span></span>|<span data-ttu-id="6c093-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6c093-116">**Type**</span></span>|<span data-ttu-id="6c093-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c093-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c093-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="6c093-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="6c093-119">Define el elemento de meteorología.</span><span class="sxs-lookup"><span data-stu-id="6c093-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6c093-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c093-120">Child elements</span></span>

|<span data-ttu-id="6c093-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="6c093-121">**Element**</span></span>|<span data-ttu-id="6c093-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6c093-122">**Type**</span></span>|<span data-ttu-id="6c093-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c093-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c093-124">actual</span><span class="sxs-lookup"><span data-stu-id="6c093-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="6c093-125">currentType</span><span class="sxs-lookup"><span data-stu-id="6c093-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="6c093-126">Especifica las condiciones del tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="6c093-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="6c093-127">previsión</span><span class="sxs-lookup"><span data-stu-id="6c093-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="6c093-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="6c093-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="6c093-129">Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.</span><span class="sxs-lookup"><span data-stu-id="6c093-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6c093-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6c093-130">Attributes</span></span>

|<span data-ttu-id="6c093-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6c093-131">**Attribute**</span></span>|<span data-ttu-id="6c093-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6c093-132">**Type**</span></span>|<span data-ttu-id="6c093-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6c093-133">**Required**</span></span>|<span data-ttu-id="6c093-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6c093-134">**Description**</span></span>|<span data-ttu-id="6c093-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="6c093-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c093-136">atribución</span><span class="sxs-lookup"><span data-stu-id="6c093-136">attribution</span></span>  <br/> |<span data-ttu-id="6c093-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c093-137">xs:string</span></span>  <br/> |<span data-ttu-id="6c093-138">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-138">required</span></span>  <br/> |<span data-ttu-id="6c093-139">Especifica el origen de la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="6c093-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="6c093-140">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="6c093-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6c093-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="6c093-141">degreetype</span></span>  <br/> |<span data-ttu-id="6c093-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c093-142">xs:string</span></span>  <br/> |<span data-ttu-id="6c093-143">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-143">required</span></span>  <br/> |<span data-ttu-id="6c093-144">Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="6c093-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="6c093-145">C, F</span><span class="sxs-lookup"><span data-stu-id="6c093-145">C, F</span></span>  <br/> |
|<span data-ttu-id="6c093-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="6c093-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="6c093-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c093-147">xs:string</span></span>  <br/> |<span data-ttu-id="6c093-148">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-148">required</span></span>  <br/> |<span data-ttu-id="6c093-149">Especifica la dirección URL de la imagen de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="6c093-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="6c093-150">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="6c093-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6c093-151">zona horaria</span><span class="sxs-lookup"><span data-stu-id="6c093-151">timezone</span></span>  <br/> |<span data-ttu-id="6c093-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6c093-152">xs:integer</span></span>  <br/> |<span data-ttu-id="6c093-153">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-153">required</span></span>  <br/> |<span data-ttu-id="6c093-154">Especifica el desplazamiento de GMT.</span><span class="sxs-lookup"><span data-stu-id="6c093-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="6c093-155">Un valor comprendido entre -11 y 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="6c093-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="6c093-156">url</span><span class="sxs-lookup"><span data-stu-id="6c093-156">url</span></span>  <br/> |<span data-ttu-id="6c093-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c093-157">xs:string</span></span>  <br/> |<span data-ttu-id="6c093-158">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-158">required</span></span>  <br/> |<span data-ttu-id="6c093-159">Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="6c093-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="6c093-160">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="6c093-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6c093-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="6c093-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="6c093-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c093-162">xs:string</span></span>  <br/> |<span data-ttu-id="6c093-163">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-163">required</span></span>  <br/> |<span data-ttu-id="6c093-164">Especifica el código que está asociado con la ubicación que se usa para distinguir múltiples ubicación que tienen el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="6c093-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="6c093-165">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="6c093-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6c093-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="6c093-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="6c093-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="6c093-167">xs:string</span></span>  <br/> |<span data-ttu-id="6c093-168">necesario</span><span class="sxs-lookup"><span data-stu-id="6c093-168">required</span></span>  <br/> |<span data-ttu-id="6c093-169">Especifica el nombre de la ubicación que aparece en el control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="6c093-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="6c093-170">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="6c093-170">A value of the type xs:string</span></span>  <br/> |
   

