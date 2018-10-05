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
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387037"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="a2898-103">currentType complexType (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="a2898-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="a2898-104">Define los parámetros acerca de las condiciones del tiempo actual de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="a2898-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="a2898-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="a2898-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2898-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2898-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="a2898-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a2898-107">**Schema file**</span></span> <br/> |<span data-ttu-id="a2898-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="a2898-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="a2898-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="a2898-109">**Extension base**</span></span> <br/> |<span data-ttu-id="a2898-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a2898-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2898-111">Definición</span><span class="sxs-lookup"><span data-stu-id="a2898-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a2898-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a2898-112">Elements and attributes</span></span>

<span data-ttu-id="a2898-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a2898-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2898-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a2898-114">Child elements</span></span>

<span data-ttu-id="a2898-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a2898-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2898-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="a2898-116">Attributes</span></span>

|<span data-ttu-id="a2898-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a2898-117">**Attribute**</span></span>|<span data-ttu-id="a2898-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a2898-118">**Type**</span></span>|<span data-ttu-id="a2898-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a2898-119">**Required**</span></span>|<span data-ttu-id="a2898-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a2898-120">**Description**</span></span>|<span data-ttu-id="a2898-121">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="a2898-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2898-122">date</span><span class="sxs-lookup"><span data-stu-id="a2898-122">date</span></span>  <br/> |<span data-ttu-id="a2898-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="a2898-123">xs:date</span></span>  <br/> |<span data-ttu-id="a2898-124">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-124">required</span></span>  <br/> |<span data-ttu-id="a2898-125">Especifica la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="a2898-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="a2898-126">Un valor de tipo de xs: Date</span><span class="sxs-lookup"><span data-stu-id="a2898-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="a2898-127">día</span><span class="sxs-lookup"><span data-stu-id="a2898-127">day</span></span>  <br/> |<span data-ttu-id="a2898-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2898-128">xs:string</span></span>  <br/> |<span data-ttu-id="a2898-129">opcional</span><span class="sxs-lookup"><span data-stu-id="a2898-129">optional</span></span>  <br/> |<span data-ttu-id="a2898-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="a2898-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="a2898-131">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="a2898-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a2898-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="a2898-132">feelslike</span></span>  <br/> |<span data-ttu-id="a2898-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a2898-133">xs:integer</span></span>  <br/> |<span data-ttu-id="a2898-134">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-134">required</span></span>  <br/> |<span data-ttu-id="a2898-135">Especifica la temperatura de cómo se siente la meteorología actual como.</span><span class="sxs-lookup"><span data-stu-id="a2898-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="a2898-136">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="a2898-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a2898-137">humedad</span><span class="sxs-lookup"><span data-stu-id="a2898-137">humidity</span></span>  <br/> |<span data-ttu-id="a2898-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a2898-138">xs:integer</span></span>  <br/> |<span data-ttu-id="a2898-139">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-139">required</span></span>  <br/> |<span data-ttu-id="a2898-140">Especifica el valor numérico humedad actual.</span><span class="sxs-lookup"><span data-stu-id="a2898-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="a2898-141">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="a2898-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a2898-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="a2898-142">observationpoint</span></span>  <br/> |<span data-ttu-id="a2898-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2898-143">xs:string</span></span>  <br/> |<span data-ttu-id="a2898-144">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-144">required</span></span>  <br/> |<span data-ttu-id="a2898-145">Especifica dónde se observa la información meteorológica actual desde.</span><span class="sxs-lookup"><span data-stu-id="a2898-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="a2898-146">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="a2898-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a2898-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="a2898-147">observationtime</span></span>  <br/> |<span data-ttu-id="a2898-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="a2898-148">xs:time</span></span>  <br/> |<span data-ttu-id="a2898-149">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-149">required</span></span>  <br/> |<span data-ttu-id="a2898-150">Especifica cuándo se observa la información meteorológica actual en.</span><span class="sxs-lookup"><span data-stu-id="a2898-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="a2898-151">Un valor del tipo de xs: Time</span><span class="sxs-lookup"><span data-stu-id="a2898-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="a2898-152">shortday</span><span class="sxs-lookup"><span data-stu-id="a2898-152">shortday</span></span>  <br/> |<span data-ttu-id="a2898-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2898-153">xs:string</span></span>  <br/> |<span data-ttu-id="a2898-154">opcional</span><span class="sxs-lookup"><span data-stu-id="a2898-154">optional</span></span>  <br/> |<span data-ttu-id="a2898-155">Especifica un día de forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="a2898-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="a2898-156">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="a2898-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a2898-157">skycode</span><span class="sxs-lookup"><span data-stu-id="a2898-157">skycode</span></span>  <br/> |<span data-ttu-id="a2898-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a2898-158">xs:integer</span></span>  <br/> |<span data-ttu-id="a2898-159">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-159">required</span></span>  <br/> |<span data-ttu-id="a2898-160">Especifica un código de número entero para las condiciones del tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="a2898-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="a2898-161">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="a2898-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a2898-162">skytext</span><span class="sxs-lookup"><span data-stu-id="a2898-162">skytext</span></span>  <br/> |<span data-ttu-id="a2898-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2898-163">xs:string</span></span>  <br/> |<span data-ttu-id="a2898-164">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-164">required</span></span>  <br/> |<span data-ttu-id="a2898-165">Especifica las palabras de uno o dos que describa las condiciones de tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="a2898-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="a2898-166">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="a2898-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a2898-167">temperatura</span><span class="sxs-lookup"><span data-stu-id="a2898-167">temperature</span></span>  <br/> |<span data-ttu-id="a2898-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a2898-168">xs:integer</span></span>  <br/> |<span data-ttu-id="a2898-169">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-169">required</span></span>  <br/> |<span data-ttu-id="a2898-170">Especifica la temperatura de la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="a2898-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="a2898-171">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="a2898-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a2898-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="a2898-172">winddisplay</span></span>  <br/> |<span data-ttu-id="a2898-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2898-173">xs:string</span></span>  <br/> |<span data-ttu-id="a2898-174">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-174">required</span></span>  <br/> |<span data-ttu-id="a2898-175">Una cadena que describe las condiciones de aire actual.</span><span class="sxs-lookup"><span data-stu-id="a2898-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="a2898-176">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="a2898-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a2898-177">velocidad del viento</span><span class="sxs-lookup"><span data-stu-id="a2898-177">windspeed</span></span>  <br/> |<span data-ttu-id="a2898-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a2898-178">xs:integer</span></span>  <br/> |<span data-ttu-id="a2898-179">necesario</span><span class="sxs-lookup"><span data-stu-id="a2898-179">required</span></span>  <br/> |<span data-ttu-id="a2898-180">Especifica el valor actual de la velocidad de aire numéricos.</span><span class="sxs-lookup"><span data-stu-id="a2898-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="a2898-181">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="a2898-181">A value of the type xs:integer</span></span>  <br/> |
   

