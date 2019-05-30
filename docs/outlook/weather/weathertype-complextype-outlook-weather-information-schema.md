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
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542950"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="7d330-103">weatherType complexType (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="7d330-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="7d330-104">Especifica las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="7d330-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="7d330-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="7d330-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d330-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7d330-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="7d330-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7d330-107">**Schema file**</span></span> <br/> |<span data-ttu-id="7d330-108">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="7d330-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="7d330-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="7d330-109">**Extension base**</span></span> <br/> |<span data-ttu-id="7d330-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7d330-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d330-111">Definición</span><span class="sxs-lookup"><span data-stu-id="7d330-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7d330-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7d330-112">Elements and attributes</span></span>

<span data-ttu-id="7d330-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7d330-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d330-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d330-114">Child elements</span></span>

|<span data-ttu-id="7d330-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d330-115">**Element**</span></span>|<span data-ttu-id="7d330-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d330-116">**Type**</span></span>|<span data-ttu-id="7d330-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d330-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d330-118">recientes</span><span class="sxs-lookup"><span data-stu-id="7d330-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="7d330-119">currentType</span><span class="sxs-lookup"><span data-stu-id="7d330-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="7d330-120">Especifica las condiciones meteorológicas actuales.</span><span class="sxs-lookup"><span data-stu-id="7d330-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="7d330-121">ID</span><span class="sxs-lookup"><span data-stu-id="7d330-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="7d330-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="7d330-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="7d330-123">Especifica las condiciones meteorológicas futuras de al menos tres días de anticipación, como hoy: hoy, mañana, día después de mañana.</span><span class="sxs-lookup"><span data-stu-id="7d330-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7d330-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d330-124">Attributes</span></span>

|<span data-ttu-id="7d330-125">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7d330-125">**Attribute**</span></span>|<span data-ttu-id="7d330-126">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d330-126">**Type**</span></span>|<span data-ttu-id="7d330-127">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7d330-127">**Required**</span></span>|<span data-ttu-id="7d330-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d330-128">**Description**</span></span>|<span data-ttu-id="7d330-129">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7d330-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d330-130">atribución</span><span class="sxs-lookup"><span data-stu-id="7d330-130">attribution</span></span>  <br/> |<span data-ttu-id="7d330-131">XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-131">xs:string</span></span>  <br/> |<span data-ttu-id="7d330-132">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-132">required</span></span>  <br/> |<span data-ttu-id="7d330-133">Especifica el origen de la información meteorológica.</span><span class="sxs-lookup"><span data-stu-id="7d330-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="7d330-134">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7d330-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="7d330-135">degreetype</span></span>  <br/> |<span data-ttu-id="7d330-136">XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-136">xs:string</span></span>  <br/> |<span data-ttu-id="7d330-137">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-137">required</span></span>  <br/> |<span data-ttu-id="7d330-138">Especifica la unidad para la temperatura de la ubicación, por ejemplo, Celsius.</span><span class="sxs-lookup"><span data-stu-id="7d330-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="7d330-139">C, F</span><span class="sxs-lookup"><span data-stu-id="7d330-139">C, F</span></span>  <br/> |
|<span data-ttu-id="7d330-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="7d330-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="7d330-141">XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-141">xs:string</span></span>  <br/> |<span data-ttu-id="7d330-142">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-142">required</span></span>  <br/> |<span data-ttu-id="7d330-143">Especifica la dirección URL de la imagen para la ubicación.</span><span class="sxs-lookup"><span data-stu-id="7d330-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="7d330-144">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7d330-145">TimeZone</span><span class="sxs-lookup"><span data-stu-id="7d330-145">timezone</span></span>  <br/> |<span data-ttu-id="7d330-146">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="7d330-146">xs:integer</span></span>  <br/> |<span data-ttu-id="7d330-147">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-147">required</span></span>  <br/> |<span data-ttu-id="7d330-148">Especifica el desplazamiento GMT.</span><span class="sxs-lookup"><span data-stu-id="7d330-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="7d330-149">Un valor comprendido entre-11 y 12 inclusive</span><span class="sxs-lookup"><span data-stu-id="7d330-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="7d330-150">url</span><span class="sxs-lookup"><span data-stu-id="7d330-150">url</span></span>  <br/> |<span data-ttu-id="7d330-151">XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-151">xs:string</span></span>  <br/> |<span data-ttu-id="7d330-152">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-152">required</span></span>  <br/> |<span data-ttu-id="7d330-153">Especifica la dirección URL de la página web del servicio meteorológico que contiene información meteorológica para la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="7d330-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="7d330-154">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7d330-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="7d330-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="7d330-156">XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-156">xs:string</span></span>  <br/> |<span data-ttu-id="7d330-157">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-157">required</span></span>  <br/> |<span data-ttu-id="7d330-158">Especifica el código que está asociado con la ubicación que se usa para distinguir varias ubicaciones que tienen el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="7d330-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="7d330-159">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7d330-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="7d330-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="7d330-161">XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-161">xs:string</span></span>  <br/> |<span data-ttu-id="7d330-162">necesario</span><span class="sxs-lookup"><span data-stu-id="7d330-162">required</span></span>  <br/> |<span data-ttu-id="7d330-163">Especifica el nombre de la ubicación que aparece en el control desplegable.</span><span class="sxs-lookup"><span data-stu-id="7d330-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="7d330-164">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="7d330-164">A value of the type xs:string</span></span>  <br/> |
   

