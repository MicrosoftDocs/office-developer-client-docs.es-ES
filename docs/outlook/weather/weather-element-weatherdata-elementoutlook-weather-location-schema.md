---
title: elemento Weather (elemento datos) (esquema de ubicación de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Especifica la ubicación en la que se va a notificar el tiempo.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355212"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="67604-103">elemento Weather (elemento datos) (esquema de ubicación de tiempo de Outlook)</span><span class="sxs-lookup"><span data-stu-id="67604-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="67604-104">Especifica la ubicación en la que se va a notificar el tiempo.</span><span class="sxs-lookup"><span data-stu-id="67604-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67604-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="67604-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67604-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="67604-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67604-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="67604-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="67604-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67604-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="67604-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67604-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67604-110">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="67604-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67604-111">Definición</span><span class="sxs-lookup"><span data-stu-id="67604-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="67604-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="67604-112">Elements and attributes</span></span>

<span data-ttu-id="67604-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="67604-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67604-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="67604-114">Parent elements</span></span>

|<span data-ttu-id="67604-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="67604-115">**Element**</span></span>|<span data-ttu-id="67604-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67604-116">**Type**</span></span>|<span data-ttu-id="67604-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67604-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67604-118">datos</span><span class="sxs-lookup"><span data-stu-id="67604-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="67604-119">Define el elemento Weather.</span><span class="sxs-lookup"><span data-stu-id="67604-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67604-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67604-120">Child elements</span></span>

<span data-ttu-id="67604-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="67604-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67604-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="67604-122">Attributes</span></span>

|<span data-ttu-id="67604-123">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="67604-123">**Attribute**</span></span>|<span data-ttu-id="67604-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67604-124">**Type**</span></span>|<span data-ttu-id="67604-125">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="67604-125">**Required**</span></span>|<span data-ttu-id="67604-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67604-126">**Description**</span></span>|<span data-ttu-id="67604-127">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="67604-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67604-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="67604-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="67604-129">XS: String</span><span class="sxs-lookup"><span data-stu-id="67604-129">xs:string</span></span>  <br/> |<span data-ttu-id="67604-130">necesario</span><span class="sxs-lookup"><span data-stu-id="67604-130">required</span></span>  <br/> |<span data-ttu-id="67604-131">Especifica un código que está asociado con la ubicación para distinguir varias ubicaciones con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="67604-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="67604-132">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="67604-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="67604-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="67604-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="67604-134">XS: String</span><span class="sxs-lookup"><span data-stu-id="67604-134">xs:string</span></span>  <br/> |<span data-ttu-id="67604-135">necesario</span><span class="sxs-lookup"><span data-stu-id="67604-135">required</span></span>  <br/> |<span data-ttu-id="67604-136">Especifica el nombre de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="67604-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="67604-137">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="67604-137">A value of the type xs:string</span></span>  <br/> |
   

