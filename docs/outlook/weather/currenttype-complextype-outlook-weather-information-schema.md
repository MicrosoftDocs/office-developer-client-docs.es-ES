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
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338454"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="ffe90-103">currentType complexType (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="ffe90-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="ffe90-104">Define los parámetros sobre las condiciones meteorológicas actuales de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ffe90-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="ffe90-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ffe90-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffe90-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ffe90-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="ffe90-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ffe90-107">**Schema file**</span></span> <br/> |<span data-ttu-id="ffe90-108">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="ffe90-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="ffe90-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ffe90-109">**Extension base**</span></span> <br/> |<span data-ttu-id="ffe90-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ffe90-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ffe90-111">Definición</span><span class="sxs-lookup"><span data-stu-id="ffe90-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ffe90-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ffe90-112">Elements and attributes</span></span>

<span data-ttu-id="ffe90-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ffe90-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ffe90-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ffe90-114">Child elements</span></span>

<span data-ttu-id="ffe90-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ffe90-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffe90-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffe90-116">Attributes</span></span>

|<span data-ttu-id="ffe90-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ffe90-117">**Attribute**</span></span>|<span data-ttu-id="ffe90-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ffe90-118">**Type**</span></span>|<span data-ttu-id="ffe90-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ffe90-119">**Required**</span></span>|<span data-ttu-id="ffe90-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ffe90-120">**Description**</span></span>|<span data-ttu-id="ffe90-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ffe90-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ffe90-122">fecha</span><span class="sxs-lookup"><span data-stu-id="ffe90-122">date</span></span>  <br/> |<span data-ttu-id="ffe90-123">XS: Date</span><span class="sxs-lookup"><span data-stu-id="ffe90-123">xs:date</span></span>  <br/> |<span data-ttu-id="ffe90-124">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-124">required</span></span>  <br/> |<span data-ttu-id="ffe90-125">Especifica la fecha de hoy.</span><span class="sxs-lookup"><span data-stu-id="ffe90-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="ffe90-126">Un valor de tipo XS: Date</span><span class="sxs-lookup"><span data-stu-id="ffe90-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="ffe90-127">cotidiano</span><span class="sxs-lookup"><span data-stu-id="ffe90-127">day</span></span>  <br/> |<span data-ttu-id="ffe90-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-128">xs:string</span></span>  <br/> |<span data-ttu-id="ffe90-129">opcional</span><span class="sxs-lookup"><span data-stu-id="ffe90-129">optional</span></span>  <br/> |<span data-ttu-id="ffe90-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="ffe90-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="ffe90-131">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ffe90-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="ffe90-132">feelslike</span></span>  <br/> |<span data-ttu-id="ffe90-133">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-133">xs:integer</span></span>  <br/> |<span data-ttu-id="ffe90-134">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-134">required</span></span>  <br/> |<span data-ttu-id="ffe90-135">Especifica la temperatura del tiempo actual que parece.</span><span class="sxs-lookup"><span data-stu-id="ffe90-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="ffe90-136">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ffe90-137">humedad</span><span class="sxs-lookup"><span data-stu-id="ffe90-137">humidity</span></span>  <br/> |<span data-ttu-id="ffe90-138">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-138">xs:integer</span></span>  <br/> |<span data-ttu-id="ffe90-139">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-139">required</span></span>  <br/> |<span data-ttu-id="ffe90-140">Especifica el valor de humedad numérica actual.</span><span class="sxs-lookup"><span data-stu-id="ffe90-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="ffe90-141">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ffe90-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="ffe90-142">observationpoint</span></span>  <br/> |<span data-ttu-id="ffe90-143">XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-143">xs:string</span></span>  <br/> |<span data-ttu-id="ffe90-144">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-144">required</span></span>  <br/> |<span data-ttu-id="ffe90-145">Especifica dónde se observa la información meteorológica actual.</span><span class="sxs-lookup"><span data-stu-id="ffe90-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="ffe90-146">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ffe90-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="ffe90-147">observationtime</span></span>  <br/> |<span data-ttu-id="ffe90-148">XS: Time</span><span class="sxs-lookup"><span data-stu-id="ffe90-148">xs:time</span></span>  <br/> |<span data-ttu-id="ffe90-149">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-149">required</span></span>  <br/> |<span data-ttu-id="ffe90-150">Especifica cuándo se observa la información meteorológica actual en.</span><span class="sxs-lookup"><span data-stu-id="ffe90-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="ffe90-151">Un valor del tipo XS: Time</span><span class="sxs-lookup"><span data-stu-id="ffe90-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="ffe90-152">shortday</span><span class="sxs-lookup"><span data-stu-id="ffe90-152">shortday</span></span>  <br/> |<span data-ttu-id="ffe90-153">XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-153">xs:string</span></span>  <br/> |<span data-ttu-id="ffe90-154">opcional</span><span class="sxs-lookup"><span data-stu-id="ffe90-154">optional</span></span>  <br/> |<span data-ttu-id="ffe90-155">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="ffe90-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="ffe90-156">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ffe90-157">skycode</span><span class="sxs-lookup"><span data-stu-id="ffe90-157">skycode</span></span>  <br/> |<span data-ttu-id="ffe90-158">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-158">xs:integer</span></span>  <br/> |<span data-ttu-id="ffe90-159">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-159">required</span></span>  <br/> |<span data-ttu-id="ffe90-160">Especifica un código de número entero para las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="ffe90-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="ffe90-161">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ffe90-162">skytext</span><span class="sxs-lookup"><span data-stu-id="ffe90-162">skytext</span></span>  <br/> |<span data-ttu-id="ffe90-163">XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-163">xs:string</span></span>  <br/> |<span data-ttu-id="ffe90-164">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-164">required</span></span>  <br/> |<span data-ttu-id="ffe90-165">Especifica de una a dos palabras que describen las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="ffe90-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="ffe90-166">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ffe90-167">medidor</span><span class="sxs-lookup"><span data-stu-id="ffe90-167">temperature</span></span>  <br/> |<span data-ttu-id="ffe90-168">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-168">xs:integer</span></span>  <br/> |<span data-ttu-id="ffe90-169">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-169">required</span></span>  <br/> |<span data-ttu-id="ffe90-170">Especifica la temperatura actual de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="ffe90-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="ffe90-171">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ffe90-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="ffe90-172">winddisplay</span></span>  <br/> |<span data-ttu-id="ffe90-173">XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-173">xs:string</span></span>  <br/> |<span data-ttu-id="ffe90-174">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-174">required</span></span>  <br/> |<span data-ttu-id="ffe90-175">Una cadena que describe las condiciones de viento actuales.</span><span class="sxs-lookup"><span data-stu-id="ffe90-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="ffe90-176">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ffe90-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ffe90-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="ffe90-177">windspeed</span></span>  <br/> |<span data-ttu-id="ffe90-178">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-178">xs:integer</span></span>  <br/> |<span data-ttu-id="ffe90-179">necesario</span><span class="sxs-lookup"><span data-stu-id="ffe90-179">required</span></span>  <br/> |<span data-ttu-id="ffe90-180">Especifica el valor numérico de velocidad de viento actual.</span><span class="sxs-lookup"><span data-stu-id="ffe90-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="ffe90-181">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ffe90-181">A value of the type xs:integer</span></span>  <br/> |
   

