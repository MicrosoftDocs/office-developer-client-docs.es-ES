---
title: currentType complexType (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Define los parámetros acerca de las condiciones del tiempo actual de una ubicación.
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821227"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="20020-103">currentType complexType (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="20020-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="20020-104">Define los parámetros acerca de las condiciones del tiempo actual de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="20020-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="20020-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="20020-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20020-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20020-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="20020-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="20020-107">**Schema file**</span></span> <br/> |<span data-ttu-id="20020-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="20020-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="20020-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="20020-109">**Extension base**</span></span> <br/> |<span data-ttu-id="20020-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="20020-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20020-111">Definición</span><span class="sxs-lookup"><span data-stu-id="20020-111">Definition</span></span>

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="20020-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="20020-112">Elements and attributes</span></span>

<span data-ttu-id="20020-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="20020-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="20020-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20020-114">Child elements</span></span>

<span data-ttu-id="20020-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="20020-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20020-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="20020-116">Attributes</span></span>

|<span data-ttu-id="20020-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="20020-117">**Attribute**</span></span>|<span data-ttu-id="20020-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="20020-118">**Type**</span></span>|<span data-ttu-id="20020-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="20020-119">**Required**</span></span>|<span data-ttu-id="20020-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20020-120">**Description**</span></span>|<span data-ttu-id="20020-121">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="20020-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20020-122">date</span><span class="sxs-lookup"><span data-stu-id="20020-122">date</span></span>  <br/> |<span data-ttu-id="20020-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="20020-123">xs:date</span></span>  <br/> |<span data-ttu-id="20020-124">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-124">required</span></span>  <br/> |<span data-ttu-id="20020-125">Especifica la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="20020-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="20020-126">Un valor de tipo de xs: Date</span><span class="sxs-lookup"><span data-stu-id="20020-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="20020-127">día</span><span class="sxs-lookup"><span data-stu-id="20020-127">day</span></span>  <br/> |<span data-ttu-id="20020-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="20020-128">xs:string</span></span>  <br/> |<span data-ttu-id="20020-129">opcional</span><span class="sxs-lookup"><span data-stu-id="20020-129">optional</span></span>  <br/> |<span data-ttu-id="20020-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="20020-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="20020-131">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="20020-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="20020-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="20020-132">feelslike</span></span>  <br/> |<span data-ttu-id="20020-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="20020-133">xs:integer</span></span>  <br/> |<span data-ttu-id="20020-134">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-134">required</span></span>  <br/> |<span data-ttu-id="20020-135">Especifica la temperatura de cómo se siente la meteorología actual como.</span><span class="sxs-lookup"><span data-stu-id="20020-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="20020-136">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="20020-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="20020-137">humedad</span><span class="sxs-lookup"><span data-stu-id="20020-137">humidity</span></span>  <br/> |<span data-ttu-id="20020-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="20020-138">xs:integer</span></span>  <br/> |<span data-ttu-id="20020-139">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-139">required</span></span>  <br/> |<span data-ttu-id="20020-140">Especifica el valor numérico humedad actual.</span><span class="sxs-lookup"><span data-stu-id="20020-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="20020-141">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="20020-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="20020-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="20020-142">observationpoint</span></span>  <br/> |<span data-ttu-id="20020-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="20020-143">xs:string</span></span>  <br/> |<span data-ttu-id="20020-144">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-144">required</span></span>  <br/> |<span data-ttu-id="20020-145">Especifica dónde se observa la información meteorológica actual desde.</span><span class="sxs-lookup"><span data-stu-id="20020-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="20020-146">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="20020-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="20020-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="20020-147">observationtime</span></span>  <br/> |<span data-ttu-id="20020-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="20020-148">xs:time</span></span>  <br/> |<span data-ttu-id="20020-149">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-149">required</span></span>  <br/> |<span data-ttu-id="20020-150">Especifica cuándo se observa la información meteorológica actual en.</span><span class="sxs-lookup"><span data-stu-id="20020-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="20020-151">Un valor del tipo de xs: Time</span><span class="sxs-lookup"><span data-stu-id="20020-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="20020-152">shortday</span><span class="sxs-lookup"><span data-stu-id="20020-152">shortday</span></span>  <br/> |<span data-ttu-id="20020-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="20020-153">xs:string</span></span>  <br/> |<span data-ttu-id="20020-154">opcional</span><span class="sxs-lookup"><span data-stu-id="20020-154">optional</span></span>  <br/> |<span data-ttu-id="20020-155">Especifica un día de forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="20020-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="20020-156">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="20020-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="20020-157">skycode</span><span class="sxs-lookup"><span data-stu-id="20020-157">skycode</span></span>  <br/> |<span data-ttu-id="20020-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="20020-158">xs:integer</span></span>  <br/> |<span data-ttu-id="20020-159">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-159">required</span></span>  <br/> |<span data-ttu-id="20020-160">Especifica un código de número entero para las condiciones del tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="20020-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="20020-161">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="20020-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="20020-162">skytext</span><span class="sxs-lookup"><span data-stu-id="20020-162">skytext</span></span>  <br/> |<span data-ttu-id="20020-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="20020-163">xs:string</span></span>  <br/> |<span data-ttu-id="20020-164">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-164">required</span></span>  <br/> |<span data-ttu-id="20020-165">Especifica las palabras de uno o dos que describa las condiciones de tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="20020-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="20020-166">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="20020-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="20020-167">temperatura</span><span class="sxs-lookup"><span data-stu-id="20020-167">temperature</span></span>  <br/> |<span data-ttu-id="20020-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="20020-168">xs:integer</span></span>  <br/> |<span data-ttu-id="20020-169">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-169">required</span></span>  <br/> |<span data-ttu-id="20020-170">Especifica la temperatura de la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="20020-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="20020-171">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="20020-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="20020-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="20020-172">winddisplay</span></span>  <br/> |<span data-ttu-id="20020-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="20020-173">xs:string</span></span>  <br/> |<span data-ttu-id="20020-174">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-174">required</span></span>  <br/> |<span data-ttu-id="20020-175">Una cadena que describe las condiciones de aire actual.</span><span class="sxs-lookup"><span data-stu-id="20020-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="20020-176">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="20020-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="20020-177">velocidad del viento</span><span class="sxs-lookup"><span data-stu-id="20020-177">windspeed</span></span>  <br/> |<span data-ttu-id="20020-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="20020-178">xs:integer</span></span>  <br/> |<span data-ttu-id="20020-179">necesario</span><span class="sxs-lookup"><span data-stu-id="20020-179">required</span></span>  <br/> |<span data-ttu-id="20020-180">Especifica el valor actual de la velocidad de aire numéricos.</span><span class="sxs-lookup"><span data-stu-id="20020-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="20020-181">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="20020-181">A value of the type xs:integer</span></span>  <br/> |
   

