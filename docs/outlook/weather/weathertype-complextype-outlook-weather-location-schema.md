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
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355184"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="aebc8-103">complexType weatherType (esquema de ubicación de tiempo de Outlook)</span><span class="sxs-lookup"><span data-stu-id="aebc8-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="aebc8-104">Define los parámetros sobre las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="aebc8-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="aebc8-105">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="aebc8-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aebc8-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aebc8-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="aebc8-107">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="aebc8-107">**Schema file**</span></span> <br/> |<span data-ttu-id="aebc8-108">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="aebc8-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="aebc8-109">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="aebc8-109">**Extension base**</span></span> <br/> |<span data-ttu-id="aebc8-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aebc8-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aebc8-111">Definición</span><span class="sxs-lookup"><span data-stu-id="aebc8-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="aebc8-112">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="aebc8-112">Elements and attributes</span></span>

<span data-ttu-id="aebc8-113">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="aebc8-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aebc8-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aebc8-114">Child elements</span></span>

<span data-ttu-id="aebc8-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aebc8-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aebc8-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="aebc8-116">Attributes</span></span>

|<span data-ttu-id="aebc8-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="aebc8-117">**Attribute**</span></span>|<span data-ttu-id="aebc8-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aebc8-118">**Type**</span></span>|<span data-ttu-id="aebc8-119">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="aebc8-119">**Required**</span></span>|<span data-ttu-id="aebc8-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aebc8-120">**Description**</span></span>|<span data-ttu-id="aebc8-121">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="aebc8-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aebc8-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="aebc8-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="aebc8-123">XS: String</span><span class="sxs-lookup"><span data-stu-id="aebc8-123">xs:string</span></span>  <br/> |<span data-ttu-id="aebc8-124">necesario</span><span class="sxs-lookup"><span data-stu-id="aebc8-124">required</span></span>  <br/> |<span data-ttu-id="aebc8-125">Especifica un código que está asociado con la ubicación para distinguir varias ubicaciones con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="aebc8-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="aebc8-126">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="aebc8-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="aebc8-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="aebc8-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="aebc8-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="aebc8-128">xs:string</span></span>  <br/> |<span data-ttu-id="aebc8-129">necesario</span><span class="sxs-lookup"><span data-stu-id="aebc8-129">required</span></span>  <br/> |<span data-ttu-id="aebc8-130">Especifica el nombre de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="aebc8-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="aebc8-131">Un valor de tipo XS: String</span><span class="sxs-lookup"><span data-stu-id="aebc8-131">A value of the type xs:string</span></span>  <br/> |
   

