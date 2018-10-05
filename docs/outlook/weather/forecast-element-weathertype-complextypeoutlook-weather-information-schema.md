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
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398328"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="33b48-103">previsión de elemento (weatherType complexType) (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="33b48-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="33b48-104">Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.</span><span class="sxs-lookup"><span data-stu-id="33b48-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33b48-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="33b48-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33b48-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="33b48-106">**Element type**</span></span> <br/> |[<span data-ttu-id="33b48-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="33b48-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="33b48-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="33b48-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="33b48-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="33b48-109">**Schema file**</span></span> <br/> |<span data-ttu-id="33b48-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="33b48-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="33b48-111">Definición</span><span class="sxs-lookup"><span data-stu-id="33b48-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="33b48-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="33b48-112">Elements and attributes</span></span>

<span data-ttu-id="33b48-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="33b48-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="33b48-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="33b48-114">Parent elements</span></span>

|<span data-ttu-id="33b48-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="33b48-115">**Element**</span></span>|<span data-ttu-id="33b48-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="33b48-116">**Type**</span></span>|<span data-ttu-id="33b48-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33b48-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="33b48-118">meteorología</span><span class="sxs-lookup"><span data-stu-id="33b48-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="33b48-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="33b48-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="33b48-120">Especifica las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="33b48-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="33b48-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="33b48-121">Child elements</span></span>

<span data-ttu-id="33b48-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="33b48-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33b48-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="33b48-123">Attributes</span></span>

|<span data-ttu-id="33b48-124">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="33b48-124">**Attribute**</span></span>|<span data-ttu-id="33b48-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="33b48-125">**Type**</span></span>|<span data-ttu-id="33b48-126">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="33b48-126">**Required**</span></span>|<span data-ttu-id="33b48-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33b48-127">**Description**</span></span>|<span data-ttu-id="33b48-128">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="33b48-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="33b48-129">date</span><span class="sxs-lookup"><span data-stu-id="33b48-129">date</span></span>  <br/> |<span data-ttu-id="33b48-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="33b48-130">xs:date</span></span>  <br/> |<span data-ttu-id="33b48-131">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-131">required</span></span>  <br/> |<span data-ttu-id="33b48-132">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="33b48-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="33b48-133">Un valor de tipo de xs: Date</span><span class="sxs-lookup"><span data-stu-id="33b48-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="33b48-134">día</span><span class="sxs-lookup"><span data-stu-id="33b48-134">day</span></span>  <br/> |<span data-ttu-id="33b48-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="33b48-135">xs:string</span></span>  <br/> |<span data-ttu-id="33b48-136">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-136">required</span></span>  <br/> |<span data-ttu-id="33b48-137">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="33b48-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="33b48-138">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="33b48-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="33b48-139">alta</span><span class="sxs-lookup"><span data-stu-id="33b48-139">high</span></span>  <br/> |<span data-ttu-id="33b48-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="33b48-140">xs:integer</span></span>  <br/> |<span data-ttu-id="33b48-141">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-141">required</span></span>  <br/> |<span data-ttu-id="33b48-142">Especifica la temperatura máxima prevista.</span><span class="sxs-lookup"><span data-stu-id="33b48-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="33b48-143">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="33b48-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="33b48-144">baja</span><span class="sxs-lookup"><span data-stu-id="33b48-144">low</span></span>  <br/> |<span data-ttu-id="33b48-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="33b48-145">xs:integer</span></span>  <br/> |<span data-ttu-id="33b48-146">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-146">required</span></span>  <br/> |<span data-ttu-id="33b48-147">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="33b48-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="33b48-148">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="33b48-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="33b48-149">precip</span><span class="sxs-lookup"><span data-stu-id="33b48-149">precip</span></span>  <br/> |<span data-ttu-id="33b48-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="33b48-150">xs:integer</span></span>  <br/> |<span data-ttu-id="33b48-151">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-151">required</span></span>  <br/> |<span data-ttu-id="33b48-152">Especifica la posibilidad de porcentaje de precipitación.</span><span class="sxs-lookup"><span data-stu-id="33b48-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="33b48-153">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="33b48-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="33b48-154">shortday</span><span class="sxs-lookup"><span data-stu-id="33b48-154">shortday</span></span>  <br/> |<span data-ttu-id="33b48-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="33b48-155">xs:string</span></span>  <br/> |<span data-ttu-id="33b48-156">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-156">required</span></span>  <br/> |<span data-ttu-id="33b48-157">Especifica un día de forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="33b48-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="33b48-158">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="33b48-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="33b48-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="33b48-159">skycodeday</span></span>  <br/> |<span data-ttu-id="33b48-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="33b48-160">xs:integer</span></span>  <br/> |<span data-ttu-id="33b48-161">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-161">required</span></span>  <br/> |<span data-ttu-id="33b48-162">Especifica un código de las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="33b48-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="33b48-163">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="33b48-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="33b48-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="33b48-164">skytextday</span></span>  <br/> |<span data-ttu-id="33b48-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="33b48-165">xs:string</span></span>  <br/> |<span data-ttu-id="33b48-166">necesario</span><span class="sxs-lookup"><span data-stu-id="33b48-166">required</span></span>  <br/> |<span data-ttu-id="33b48-167">Especifica una o dos palabras que describen las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="33b48-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="33b48-168">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="33b48-168">A value of the type xs:string</span></span>  <br/> |
   

