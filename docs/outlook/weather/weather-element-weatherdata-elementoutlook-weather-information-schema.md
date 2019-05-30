---
title: elemento Weather (elemento datos) (esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Especifica las condiciones meteorológicas de una ubicación.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541270"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="b5570-103">elemento Weather (elemento datos) (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="b5570-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="b5570-104">Especifica las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="b5570-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5570-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5570-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5570-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b5570-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5570-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="b5570-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="b5570-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5570-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="b5570-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5570-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5570-110">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="b5570-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5570-111">Definición</span><span class="sxs-lookup"><span data-stu-id="b5570-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5570-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b5570-112">Elements and attributes</span></span>

<span data-ttu-id="b5570-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b5570-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5570-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5570-114">Parent elements</span></span>

|<span data-ttu-id="b5570-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5570-115">**Element**</span></span>|<span data-ttu-id="b5570-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5570-116">**Type**</span></span>|<span data-ttu-id="b5570-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5570-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5570-118">datos</span><span class="sxs-lookup"><span data-stu-id="b5570-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="b5570-119">Define el elemento Weather.</span><span class="sxs-lookup"><span data-stu-id="b5570-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5570-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5570-120">Child elements</span></span>

|<span data-ttu-id="b5570-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b5570-121">**Element**</span></span>|<span data-ttu-id="b5570-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5570-122">**Type**</span></span>|<span data-ttu-id="b5570-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5570-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5570-124">recientes</span><span class="sxs-lookup"><span data-stu-id="b5570-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="b5570-125">currentType</span><span class="sxs-lookup"><span data-stu-id="b5570-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="b5570-126">Especifica las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="b5570-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="b5570-127">ID</span><span class="sxs-lookup"><span data-stu-id="b5570-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="b5570-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="b5570-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="b5570-129">Especifica las condiciones meteorológicas futuras de al menos tres días de anticipación, como hoy: hoy, mañana, día después de mañana.</span><span class="sxs-lookup"><span data-stu-id="b5570-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b5570-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5570-130">Attributes</span></span>

|<span data-ttu-id="b5570-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b5570-131">**Attribute**</span></span>|<span data-ttu-id="b5570-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5570-132">**Type**</span></span>|<span data-ttu-id="b5570-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b5570-133">**Required**</span></span>|<span data-ttu-id="b5570-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5570-134">**Description**</span></span>|<span data-ttu-id="b5570-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b5570-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5570-136">atribución</span><span class="sxs-lookup"><span data-stu-id="b5570-136">attribution</span></span>  <br/> |<span data-ttu-id="b5570-137">XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-137">xs:string</span></span>  <br/> |<span data-ttu-id="b5570-138">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-138">required</span></span>  <br/> |<span data-ttu-id="b5570-139">Especifica el origen de la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="b5570-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="b5570-140">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b5570-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="b5570-141">degreetype</span></span>  <br/> |<span data-ttu-id="b5570-142">XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-142">xs:string</span></span>  <br/> |<span data-ttu-id="b5570-143">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-143">required</span></span>  <br/> |<span data-ttu-id="b5570-144">Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="b5570-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="b5570-145">C, F</span><span class="sxs-lookup"><span data-stu-id="b5570-145">C, F</span></span>  <br/> |
|<span data-ttu-id="b5570-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="b5570-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="b5570-147">XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-147">xs:string</span></span>  <br/> |<span data-ttu-id="b5570-148">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-148">required</span></span>  <br/> |<span data-ttu-id="b5570-149">Especifica la dirección URL de la imagen para la ubicación.</span><span class="sxs-lookup"><span data-stu-id="b5570-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="b5570-150">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b5570-151">TimeZone</span><span class="sxs-lookup"><span data-stu-id="b5570-151">timezone</span></span>  <br/> |<span data-ttu-id="b5570-152">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="b5570-152">xs:integer</span></span>  <br/> |<span data-ttu-id="b5570-153">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-153">required</span></span>  <br/> |<span data-ttu-id="b5570-154">Especifica el desplazamiento GMT.</span><span class="sxs-lookup"><span data-stu-id="b5570-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="b5570-155">Un valor comprendido entre-11 y 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="b5570-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="b5570-156">url</span><span class="sxs-lookup"><span data-stu-id="b5570-156">url</span></span>  <br/> |<span data-ttu-id="b5570-157">XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-157">xs:string</span></span>  <br/> |<span data-ttu-id="b5570-158">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-158">required</span></span>  <br/> |<span data-ttu-id="b5570-159">Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="b5570-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="b5570-160">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b5570-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="b5570-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="b5570-162">XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-162">xs:string</span></span>  <br/> |<span data-ttu-id="b5570-163">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-163">required</span></span>  <br/> |<span data-ttu-id="b5570-164">Especifica el código que está asociado con la ubicación que se usa para distinguir varias ubicaciones que tienen el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="b5570-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="b5570-165">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b5570-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="b5570-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="b5570-167">XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-167">xs:string</span></span>  <br/> |<span data-ttu-id="b5570-168">necesario</span><span class="sxs-lookup"><span data-stu-id="b5570-168">required</span></span>  <br/> |<span data-ttu-id="b5570-169">Especifica el nombre de la ubicación que aparece en el control desplegable.</span><span class="sxs-lookup"><span data-stu-id="b5570-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="b5570-170">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="b5570-170">A value of the type xs:string</span></span>  <br/> |
   

