---
title: elemento Forecast (complexType weatherType) (esquema de información de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Especifica las condiciones meteorológicas futuras de al menos tres días de anticipación, como hoy: hoy, mañana, día después de mañana.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540983"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="0079f-103">elemento Forecast (complexType weatherType) (esquema de información de tiempo de Outlook)</span><span class="sxs-lookup"><span data-stu-id="0079f-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="0079f-104">Especifica las condiciones meteorológicas futuras de al menos tres días de anticipación, como hoy: hoy, mañana, día después de mañana.</span><span class="sxs-lookup"><span data-stu-id="0079f-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0079f-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0079f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0079f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0079f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0079f-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="0079f-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="0079f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0079f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="0079f-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0079f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0079f-110">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="0079f-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0079f-111">Definición</span><span class="sxs-lookup"><span data-stu-id="0079f-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="0079f-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0079f-112">Elements and attributes</span></span>

<span data-ttu-id="0079f-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0079f-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0079f-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0079f-114">Parent elements</span></span>

|<span data-ttu-id="0079f-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0079f-115">**Element**</span></span>|<span data-ttu-id="0079f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0079f-116">**Type**</span></span>|<span data-ttu-id="0079f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0079f-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0079f-118">Boletín</span><span class="sxs-lookup"><span data-stu-id="0079f-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="0079f-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="0079f-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="0079f-120">Especifica las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="0079f-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0079f-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0079f-121">Child elements</span></span>

<span data-ttu-id="0079f-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0079f-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0079f-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="0079f-123">Attributes</span></span>

|<span data-ttu-id="0079f-124">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0079f-124">**Attribute**</span></span>|<span data-ttu-id="0079f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0079f-125">**Type**</span></span>|<span data-ttu-id="0079f-126">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0079f-126">**Required**</span></span>|<span data-ttu-id="0079f-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0079f-127">**Description**</span></span>|<span data-ttu-id="0079f-128">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="0079f-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0079f-129">date</span><span class="sxs-lookup"><span data-stu-id="0079f-129">date</span></span>  <br/> |<span data-ttu-id="0079f-130">XS: Date</span><span class="sxs-lookup"><span data-stu-id="0079f-130">xs:date</span></span>  <br/> |<span data-ttu-id="0079f-131">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-131">required</span></span>  <br/> |<span data-ttu-id="0079f-132">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="0079f-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="0079f-133">Un valor de tipo XS: Date</span><span class="sxs-lookup"><span data-stu-id="0079f-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="0079f-134">cotidiano</span><span class="sxs-lookup"><span data-stu-id="0079f-134">day</span></span>  <br/> |<span data-ttu-id="0079f-135">XS: String</span><span class="sxs-lookup"><span data-stu-id="0079f-135">xs:string</span></span>  <br/> |<span data-ttu-id="0079f-136">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-136">required</span></span>  <br/> |<span data-ttu-id="0079f-137">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="0079f-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="0079f-138">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="0079f-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0079f-139">mayor</span><span class="sxs-lookup"><span data-stu-id="0079f-139">high</span></span>  <br/> |<span data-ttu-id="0079f-140">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-140">xs:integer</span></span>  <br/> |<span data-ttu-id="0079f-141">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-141">required</span></span>  <br/> |<span data-ttu-id="0079f-142">Especifica la temperatura más alta prevista.</span><span class="sxs-lookup"><span data-stu-id="0079f-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="0079f-143">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0079f-144">baja</span><span class="sxs-lookup"><span data-stu-id="0079f-144">low</span></span>  <br/> |<span data-ttu-id="0079f-145">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-145">xs:integer</span></span>  <br/> |<span data-ttu-id="0079f-146">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-146">required</span></span>  <br/> |<span data-ttu-id="0079f-147">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="0079f-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="0079f-148">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0079f-149">precip</span><span class="sxs-lookup"><span data-stu-id="0079f-149">precip</span></span>  <br/> |<span data-ttu-id="0079f-150">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-150">xs:integer</span></span>  <br/> |<span data-ttu-id="0079f-151">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-151">required</span></span>  <br/> |<span data-ttu-id="0079f-152">Especifica el porcentaje de probabilidad de precipitación.</span><span class="sxs-lookup"><span data-stu-id="0079f-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="0079f-153">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0079f-154">shortday</span><span class="sxs-lookup"><span data-stu-id="0079f-154">shortday</span></span>  <br/> |<span data-ttu-id="0079f-155">XS: String</span><span class="sxs-lookup"><span data-stu-id="0079f-155">xs:string</span></span>  <br/> |<span data-ttu-id="0079f-156">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-156">required</span></span>  <br/> |<span data-ttu-id="0079f-157">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="0079f-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="0079f-158">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="0079f-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0079f-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="0079f-159">skycodeday</span></span>  <br/> |<span data-ttu-id="0079f-160">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-160">xs:integer</span></span>  <br/> |<span data-ttu-id="0079f-161">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-161">required</span></span>  <br/> |<span data-ttu-id="0079f-162">Especifica un código para las condiciones de previsión.</span><span class="sxs-lookup"><span data-stu-id="0079f-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="0079f-163">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="0079f-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0079f-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="0079f-164">skytextday</span></span>  <br/> |<span data-ttu-id="0079f-165">XS: String</span><span class="sxs-lookup"><span data-stu-id="0079f-165">xs:string</span></span>  <br/> |<span data-ttu-id="0079f-166">necesario</span><span class="sxs-lookup"><span data-stu-id="0079f-166">required</span></span>  <br/> |<span data-ttu-id="0079f-167">Especifica de una a dos palabras que describen las condiciones de previsión.</span><span class="sxs-lookup"><span data-stu-id="0079f-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="0079f-168">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="0079f-168">A value of the type xs:string</span></span>  <br/> |
   

