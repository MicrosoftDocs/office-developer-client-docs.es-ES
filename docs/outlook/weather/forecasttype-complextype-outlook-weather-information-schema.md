---
title: forecastType complexType (esquema de información meteorológica de Outlook)
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
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="d7db3-103">forecastType complexType (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="d7db3-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d7db3-104">Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="d7db3-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="d7db3-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d7db3-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7db3-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d7db3-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d7db3-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d7db3-107">**Schema file**</span></span> <br/> |<span data-ttu-id="d7db3-108">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="d7db3-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="d7db3-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d7db3-109">**Extension base**</span></span> <br/> |<span data-ttu-id="d7db3-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d7db3-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7db3-111">Definición</span><span class="sxs-lookup"><span data-stu-id="d7db3-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d7db3-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d7db3-112">Elements and attributes</span></span>

<span data-ttu-id="d7db3-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d7db3-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d7db3-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7db3-114">Child elements</span></span>

<span data-ttu-id="d7db3-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d7db3-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7db3-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7db3-116">Attributes</span></span>

|<span data-ttu-id="d7db3-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d7db3-117">**Attribute**</span></span>|<span data-ttu-id="d7db3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d7db3-118">**Type**</span></span>|<span data-ttu-id="d7db3-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d7db3-119">**Required**</span></span>|<span data-ttu-id="d7db3-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7db3-120">**Description**</span></span>|<span data-ttu-id="d7db3-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="d7db3-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7db3-122">date</span><span class="sxs-lookup"><span data-stu-id="d7db3-122">date</span></span>  <br/> |<span data-ttu-id="d7db3-123">XS: Date</span><span class="sxs-lookup"><span data-stu-id="d7db3-123">xs:date</span></span>  <br/> |<span data-ttu-id="d7db3-124">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-124">required</span></span>  <br/> |<span data-ttu-id="d7db3-125">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="d7db3-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="d7db3-126">Un valor de tipo XS: Date</span><span class="sxs-lookup"><span data-stu-id="d7db3-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="d7db3-127">cotidiano</span><span class="sxs-lookup"><span data-stu-id="d7db3-127">day</span></span>  <br/> |<span data-ttu-id="d7db3-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="d7db3-128">xs:string</span></span>  <br/> |<span data-ttu-id="d7db3-129">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-129">required</span></span>  <br/> |<span data-ttu-id="d7db3-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="d7db3-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="d7db3-131">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="d7db3-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d7db3-132">mayor</span><span class="sxs-lookup"><span data-stu-id="d7db3-132">high</span></span>  <br/> |<span data-ttu-id="d7db3-133">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-133">xs:integer</span></span>  <br/> |<span data-ttu-id="d7db3-134">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-134">required</span></span>  <br/> |<span data-ttu-id="d7db3-135">Especifica la temperatura más alta prevista.</span><span class="sxs-lookup"><span data-stu-id="d7db3-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="d7db3-136">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d7db3-137">baja</span><span class="sxs-lookup"><span data-stu-id="d7db3-137">low</span></span>  <br/> |<span data-ttu-id="d7db3-138">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-138">xs:integer</span></span>  <br/> |<span data-ttu-id="d7db3-139">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-139">required</span></span>  <br/> |<span data-ttu-id="d7db3-140">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="d7db3-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="d7db3-141">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d7db3-142">precip</span><span class="sxs-lookup"><span data-stu-id="d7db3-142">precip</span></span>  <br/> |<span data-ttu-id="d7db3-143">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-143">xs:integer</span></span>  <br/> |<span data-ttu-id="d7db3-144">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-144">required</span></span>  <br/> |<span data-ttu-id="d7db3-145">Especifica el porcentaje de probabilidad de precipitación.</span><span class="sxs-lookup"><span data-stu-id="d7db3-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="d7db3-146">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d7db3-147">shortday</span><span class="sxs-lookup"><span data-stu-id="d7db3-147">shortday</span></span>  <br/> |<span data-ttu-id="d7db3-148">XS: String</span><span class="sxs-lookup"><span data-stu-id="d7db3-148">xs:string</span></span>  <br/> |<span data-ttu-id="d7db3-149">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-149">required</span></span>  <br/> |<span data-ttu-id="d7db3-150">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="d7db3-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="d7db3-151">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="d7db3-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d7db3-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="d7db3-152">skycodeday</span></span>  <br/> |<span data-ttu-id="d7db3-153">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-153">xs:integer</span></span>  <br/> |<span data-ttu-id="d7db3-154">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-154">required</span></span>  <br/> |<span data-ttu-id="d7db3-155">Especifica un código para las condiciones de previsión.</span><span class="sxs-lookup"><span data-stu-id="d7db3-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="d7db3-156">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d7db3-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d7db3-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="d7db3-157">skytextday</span></span>  <br/> |<span data-ttu-id="d7db3-158">XS: String</span><span class="sxs-lookup"><span data-stu-id="d7db3-158">xs:string</span></span>  <br/> |<span data-ttu-id="d7db3-159">necesario</span><span class="sxs-lookup"><span data-stu-id="d7db3-159">required</span></span>  <br/> |<span data-ttu-id="d7db3-160">Especifica de una a dos palabras que describen las condiciones de previsión.</span><span class="sxs-lookup"><span data-stu-id="d7db3-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="d7db3-161">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="d7db3-161">A value of the type xs:string</span></span>  <br/> |
   

