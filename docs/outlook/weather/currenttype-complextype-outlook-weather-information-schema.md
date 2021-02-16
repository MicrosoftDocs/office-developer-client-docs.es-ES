---
title: currentType complexType (esquema de información meteorológica de Outlook)
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
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="076eb-103">currentType complexType (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="076eb-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="076eb-104">Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="076eb-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="076eb-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="076eb-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="076eb-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="076eb-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="076eb-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="076eb-107">**Schema file**</span></span> <br/> |<span data-ttu-id="076eb-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="076eb-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="076eb-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="076eb-109">**Extension base**</span></span> <br/> |<span data-ttu-id="076eb-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="076eb-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="076eb-111">Definición</span><span class="sxs-lookup"><span data-stu-id="076eb-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="076eb-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="076eb-112">Elements and attributes</span></span>

<span data-ttu-id="076eb-113">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="076eb-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="076eb-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="076eb-114">Child elements</span></span>

<span data-ttu-id="076eb-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="076eb-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="076eb-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="076eb-116">Attributes</span></span>

|<span data-ttu-id="076eb-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="076eb-117">**Attribute**</span></span>|<span data-ttu-id="076eb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="076eb-118">**Type**</span></span>|<span data-ttu-id="076eb-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="076eb-119">**Required**</span></span>|<span data-ttu-id="076eb-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="076eb-120">**Description**</span></span>|<span data-ttu-id="076eb-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="076eb-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="076eb-122">date</span><span class="sxs-lookup"><span data-stu-id="076eb-122">date</span></span>  <br/> |<span data-ttu-id="076eb-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="076eb-123">xs:date</span></span>  <br/> |<span data-ttu-id="076eb-124">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-124">required</span></span>  <br/> |<span data-ttu-id="076eb-125">Especifica la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="076eb-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="076eb-126">Un valor del tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="076eb-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="076eb-127">day</span><span class="sxs-lookup"><span data-stu-id="076eb-127">day</span></span>  <br/> |<span data-ttu-id="076eb-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-128">xs:string</span></span>  <br/> |<span data-ttu-id="076eb-129">opcional</span><span class="sxs-lookup"><span data-stu-id="076eb-129">optional</span></span>  <br/> |<span data-ttu-id="076eb-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="076eb-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="076eb-131">Un valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="076eb-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="076eb-132">feelslike</span></span>  <br/> |<span data-ttu-id="076eb-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-133">xs:integer</span></span>  <br/> |<span data-ttu-id="076eb-134">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-134">required</span></span>  <br/> |<span data-ttu-id="076eb-135">Especifica la temperatura de la sensación meteorológica actual.</span><span class="sxs-lookup"><span data-stu-id="076eb-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="076eb-136">Un valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="076eb-137">desa.</span><span class="sxs-lookup"><span data-stu-id="076eb-137">humidity</span></span>  <br/> |<span data-ttu-id="076eb-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-138">xs:integer</span></span>  <br/> |<span data-ttu-id="076eb-139">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-139">required</span></span>  <br/> |<span data-ttu-id="076eb-140">Especifica el valor numérico actual de la humedad.</span><span class="sxs-lookup"><span data-stu-id="076eb-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="076eb-141">Un valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="076eb-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="076eb-142">observationpoint</span></span>  <br/> |<span data-ttu-id="076eb-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-143">xs:string</span></span>  <br/> |<span data-ttu-id="076eb-144">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-144">required</span></span>  <br/> |<span data-ttu-id="076eb-145">Especifica de dónde se observa la información meteorológica actual.</span><span class="sxs-lookup"><span data-stu-id="076eb-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="076eb-146">Un valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="076eb-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="076eb-147">observationtime</span></span>  <br/> |<span data-ttu-id="076eb-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="076eb-148">xs:time</span></span>  <br/> |<span data-ttu-id="076eb-149">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-149">required</span></span>  <br/> |<span data-ttu-id="076eb-150">Especifica cuándo se observa la información meteorológica actual.</span><span class="sxs-lookup"><span data-stu-id="076eb-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="076eb-151">Un valor del tipo xs:time</span><span class="sxs-lookup"><span data-stu-id="076eb-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="076eb-152">shortday</span><span class="sxs-lookup"><span data-stu-id="076eb-152">shortday</span></span>  <br/> |<span data-ttu-id="076eb-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-153">xs:string</span></span>  <br/> |<span data-ttu-id="076eb-154">opcional</span><span class="sxs-lookup"><span data-stu-id="076eb-154">optional</span></span>  <br/> |<span data-ttu-id="076eb-155">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="076eb-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="076eb-156">Un valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="076eb-157">skycode</span><span class="sxs-lookup"><span data-stu-id="076eb-157">skycode</span></span>  <br/> |<span data-ttu-id="076eb-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-158">xs:integer</span></span>  <br/> |<span data-ttu-id="076eb-159">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-159">required</span></span>  <br/> |<span data-ttu-id="076eb-160">Especifica un código entero para las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="076eb-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="076eb-161">Un valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="076eb-162">skytext</span><span class="sxs-lookup"><span data-stu-id="076eb-162">skytext</span></span>  <br/> |<span data-ttu-id="076eb-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-163">xs:string</span></span>  <br/> |<span data-ttu-id="076eb-164">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-164">required</span></span>  <br/> |<span data-ttu-id="076eb-165">Especifica de una a dos palabras que describen las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="076eb-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="076eb-166">Un valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="076eb-167">temperature</span><span class="sxs-lookup"><span data-stu-id="076eb-167">temperature</span></span>  <br/> |<span data-ttu-id="076eb-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-168">xs:integer</span></span>  <br/> |<span data-ttu-id="076eb-169">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-169">required</span></span>  <br/> |<span data-ttu-id="076eb-170">Especifica la temperatura actual de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="076eb-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="076eb-171">Un valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="076eb-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="076eb-172">winddisplay</span></span>  <br/> |<span data-ttu-id="076eb-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-173">xs:string</span></span>  <br/> |<span data-ttu-id="076eb-174">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-174">required</span></span>  <br/> |<span data-ttu-id="076eb-175">Cadena que describe las condiciones actuales del aire.</span><span class="sxs-lookup"><span data-stu-id="076eb-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="076eb-176">Un valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="076eb-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="076eb-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="076eb-177">windspeed</span></span>  <br/> |<span data-ttu-id="076eb-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-178">xs:integer</span></span>  <br/> |<span data-ttu-id="076eb-179">necesario</span><span class="sxs-lookup"><span data-stu-id="076eb-179">required</span></span>  <br/> |<span data-ttu-id="076eb-180">Especifica el valor de velocidad de energía numérico actual.</span><span class="sxs-lookup"><span data-stu-id="076eb-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="076eb-181">Un valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="076eb-181">A value of the type xs:integer</span></span>  <br/> |
   

