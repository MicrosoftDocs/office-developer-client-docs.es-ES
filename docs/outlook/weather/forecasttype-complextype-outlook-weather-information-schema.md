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
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821222"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="4aa44-103">forecastType complexType (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="4aa44-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="4aa44-104">Define los parámetros acerca de las condiciones de previsión meteorológica de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="4aa44-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="4aa44-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="4aa44-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4aa44-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4aa44-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="4aa44-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4aa44-107">**Schema file**</span></span> <br/> |<span data-ttu-id="4aa44-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="4aa44-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="4aa44-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="4aa44-109">**Extension base**</span></span> <br/> |<span data-ttu-id="4aa44-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4aa44-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4aa44-111">Definición</span><span class="sxs-lookup"><span data-stu-id="4aa44-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4aa44-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4aa44-112">Elements and attributes</span></span>

<span data-ttu-id="4aa44-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="4aa44-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4aa44-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4aa44-114">Child elements</span></span>

<span data-ttu-id="4aa44-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4aa44-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4aa44-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="4aa44-116">Attributes</span></span>

|<span data-ttu-id="4aa44-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4aa44-117">**Attribute**</span></span>|<span data-ttu-id="4aa44-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4aa44-118">**Type**</span></span>|<span data-ttu-id="4aa44-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4aa44-119">**Required**</span></span>|<span data-ttu-id="4aa44-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4aa44-120">**Description**</span></span>|<span data-ttu-id="4aa44-121">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="4aa44-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4aa44-122">date</span><span class="sxs-lookup"><span data-stu-id="4aa44-122">date</span></span>  <br/> |<span data-ttu-id="4aa44-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="4aa44-123">xs:date</span></span>  <br/> |<span data-ttu-id="4aa44-124">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-124">required</span></span>  <br/> |<span data-ttu-id="4aa44-125">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="4aa44-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="4aa44-126">Un valor de tipo de xs: Date</span><span class="sxs-lookup"><span data-stu-id="4aa44-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="4aa44-127">día</span><span class="sxs-lookup"><span data-stu-id="4aa44-127">day</span></span>  <br/> |<span data-ttu-id="4aa44-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4aa44-128">xs:string</span></span>  <br/> |<span data-ttu-id="4aa44-129">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-129">required</span></span>  <br/> |<span data-ttu-id="4aa44-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="4aa44-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="4aa44-131">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="4aa44-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4aa44-132">alta</span><span class="sxs-lookup"><span data-stu-id="4aa44-132">high</span></span>  <br/> |<span data-ttu-id="4aa44-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-133">xs:integer</span></span>  <br/> |<span data-ttu-id="4aa44-134">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-134">required</span></span>  <br/> |<span data-ttu-id="4aa44-135">Especifica la temperatura máxima prevista.</span><span class="sxs-lookup"><span data-stu-id="4aa44-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="4aa44-136">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4aa44-137">baja</span><span class="sxs-lookup"><span data-stu-id="4aa44-137">low</span></span>  <br/> |<span data-ttu-id="4aa44-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-138">xs:integer</span></span>  <br/> |<span data-ttu-id="4aa44-139">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-139">required</span></span>  <br/> |<span data-ttu-id="4aa44-140">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="4aa44-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="4aa44-141">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4aa44-142">precip</span><span class="sxs-lookup"><span data-stu-id="4aa44-142">precip</span></span>  <br/> |<span data-ttu-id="4aa44-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-143">xs:integer</span></span>  <br/> |<span data-ttu-id="4aa44-144">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-144">required</span></span>  <br/> |<span data-ttu-id="4aa44-145">Especifica la posibilidad de porcentaje de precipitación.</span><span class="sxs-lookup"><span data-stu-id="4aa44-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="4aa44-146">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4aa44-147">shortday</span><span class="sxs-lookup"><span data-stu-id="4aa44-147">shortday</span></span>  <br/> |<span data-ttu-id="4aa44-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="4aa44-148">xs:string</span></span>  <br/> |<span data-ttu-id="4aa44-149">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-149">required</span></span>  <br/> |<span data-ttu-id="4aa44-150">Especifica un día de forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="4aa44-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="4aa44-151">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="4aa44-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4aa44-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="4aa44-152">skycodeday</span></span>  <br/> |<span data-ttu-id="4aa44-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-153">xs:integer</span></span>  <br/> |<span data-ttu-id="4aa44-154">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-154">required</span></span>  <br/> |<span data-ttu-id="4aa44-155">Especifica un código de las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="4aa44-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="4aa44-156">Un valor del tipo xs: Integer</span><span class="sxs-lookup"><span data-stu-id="4aa44-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4aa44-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="4aa44-157">skytextday</span></span>  <br/> |<span data-ttu-id="4aa44-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="4aa44-158">xs:string</span></span>  <br/> |<span data-ttu-id="4aa44-159">necesario</span><span class="sxs-lookup"><span data-stu-id="4aa44-159">required</span></span>  <br/> |<span data-ttu-id="4aa44-160">Especifica una o dos palabras que describen las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="4aa44-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="4aa44-161">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="4aa44-161">A value of the type xs:string</span></span>  <br/> |
   

