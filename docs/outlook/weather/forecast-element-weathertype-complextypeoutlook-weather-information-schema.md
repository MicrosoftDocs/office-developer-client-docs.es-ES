---
title: previsión de elemento (weatherType complexType) (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.'
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821228"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="edcba-103">previsión de elemento (weatherType complexType) (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="edcba-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="edcba-104">Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.</span><span class="sxs-lookup"><span data-stu-id="edcba-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="edcba-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="edcba-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="edcba-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="edcba-106">**Element type**</span></span> <br/> |[<span data-ttu-id="edcba-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="edcba-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="edcba-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="edcba-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="edcba-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="edcba-109">**Schema file**</span></span> <br/> |<span data-ttu-id="edcba-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="edcba-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="edcba-111">Definición</span><span class="sxs-lookup"><span data-stu-id="edcba-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="edcba-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="edcba-112">Elements and attributes</span></span>

<span data-ttu-id="edcba-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="edcba-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="edcba-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="edcba-114">Parent elements</span></span>

|<span data-ttu-id="edcba-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="edcba-115">**Element**</span></span>|<span data-ttu-id="edcba-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="edcba-116">**Type**</span></span>|<span data-ttu-id="edcba-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edcba-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="edcba-118">meteorología</span><span class="sxs-lookup"><span data-stu-id="edcba-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="edcba-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="edcba-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="edcba-120">Especifica las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="edcba-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="edcba-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="edcba-121">Child elements</span></span>

<span data-ttu-id="edcba-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="edcba-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="edcba-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="edcba-123">Attributes</span></span>

|<span data-ttu-id="edcba-124">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="edcba-124">**Attribute**</span></span>|<span data-ttu-id="edcba-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="edcba-125">**Type**</span></span>|<span data-ttu-id="edcba-126">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="edcba-126">**Required**</span></span>|<span data-ttu-id="edcba-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edcba-127">**Description**</span></span>|<span data-ttu-id="edcba-128">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="edcba-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="edcba-129">date</span><span class="sxs-lookup"><span data-stu-id="edcba-129">date</span></span>  <br/> |<span data-ttu-id="edcba-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="edcba-130">xs:date</span></span>  <br/> |<span data-ttu-id="edcba-131">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-131">required</span></span>  <br/> |<span data-ttu-id="edcba-132">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="edcba-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="edcba-133">Un valor de tipo de xs: Date</span><span class="sxs-lookup"><span data-stu-id="edcba-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="edcba-134">día</span><span class="sxs-lookup"><span data-stu-id="edcba-134">day</span></span>  <br/> |<span data-ttu-id="edcba-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="edcba-135">xs:string</span></span>  <br/> |<span data-ttu-id="edcba-136">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-136">required</span></span>  <br/> |<span data-ttu-id="edcba-137">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="edcba-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="edcba-138">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="edcba-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="edcba-139">alta</span><span class="sxs-lookup"><span data-stu-id="edcba-139">high</span></span>  <br/> |<span data-ttu-id="edcba-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="edcba-140">xs:integer</span></span>  <br/> |<span data-ttu-id="edcba-141">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-141">required</span></span>  <br/> |<span data-ttu-id="edcba-142">Especifica la temperatura máxima prevista.</span><span class="sxs-lookup"><span data-stu-id="edcba-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="edcba-143">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="edcba-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="edcba-144">baja</span><span class="sxs-lookup"><span data-stu-id="edcba-144">low</span></span>  <br/> |<span data-ttu-id="edcba-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="edcba-145">xs:integer</span></span>  <br/> |<span data-ttu-id="edcba-146">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-146">required</span></span>  <br/> |<span data-ttu-id="edcba-147">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="edcba-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="edcba-148">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="edcba-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="edcba-149">precip</span><span class="sxs-lookup"><span data-stu-id="edcba-149">precip</span></span>  <br/> |<span data-ttu-id="edcba-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="edcba-150">xs:integer</span></span>  <br/> |<span data-ttu-id="edcba-151">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-151">required</span></span>  <br/> |<span data-ttu-id="edcba-152">Especifica la posibilidad de porcentaje de precipitación.</span><span class="sxs-lookup"><span data-stu-id="edcba-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="edcba-153">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="edcba-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="edcba-154">shortday</span><span class="sxs-lookup"><span data-stu-id="edcba-154">shortday</span></span>  <br/> |<span data-ttu-id="edcba-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="edcba-155">xs:string</span></span>  <br/> |<span data-ttu-id="edcba-156">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-156">required</span></span>  <br/> |<span data-ttu-id="edcba-157">Especifica un día de forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="edcba-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="edcba-158">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="edcba-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="edcba-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="edcba-159">skycodeday</span></span>  <br/> |<span data-ttu-id="edcba-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="edcba-160">xs:integer</span></span>  <br/> |<span data-ttu-id="edcba-161">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-161">required</span></span>  <br/> |<span data-ttu-id="edcba-162">Especifica un código de las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="edcba-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="edcba-163">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="edcba-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="edcba-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="edcba-164">skytextday</span></span>  <br/> |<span data-ttu-id="edcba-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="edcba-165">xs:string</span></span>  <br/> |<span data-ttu-id="edcba-166">necesario</span><span class="sxs-lookup"><span data-stu-id="edcba-166">required</span></span>  <br/> |<span data-ttu-id="edcba-167">Especifica una o dos palabras que describen las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="edcba-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="edcba-168">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="edcba-168">A value of the type xs:string</span></span>  <br/> |
   

