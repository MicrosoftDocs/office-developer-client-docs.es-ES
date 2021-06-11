---
title: forecastType complexType (Outlook de información meteorológica)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540955"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="2f7af-103">forecastType complexType (Outlook de información meteorológica)</span><span class="sxs-lookup"><span data-stu-id="2f7af-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="2f7af-104">Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="2f7af-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="2f7af-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2f7af-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f7af-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2f7af-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="2f7af-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2f7af-107">**Schema file**</span></span> <br/> |<span data-ttu-id="2f7af-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="2f7af-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="2f7af-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2f7af-109">**Extension base**</span></span> <br/> |<span data-ttu-id="2f7af-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2f7af-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f7af-111">Definición</span><span class="sxs-lookup"><span data-stu-id="2f7af-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2f7af-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2f7af-112">Elements and attributes</span></span>

<span data-ttu-id="2f7af-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2f7af-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2f7af-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f7af-114">Child elements</span></span>

<span data-ttu-id="2f7af-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f7af-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f7af-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f7af-116">Attributes</span></span>

|<span data-ttu-id="2f7af-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2f7af-117">**Attribute**</span></span>|<span data-ttu-id="2f7af-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2f7af-118">**Type**</span></span>|<span data-ttu-id="2f7af-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2f7af-119">**Required**</span></span>|<span data-ttu-id="2f7af-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f7af-120">**Description**</span></span>|<span data-ttu-id="2f7af-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="2f7af-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2f7af-122">date</span><span class="sxs-lookup"><span data-stu-id="2f7af-122">date</span></span>  <br/> |<span data-ttu-id="2f7af-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="2f7af-123">xs:date</span></span>  <br/> |<span data-ttu-id="2f7af-124">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-124">required</span></span>  <br/> |<span data-ttu-id="2f7af-125">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="2f7af-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="2f7af-126">Valor del tipo xs:date</span><span class="sxs-lookup"><span data-stu-id="2f7af-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="2f7af-127">día</span><span class="sxs-lookup"><span data-stu-id="2f7af-127">day</span></span>  <br/> |<span data-ttu-id="2f7af-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="2f7af-128">xs:string</span></span>  <br/> |<span data-ttu-id="2f7af-129">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-129">required</span></span>  <br/> |<span data-ttu-id="2f7af-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="2f7af-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="2f7af-131">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="2f7af-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2f7af-132">high</span><span class="sxs-lookup"><span data-stu-id="2f7af-132">high</span></span>  <br/> |<span data-ttu-id="2f7af-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-133">xs:integer</span></span>  <br/> |<span data-ttu-id="2f7af-134">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-134">required</span></span>  <br/> |<span data-ttu-id="2f7af-135">Especifica la temperatura más alta prevista.</span><span class="sxs-lookup"><span data-stu-id="2f7af-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="2f7af-136">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2f7af-137">low</span><span class="sxs-lookup"><span data-stu-id="2f7af-137">low</span></span>  <br/> |<span data-ttu-id="2f7af-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-138">xs:integer</span></span>  <br/> |<span data-ttu-id="2f7af-139">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-139">required</span></span>  <br/> |<span data-ttu-id="2f7af-140">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="2f7af-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="2f7af-141">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2f7af-142">precip</span><span class="sxs-lookup"><span data-stu-id="2f7af-142">precip</span></span>  <br/> |<span data-ttu-id="2f7af-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-143">xs:integer</span></span>  <br/> |<span data-ttu-id="2f7af-144">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-144">required</span></span>  <br/> |<span data-ttu-id="2f7af-145">Especifica el porcentaje de posibilidad de precipitación.</span><span class="sxs-lookup"><span data-stu-id="2f7af-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="2f7af-146">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2f7af-147">shortday</span><span class="sxs-lookup"><span data-stu-id="2f7af-147">shortday</span></span>  <br/> |<span data-ttu-id="2f7af-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="2f7af-148">xs:string</span></span>  <br/> |<span data-ttu-id="2f7af-149">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-149">required</span></span>  <br/> |<span data-ttu-id="2f7af-150">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="2f7af-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="2f7af-151">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="2f7af-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2f7af-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="2f7af-152">skycodeday</span></span>  <br/> |<span data-ttu-id="2f7af-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-153">xs:integer</span></span>  <br/> |<span data-ttu-id="2f7af-154">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-154">required</span></span>  <br/> |<span data-ttu-id="2f7af-155">Especifica un código para las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="2f7af-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2f7af-156">Valor del tipo xs:integer</span><span class="sxs-lookup"><span data-stu-id="2f7af-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2f7af-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="2f7af-157">skytextday</span></span>  <br/> |<span data-ttu-id="2f7af-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="2f7af-158">xs:string</span></span>  <br/> |<span data-ttu-id="2f7af-159">necesario</span><span class="sxs-lookup"><span data-stu-id="2f7af-159">required</span></span>  <br/> |<span data-ttu-id="2f7af-160">Especifica de una a dos palabras que describen las condiciones previstas.</span><span class="sxs-lookup"><span data-stu-id="2f7af-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2f7af-161">Valor del tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="2f7af-161">A value of the type xs:string</span></span>  <br/> |
   

