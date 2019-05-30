---
title: complexType weatherType (esquema de ubicación de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define los parámetros sobre las condiciones meteorológicas de una ubicación.
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542922"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="dd3c0-103">complexType weatherType (esquema de ubicación de tiempo de Outlook)</span><span class="sxs-lookup"><span data-stu-id="dd3c0-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="dd3c0-104">Define los parámetros sobre las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="dd3c0-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="dd3c0-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="dd3c0-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd3c0-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="dd3c0-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-107">**Schema file**</span></span> <br/> |<span data-ttu-id="dd3c0-108">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="dd3c0-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="dd3c0-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-109">**Extension base**</span></span> <br/> |<span data-ttu-id="dd3c0-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dd3c0-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dd3c0-111">Definición</span><span class="sxs-lookup"><span data-stu-id="dd3c0-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="dd3c0-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="dd3c0-112">Elements and attributes</span></span>

<span data-ttu-id="dd3c0-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="dd3c0-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dd3c0-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd3c0-114">Child elements</span></span>

<span data-ttu-id="dd3c0-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd3c0-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd3c0-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd3c0-116">Attributes</span></span>

|<span data-ttu-id="dd3c0-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-117">**Attribute**</span></span>|<span data-ttu-id="dd3c0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-118">**Type**</span></span>|<span data-ttu-id="dd3c0-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-119">**Required**</span></span>|<span data-ttu-id="dd3c0-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-120">**Description**</span></span>|<span data-ttu-id="dd3c0-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="dd3c0-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dd3c0-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="dd3c0-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="dd3c0-123">XS: String</span><span class="sxs-lookup"><span data-stu-id="dd3c0-123">xs:string</span></span>  <br/> |<span data-ttu-id="dd3c0-124">necesario</span><span class="sxs-lookup"><span data-stu-id="dd3c0-124">required</span></span>  <br/> |<span data-ttu-id="dd3c0-125">Especifica un código que está asociado con la ubicación para distinguir varias ubicaciones con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="dd3c0-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="dd3c0-126">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="dd3c0-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="dd3c0-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="dd3c0-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="dd3c0-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="dd3c0-128">xs:string</span></span>  <br/> |<span data-ttu-id="dd3c0-129">necesario</span><span class="sxs-lookup"><span data-stu-id="dd3c0-129">required</span></span>  <br/> |<span data-ttu-id="dd3c0-130">Especifica el nombre de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="dd3c0-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="dd3c0-131">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="dd3c0-131">A value of the type xs:string</span></span>  <br/> |
   

