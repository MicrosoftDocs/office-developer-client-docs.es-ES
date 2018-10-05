---
title: forecastType complexType (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Define los parámetros acerca de las condiciones de previsión meteorológica de una ubicación.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390628"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="06316-103">forecastType complexType (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="06316-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="06316-104">Define los parámetros acerca de las condiciones de previsión meteorológica de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="06316-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="06316-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="06316-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06316-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="06316-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="06316-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="06316-107">**Schema file**</span></span> <br/> |<span data-ttu-id="06316-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="06316-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="06316-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="06316-109">**Extension base**</span></span> <br/> |<span data-ttu-id="06316-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="06316-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06316-111">Definición</span><span class="sxs-lookup"><span data-stu-id="06316-111">Definition</span></span>

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="06316-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="06316-112">Elements and attributes</span></span>

<span data-ttu-id="06316-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="06316-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="06316-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06316-114">Child elements</span></span>

<span data-ttu-id="06316-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="06316-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06316-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="06316-116">Attributes</span></span>

|<span data-ttu-id="06316-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="06316-117">**Attribute**</span></span>|<span data-ttu-id="06316-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06316-118">**Type**</span></span>|<span data-ttu-id="06316-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="06316-119">**Required**</span></span>|<span data-ttu-id="06316-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06316-120">**Description**</span></span>|<span data-ttu-id="06316-121">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="06316-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="06316-122">date</span><span class="sxs-lookup"><span data-stu-id="06316-122">date</span></span>  <br/> |<span data-ttu-id="06316-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="06316-123">xs:date</span></span>  <br/> |<span data-ttu-id="06316-124">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-124">required</span></span>  <br/> |<span data-ttu-id="06316-125">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="06316-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="06316-126">Un valor de tipo de xs: Date</span><span class="sxs-lookup"><span data-stu-id="06316-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="06316-127">día</span><span class="sxs-lookup"><span data-stu-id="06316-127">day</span></span>  <br/> |<span data-ttu-id="06316-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="06316-128">xs:string</span></span>  <br/> |<span data-ttu-id="06316-129">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-129">required</span></span>  <br/> |<span data-ttu-id="06316-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="06316-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="06316-131">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="06316-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="06316-132">alta</span><span class="sxs-lookup"><span data-stu-id="06316-132">high</span></span>  <br/> |<span data-ttu-id="06316-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06316-133">xs:integer</span></span>  <br/> |<span data-ttu-id="06316-134">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-134">required</span></span>  <br/> |<span data-ttu-id="06316-135">Especifica la temperatura máxima prevista.</span><span class="sxs-lookup"><span data-stu-id="06316-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="06316-136">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="06316-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06316-137">baja</span><span class="sxs-lookup"><span data-stu-id="06316-137">low</span></span>  <br/> |<span data-ttu-id="06316-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06316-138">xs:integer</span></span>  <br/> |<span data-ttu-id="06316-139">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-139">required</span></span>  <br/> |<span data-ttu-id="06316-140">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="06316-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="06316-141">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="06316-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06316-142">precip</span><span class="sxs-lookup"><span data-stu-id="06316-142">precip</span></span>  <br/> |<span data-ttu-id="06316-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06316-143">xs:integer</span></span>  <br/> |<span data-ttu-id="06316-144">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-144">required</span></span>  <br/> |<span data-ttu-id="06316-145">Especifica la posibilidad de porcentaje de precipitación.</span><span class="sxs-lookup"><span data-stu-id="06316-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="06316-146">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="06316-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06316-147">shortday</span><span class="sxs-lookup"><span data-stu-id="06316-147">shortday</span></span>  <br/> |<span data-ttu-id="06316-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="06316-148">xs:string</span></span>  <br/> |<span data-ttu-id="06316-149">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-149">required</span></span>  <br/> |<span data-ttu-id="06316-150">Especifica un día de forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="06316-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="06316-151">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="06316-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="06316-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="06316-152">skycodeday</span></span>  <br/> |<span data-ttu-id="06316-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="06316-153">xs:integer</span></span>  <br/> |<span data-ttu-id="06316-154">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-154">required</span></span>  <br/> |<span data-ttu-id="06316-155">Especifica un código de las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="06316-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="06316-156">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="06316-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06316-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="06316-157">skytextday</span></span>  <br/> |<span data-ttu-id="06316-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="06316-158">xs:string</span></span>  <br/> |<span data-ttu-id="06316-159">necesario</span><span class="sxs-lookup"><span data-stu-id="06316-159">required</span></span>  <br/> |<span data-ttu-id="06316-160">Especifica una o dos palabras que describen las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="06316-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="06316-161">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="06316-161">A value of the type xs:string</span></span>  <br/> |
   

