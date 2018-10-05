---
title: weatherType complexType (esquema de ubicación de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define los parámetros acerca de las condiciones del tiempo de una ubicación.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387716"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="ad4d5-103">weatherType complexType (esquema de ubicación de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="ad4d5-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="ad4d5-104">Define los parámetros acerca de las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ad4d5-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="ad4d5-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ad4d5-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad4d5-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="ad4d5-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-107">**Schema file**</span></span> <br/> |<span data-ttu-id="ad4d5-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="ad4d5-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="ad4d5-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-109">**Extension base**</span></span> <br/> |<span data-ttu-id="ad4d5-110">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ad4d5-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad4d5-111">Definición</span><span class="sxs-lookup"><span data-stu-id="ad4d5-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad4d5-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ad4d5-112">Elements and attributes</span></span>

<span data-ttu-id="ad4d5-113">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ad4d5-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad4d5-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad4d5-114">Child elements</span></span>

<span data-ttu-id="ad4d5-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad4d5-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad4d5-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad4d5-116">Attributes</span></span>

|<span data-ttu-id="ad4d5-117">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-117">**Attribute**</span></span>|<span data-ttu-id="ad4d5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-118">**Type**</span></span>|<span data-ttu-id="ad4d5-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-119">**Required**</span></span>|<span data-ttu-id="ad4d5-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-120">**Description**</span></span>|<span data-ttu-id="ad4d5-121">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="ad4d5-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad4d5-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="ad4d5-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="ad4d5-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="ad4d5-123">xs:string</span></span>  <br/> |<span data-ttu-id="ad4d5-124">necesario</span><span class="sxs-lookup"><span data-stu-id="ad4d5-124">required</span></span>  <br/> |<span data-ttu-id="ad4d5-125">Especifica un código que está asociado a la ubicación para distinguir varias ubicaciones con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="ad4d5-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="ad4d5-126">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="ad4d5-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ad4d5-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="ad4d5-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="ad4d5-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="ad4d5-128">xs:string</span></span>  <br/> |<span data-ttu-id="ad4d5-129">necesario</span><span class="sxs-lookup"><span data-stu-id="ad4d5-129">required</span></span>  <br/> |<span data-ttu-id="ad4d5-130">Especifica el nombre de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="ad4d5-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="ad4d5-131">Un valor del tipo xs: String</span><span class="sxs-lookup"><span data-stu-id="ad4d5-131">A value of the type xs:string</span></span>  <br/> |
   

