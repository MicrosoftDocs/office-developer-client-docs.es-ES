---
title: weatherType complexType (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Especifica las condiciones del tiempo de una ubicación.
ms.openlocfilehash: b333bb6ce60dd1613bceda0a57e7e34c9819bd84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821298"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="90913-103">weatherType complexType (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="90913-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="90913-104">Especifica las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="90913-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="90913-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="90913-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90913-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="90913-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="90913-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="90913-107">**Schema file**</span></span> <br/> |<span data-ttu-id="90913-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="90913-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="90913-109">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="90913-109">**Extension base**</span></span> <br/> |<span data-ttu-id="90913-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="90913-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="90913-111">Definición</span><span class="sxs-lookup"><span data-stu-id="90913-111">Definition</span></span>

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="90913-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="90913-112">Elements and attributes</span></span>

<span data-ttu-id="90913-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="90913-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="90913-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90913-114">Child elements</span></span>

|<span data-ttu-id="90913-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="90913-115">**Element**</span></span>|<span data-ttu-id="90913-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="90913-116">**Type**</span></span>|<span data-ttu-id="90913-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90913-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="90913-118">actual</span><span class="sxs-lookup"><span data-stu-id="90913-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="90913-119">currentType</span><span class="sxs-lookup"><span data-stu-id="90913-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="90913-120">Especifica las condiciones del tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="90913-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="90913-121">previsión</span><span class="sxs-lookup"><span data-stu-id="90913-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="90913-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="90913-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="90913-123">Especifica las condiciones de meteorología futuras de al menos tres días con antelación incluido hoy: hoy, mañana, dos días.</span><span class="sxs-lookup"><span data-stu-id="90913-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="90913-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="90913-124">Attributes</span></span>

|<span data-ttu-id="90913-125">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="90913-125">**Attribute**</span></span>|<span data-ttu-id="90913-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="90913-126">**Type**</span></span>|<span data-ttu-id="90913-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="90913-127">**Required**</span></span>|<span data-ttu-id="90913-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90913-128">**Description**</span></span>|<span data-ttu-id="90913-129">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="90913-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="90913-130">atribución</span><span class="sxs-lookup"><span data-stu-id="90913-130">attribution</span></span>  <br/> |<span data-ttu-id="90913-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="90913-131">xs:string</span></span>  <br/> |<span data-ttu-id="90913-132">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-132">required</span></span>  <br/> |<span data-ttu-id="90913-133">Especifica el origen de la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="90913-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="90913-134">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="90913-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="90913-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="90913-135">degreetype</span></span>  <br/> |<span data-ttu-id="90913-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="90913-136">xs:string</span></span>  <br/> |<span data-ttu-id="90913-137">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-137">required</span></span>  <br/> |<span data-ttu-id="90913-138">Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="90913-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="90913-139">C, F</span><span class="sxs-lookup"><span data-stu-id="90913-139">C, F</span></span>  <br/> |
|<span data-ttu-id="90913-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="90913-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="90913-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="90913-141">xs:string</span></span>  <br/> |<span data-ttu-id="90913-142">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-142">required</span></span>  <br/> |<span data-ttu-id="90913-143">Especifica la dirección URL de la imagen de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="90913-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="90913-144">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="90913-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="90913-145">zona horaria</span><span class="sxs-lookup"><span data-stu-id="90913-145">timezone</span></span>  <br/> |<span data-ttu-id="90913-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="90913-146">xs:integer</span></span>  <br/> |<span data-ttu-id="90913-147">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-147">required</span></span>  <br/> |<span data-ttu-id="90913-148">Especifica el desplazamiento de GMT.</span><span class="sxs-lookup"><span data-stu-id="90913-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="90913-149">Un valor comprendido entre -11 y 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="90913-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="90913-150">url</span><span class="sxs-lookup"><span data-stu-id="90913-150">url</span></span>  <br/> |<span data-ttu-id="90913-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="90913-151">xs:string</span></span>  <br/> |<span data-ttu-id="90913-152">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-152">required</span></span>  <br/> |<span data-ttu-id="90913-153">Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="90913-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="90913-154">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="90913-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="90913-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="90913-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="90913-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="90913-156">xs:string</span></span>  <br/> |<span data-ttu-id="90913-157">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-157">required</span></span>  <br/> |<span data-ttu-id="90913-158">Especifica el código que está asociado con la ubicación que se usa para distinguir múltiples ubicación que tienen el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="90913-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="90913-159">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="90913-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="90913-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="90913-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="90913-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="90913-161">xs:string</span></span>  <br/> |<span data-ttu-id="90913-162">necesario</span><span class="sxs-lookup"><span data-stu-id="90913-162">required</span></span>  <br/> |<span data-ttu-id="90913-163">Especifica el nombre de la ubicación que aparece en el control de lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="90913-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="90913-164">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="90913-164">A value of the type xs:string</span></span>  <br/> |
   

