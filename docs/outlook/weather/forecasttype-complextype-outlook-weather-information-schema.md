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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361148"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="ab2c2-103">forecastType complexType (esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="ab2c2-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="ab2c2-104">Define los parámetros sobre las condiciones meteorológicas de previsión de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="ab2c2-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ab2c2-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab2c2-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="ab2c2-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-107">**Schema file**</span></span> <br/> |<span data-ttu-id="ab2c2-108">getweatherinfo. xsd</span><span class="sxs-lookup"><span data-stu-id="ab2c2-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="ab2c2-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-109">**Extension base**</span></span> <br/> |<span data-ttu-id="ab2c2-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ab2c2-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab2c2-111">Definición</span><span class="sxs-lookup"><span data-stu-id="ab2c2-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ab2c2-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ab2c2-112">Elements and attributes</span></span>

<span data-ttu-id="ab2c2-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ab2c2-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab2c2-114">Child elements</span></span>

<span data-ttu-id="ab2c2-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab2c2-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab2c2-116">Attributes</span></span>

|<span data-ttu-id="ab2c2-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-117">**Attribute**</span></span>|<span data-ttu-id="ab2c2-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-118">**Type**</span></span>|<span data-ttu-id="ab2c2-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-119">**Required**</span></span>|<span data-ttu-id="ab2c2-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-120">**Description**</span></span>|<span data-ttu-id="ab2c2-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="ab2c2-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab2c2-122">fecha</span><span class="sxs-lookup"><span data-stu-id="ab2c2-122">date</span></span>  <br/> |<span data-ttu-id="ab2c2-123">XS: Date</span><span class="sxs-lookup"><span data-stu-id="ab2c2-123">xs:date</span></span>  <br/> |<span data-ttu-id="ab2c2-124">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-124">required</span></span>  <br/> |<span data-ttu-id="ab2c2-125">Especifica la fecha de la previsión.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="ab2c2-126">Un valor de tipo XS: Date</span><span class="sxs-lookup"><span data-stu-id="ab2c2-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="ab2c2-127">cotidiano</span><span class="sxs-lookup"><span data-stu-id="ab2c2-127">day</span></span>  <br/> |<span data-ttu-id="ab2c2-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="ab2c2-128">xs:string</span></span>  <br/> |<span data-ttu-id="ab2c2-129">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-129">required</span></span>  <br/> |<span data-ttu-id="ab2c2-130">Especifica un día para la previsión.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="ab2c2-131">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ab2c2-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ab2c2-132">mayor</span><span class="sxs-lookup"><span data-stu-id="ab2c2-132">high</span></span>  <br/> |<span data-ttu-id="ab2c2-133">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-133">xs:integer</span></span>  <br/> |<span data-ttu-id="ab2c2-134">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-134">required</span></span>  <br/> |<span data-ttu-id="ab2c2-135">Especifica la temperatura más alta prevista.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="ab2c2-136">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ab2c2-137">baja</span><span class="sxs-lookup"><span data-stu-id="ab2c2-137">low</span></span>  <br/> |<span data-ttu-id="ab2c2-138">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-138">xs:integer</span></span>  <br/> |<span data-ttu-id="ab2c2-139">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-139">required</span></span>  <br/> |<span data-ttu-id="ab2c2-140">Especifica la temperatura más baja prevista.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="ab2c2-141">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ab2c2-142">Precip</span><span class="sxs-lookup"><span data-stu-id="ab2c2-142">precip</span></span>  <br/> |<span data-ttu-id="ab2c2-143">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-143">xs:integer</span></span>  <br/> |<span data-ttu-id="ab2c2-144">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-144">required</span></span>  <br/> |<span data-ttu-id="ab2c2-145">Especifica el porcentaje de probabilidad de precipitación.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="ab2c2-146">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ab2c2-147">shortday</span><span class="sxs-lookup"><span data-stu-id="ab2c2-147">shortday</span></span>  <br/> |<span data-ttu-id="ab2c2-148">XS: String</span><span class="sxs-lookup"><span data-stu-id="ab2c2-148">xs:string</span></span>  <br/> |<span data-ttu-id="ab2c2-149">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-149">required</span></span>  <br/> |<span data-ttu-id="ab2c2-150">Especifica un día en forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="ab2c2-151">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ab2c2-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ab2c2-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="ab2c2-152">skycodeday</span></span>  <br/> |<span data-ttu-id="ab2c2-153">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-153">xs:integer</span></span>  <br/> |<span data-ttu-id="ab2c2-154">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-154">required</span></span>  <br/> |<span data-ttu-id="ab2c2-155">Especifica un código para las condiciones de previsión.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="ab2c2-156">Un valor del tipo XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ab2c2-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="ab2c2-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="ab2c2-157">skytextday</span></span>  <br/> |<span data-ttu-id="ab2c2-158">XS: String</span><span class="sxs-lookup"><span data-stu-id="ab2c2-158">xs:string</span></span>  <br/> |<span data-ttu-id="ab2c2-159">necesario</span><span class="sxs-lookup"><span data-stu-id="ab2c2-159">required</span></span>  <br/> |<span data-ttu-id="ab2c2-160">Especifica de una a dos palabras que describen las condiciones de previsión.</span><span class="sxs-lookup"><span data-stu-id="ab2c2-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="ab2c2-161">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="ab2c2-161">A value of the type xs:string</span></span>  <br/> |
   

