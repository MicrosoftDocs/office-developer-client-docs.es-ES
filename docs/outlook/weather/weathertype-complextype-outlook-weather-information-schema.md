---
title: weatherType complexType (esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Especifica las condiciones meteorológicas de una ubicación.
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355044"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="fbbd9-103">weatherType complexType (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="fbbd9-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="fbbd9-104">Especifica las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="fbbd9-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="fbbd9-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbbd9-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="fbbd9-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-107">**Schema file**</span></span> <br/> |<span data-ttu-id="fbbd9-108">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="fbbd9-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="fbbd9-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-109">**Extension base**</span></span> <br/> |<span data-ttu-id="fbbd9-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fbbd9-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fbbd9-111">Definición</span><span class="sxs-lookup"><span data-stu-id="fbbd9-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fbbd9-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fbbd9-112">Elements and attributes</span></span>

<span data-ttu-id="fbbd9-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fbbd9-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fbbd9-114">Child elements</span></span>

|<span data-ttu-id="fbbd9-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-115">**Element**</span></span>|<span data-ttu-id="fbbd9-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-116">**Type**</span></span>|<span data-ttu-id="fbbd9-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbbd9-118">recientes</span><span class="sxs-lookup"><span data-stu-id="fbbd9-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="fbbd9-119">currentType</span><span class="sxs-lookup"><span data-stu-id="fbbd9-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="fbbd9-120">Especifica las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="fbbd9-121">ID</span><span class="sxs-lookup"><span data-stu-id="fbbd9-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="fbbd9-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="fbbd9-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="fbbd9-123">Especifica las condiciones meteorológicas futuras de al menos tres días de anticipación, como hoy: hoy, mañana, día después de mañana.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fbbd9-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbbd9-124">Attributes</span></span>

|<span data-ttu-id="fbbd9-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-125">**Attribute**</span></span>|<span data-ttu-id="fbbd9-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-126">**Type**</span></span>|<span data-ttu-id="fbbd9-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-127">**Required**</span></span>|<span data-ttu-id="fbbd9-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-128">**Description**</span></span>|<span data-ttu-id="fbbd9-129">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="fbbd9-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fbbd9-130">atribución</span><span class="sxs-lookup"><span data-stu-id="fbbd9-130">attribution</span></span>  <br/> |<span data-ttu-id="fbbd9-131">XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-131">xs:string</span></span>  <br/> |<span data-ttu-id="fbbd9-132">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-132">required</span></span>  <br/> |<span data-ttu-id="fbbd9-133">Especifica el origen de la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="fbbd9-134">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="fbbd9-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="fbbd9-135">degreetype</span></span>  <br/> |<span data-ttu-id="fbbd9-136">XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-136">xs:string</span></span>  <br/> |<span data-ttu-id="fbbd9-137">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-137">required</span></span>  <br/> |<span data-ttu-id="fbbd9-138">Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="fbbd9-139">C, F</span><span class="sxs-lookup"><span data-stu-id="fbbd9-139">C, F</span></span>  <br/> |
|<span data-ttu-id="fbbd9-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="fbbd9-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="fbbd9-141">XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-141">xs:string</span></span>  <br/> |<span data-ttu-id="fbbd9-142">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-142">required</span></span>  <br/> |<span data-ttu-id="fbbd9-143">Especifica la dirección URL de la imagen para la ubicación.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="fbbd9-144">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="fbbd9-145">TimeZone</span><span class="sxs-lookup"><span data-stu-id="fbbd9-145">timezone</span></span>  <br/> |<span data-ttu-id="fbbd9-146">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="fbbd9-146">xs:integer</span></span>  <br/> |<span data-ttu-id="fbbd9-147">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-147">required</span></span>  <br/> |<span data-ttu-id="fbbd9-148">Especifica el desplazamiento GMT.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="fbbd9-149">Un valor comprendido entre-11 y 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="fbbd9-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="fbbd9-150">url</span><span class="sxs-lookup"><span data-stu-id="fbbd9-150">url</span></span>  <br/> |<span data-ttu-id="fbbd9-151">XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-151">xs:string</span></span>  <br/> |<span data-ttu-id="fbbd9-152">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-152">required</span></span>  <br/> |<span data-ttu-id="fbbd9-153">Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="fbbd9-154">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="fbbd9-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="fbbd9-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="fbbd9-156">XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-156">xs:string</span></span>  <br/> |<span data-ttu-id="fbbd9-157">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-157">required</span></span>  <br/> |<span data-ttu-id="fbbd9-158">Especifica el código que está asociado con la ubicación que se usa para distinguir varias ubicaciones que tienen el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="fbbd9-159">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="fbbd9-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="fbbd9-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="fbbd9-161">XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-161">xs:string</span></span>  <br/> |<span data-ttu-id="fbbd9-162">necesario</span><span class="sxs-lookup"><span data-stu-id="fbbd9-162">required</span></span>  <br/> |<span data-ttu-id="fbbd9-163">Especifica el nombre de la ubicación que aparece en el control desplegable.</span><span class="sxs-lookup"><span data-stu-id="fbbd9-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="fbbd9-164">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="fbbd9-164">A value of the type xs:string</span></span>  <br/> |
   

