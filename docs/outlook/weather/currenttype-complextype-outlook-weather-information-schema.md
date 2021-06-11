---
title: currentType complexType (Outlook de información meteorológica)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540990"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="5b3c9-103">currentType complexType (Outlook de información meteorológica)</span><span class="sxs-lookup"><span data-stu-id="5b3c9-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="5b3c9-104">Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="5b3c9-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="5b3c9-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b3c9-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="5b3c9-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-107">**Schema file**</span></span> <br/> |<span data-ttu-id="5b3c9-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="5b3c9-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="5b3c9-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-109">**Extension base**</span></span> <br/> |<span data-ttu-id="5b3c9-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5b3c9-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b3c9-111">Definición</span><span class="sxs-lookup"><span data-stu-id="5b3c9-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5b3c9-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5b3c9-112">Elements and attributes</span></span>

<span data-ttu-id="5b3c9-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5b3c9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5b3c9-114">Child elements</span></span>

<span data-ttu-id="5b3c9-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b3c9-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="5b3c9-116">Attributes</span></span>

|<span data-ttu-id="5b3c9-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-117">**Attribute**</span></span>|<span data-ttu-id="5b3c9-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-118">**Type**</span></span>|<span data-ttu-id="5b3c9-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-119">**Required**</span></span>|<span data-ttu-id="5b3c9-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-120">**Description**</span></span>|<span data-ttu-id="5b3c9-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5b3c9-122">date</span><span class="sxs-lookup"><span data-stu-id="5b3c9-122">date</span></span>  <br/> |<span data-ttu-id="5b3c9-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="5b3c9-123">xs:date</span></span>  <br/> |<span data-ttu-id="5b3c9-124">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-124">required</span></span>  <br/> |<span data-ttu-id="5b3c9-125">Especifica la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="5b3c9-126">Valor del tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="5b3c9-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="5b3c9-127">día</span><span class="sxs-lookup"><span data-stu-id="5b3c9-127">day</span></span>  <br/> |<span data-ttu-id="5b3c9-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-128">xs:string</span></span>  <br/> |<span data-ttu-id="5b3c9-129">opcional</span><span class="sxs-lookup"><span data-stu-id="5b3c9-129">optional</span></span>  <br/> |<span data-ttu-id="5b3c9-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="5b3c9-131">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5b3c9-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="5b3c9-132">feelslike</span></span>  <br/> |<span data-ttu-id="5b3c9-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-133">xs:integer</span></span>  <br/> |<span data-ttu-id="5b3c9-134">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-134">required</span></span>  <br/> |<span data-ttu-id="5b3c9-135">Especifica la temperatura de cómo se siente el tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="5b3c9-136">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5b3c9-137">humedad</span><span class="sxs-lookup"><span data-stu-id="5b3c9-137">humidity</span></span>  <br/> |<span data-ttu-id="5b3c9-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-138">xs:integer</span></span>  <br/> |<span data-ttu-id="5b3c9-139">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-139">required</span></span>  <br/> |<span data-ttu-id="5b3c9-140">Especifica el valor de humedad numérica actual.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="5b3c9-141">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5b3c9-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="5b3c9-142">observationpoint</span></span>  <br/> |<span data-ttu-id="5b3c9-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-143">xs:string</span></span>  <br/> |<span data-ttu-id="5b3c9-144">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-144">required</span></span>  <br/> |<span data-ttu-id="5b3c9-145">Especifica desde dónde se observa la información meteorológica actual.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="5b3c9-146">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5b3c9-147">tiempo de observación</span><span class="sxs-lookup"><span data-stu-id="5b3c9-147">observationtime</span></span>  <br/> |<span data-ttu-id="5b3c9-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="5b3c9-148">xs:time</span></span>  <br/> |<span data-ttu-id="5b3c9-149">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-149">required</span></span>  <br/> |<span data-ttu-id="5b3c9-150">Especifica cuándo se observa la información meteorológica actual en.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="5b3c9-151">Valor del tipo xs:time</span><span class="sxs-lookup"><span data-stu-id="5b3c9-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="5b3c9-152">shortday</span><span class="sxs-lookup"><span data-stu-id="5b3c9-152">shortday</span></span>  <br/> |<span data-ttu-id="5b3c9-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-153">xs:string</span></span>  <br/> |<span data-ttu-id="5b3c9-154">opcional</span><span class="sxs-lookup"><span data-stu-id="5b3c9-154">optional</span></span>  <br/> |<span data-ttu-id="5b3c9-155">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="5b3c9-156">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5b3c9-157">skycode</span><span class="sxs-lookup"><span data-stu-id="5b3c9-157">skycode</span></span>  <br/> |<span data-ttu-id="5b3c9-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-158">xs:integer</span></span>  <br/> |<span data-ttu-id="5b3c9-159">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-159">required</span></span>  <br/> |<span data-ttu-id="5b3c9-160">Especifica un código entero para las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="5b3c9-161">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5b3c9-162">skytext</span><span class="sxs-lookup"><span data-stu-id="5b3c9-162">skytext</span></span>  <br/> |<span data-ttu-id="5b3c9-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-163">xs:string</span></span>  <br/> |<span data-ttu-id="5b3c9-164">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-164">required</span></span>  <br/> |<span data-ttu-id="5b3c9-165">Especifica de una a dos palabras que describen las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="5b3c9-166">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5b3c9-167">temperatura</span><span class="sxs-lookup"><span data-stu-id="5b3c9-167">temperature</span></span>  <br/> |<span data-ttu-id="5b3c9-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-168">xs:integer</span></span>  <br/> |<span data-ttu-id="5b3c9-169">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-169">required</span></span>  <br/> |<span data-ttu-id="5b3c9-170">Especifica la temperatura actual de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="5b3c9-171">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="5b3c9-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="5b3c9-172">winddisplay</span></span>  <br/> |<span data-ttu-id="5b3c9-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-173">xs:string</span></span>  <br/> |<span data-ttu-id="5b3c9-174">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-174">required</span></span>  <br/> |<span data-ttu-id="5b3c9-175">Cadena que describe las condiciones de viento actuales.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="5b3c9-176">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="5b3c9-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="5b3c9-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="5b3c9-177">windspeed</span></span>  <br/> |<span data-ttu-id="5b3c9-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-178">xs:integer</span></span>  <br/> |<span data-ttu-id="5b3c9-179">necesario</span><span class="sxs-lookup"><span data-stu-id="5b3c9-179">required</span></span>  <br/> |<span data-ttu-id="5b3c9-180">Especifica el valor de velocidad de viento numérico actual.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="5b3c9-181">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="5b3c9-181">A value of the type xs:integer</span></span>  <br/> |
   

