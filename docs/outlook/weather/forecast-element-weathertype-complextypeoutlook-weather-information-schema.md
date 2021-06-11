---
title: elemento forecast (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Especifica las condiciones meteorológicas futuras de al menos tres días antes, incluido hoy: Hoy, Mañana, Día después de Mañana.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540983"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="f4034-103">elemento forecast (weatherType complexType) (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="f4034-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="f4034-104">Especifica las condiciones meteorológicas futuras de al menos tres días antes, incluido hoy: Hoy, Mañana, Día después de Mañana.</span><span class="sxs-lookup"><span data-stu-id="f4034-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4034-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4034-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4034-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f4034-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f4034-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="f4034-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="f4034-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f4034-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="f4034-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f4034-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f4034-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="f4034-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4034-111">Definición</span><span class="sxs-lookup"><span data-stu-id="f4034-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4034-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f4034-112">Elements and attributes</span></span>

<span data-ttu-id="f4034-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f4034-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f4034-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4034-114">Parent elements</span></span>

|<span data-ttu-id="f4034-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f4034-115">**Element**</span></span>|<span data-ttu-id="f4034-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4034-116">**Type**</span></span>|<span data-ttu-id="f4034-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4034-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4034-118">tiempo</span><span class="sxs-lookup"><span data-stu-id="f4034-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="f4034-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="f4034-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="f4034-120">Especifica las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="f4034-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4034-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4034-121">Child elements</span></span>

<span data-ttu-id="f4034-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4034-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4034-123">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4034-123">Attributes</span></span>

|<span data-ttu-id="f4034-124">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f4034-124">**Attribute**</span></span>|<span data-ttu-id="f4034-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4034-125">**Type**</span></span>|<span data-ttu-id="f4034-126">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f4034-126">**Required**</span></span>|<span data-ttu-id="f4034-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4034-127">**Description**</span></span>|<span data-ttu-id="f4034-128">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f4034-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f4034-129">date</span><span class="sxs-lookup"><span data-stu-id="f4034-129">date</span></span>  <br/> |<span data-ttu-id="f4034-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="f4034-130">xs:date</span></span>  <br/> |<span data-ttu-id="f4034-131">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-131">required</span></span>  <br/> |<span data-ttu-id="f4034-132">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="f4034-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="f4034-133">Valor del tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="f4034-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="f4034-134">día</span><span class="sxs-lookup"><span data-stu-id="f4034-134">day</span></span>  <br/> |<span data-ttu-id="f4034-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="f4034-135">xs:string</span></span>  <br/> |<span data-ttu-id="f4034-136">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-136">required</span></span>  <br/> |<span data-ttu-id="f4034-137">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="f4034-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="f4034-138">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="f4034-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f4034-139">high</span><span class="sxs-lookup"><span data-stu-id="f4034-139">high</span></span>  <br/> |<span data-ttu-id="f4034-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-140">xs:integer</span></span>  <br/> |<span data-ttu-id="f4034-141">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-141">required</span></span>  <br/> |<span data-ttu-id="f4034-142">Especifica la temperatura más alta prevista.</span><span class="sxs-lookup"><span data-stu-id="f4034-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="f4034-143">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f4034-144">low</span><span class="sxs-lookup"><span data-stu-id="f4034-144">low</span></span>  <br/> |<span data-ttu-id="f4034-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-145">xs:integer</span></span>  <br/> |<span data-ttu-id="f4034-146">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-146">required</span></span>  <br/> |<span data-ttu-id="f4034-147">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="f4034-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="f4034-148">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f4034-149">precip</span><span class="sxs-lookup"><span data-stu-id="f4034-149">precip</span></span>  <br/> |<span data-ttu-id="f4034-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-150">xs:integer</span></span>  <br/> |<span data-ttu-id="f4034-151">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-151">required</span></span>  <br/> |<span data-ttu-id="f4034-152">Especifica el porcentaje de posibilidad de precipitación.</span><span class="sxs-lookup"><span data-stu-id="f4034-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="f4034-153">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f4034-154">shortday</span><span class="sxs-lookup"><span data-stu-id="f4034-154">shortday</span></span>  <br/> |<span data-ttu-id="f4034-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="f4034-155">xs:string</span></span>  <br/> |<span data-ttu-id="f4034-156">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-156">required</span></span>  <br/> |<span data-ttu-id="f4034-157">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="f4034-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="f4034-158">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="f4034-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f4034-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="f4034-159">skycodeday</span></span>  <br/> |<span data-ttu-id="f4034-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-160">xs:integer</span></span>  <br/> |<span data-ttu-id="f4034-161">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-161">required</span></span>  <br/> |<span data-ttu-id="f4034-162">Especifica un código para las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="f4034-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f4034-163">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="f4034-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f4034-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="f4034-164">skytextday</span></span>  <br/> |<span data-ttu-id="f4034-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="f4034-165">xs:string</span></span>  <br/> |<span data-ttu-id="f4034-166">necesario</span><span class="sxs-lookup"><span data-stu-id="f4034-166">required</span></span>  <br/> |<span data-ttu-id="f4034-167">Especifica de una a dos palabras que describen las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="f4034-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f4034-168">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="f4034-168">A value of the type xs:string</span></span>  <br/> |
   

