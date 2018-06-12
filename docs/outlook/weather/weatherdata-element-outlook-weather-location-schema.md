---
title: elemento WeatherData (esquema de ubicación de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Define el elemento de meteorología.
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821329"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="fbbf9-103">elemento WeatherData (esquema de ubicación de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="fbbf9-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="fbbf9-104">Define el elemento de meteorología.</span><span class="sxs-lookup"><span data-stu-id="fbbf9-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbbf9-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fbbf9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbbf9-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fbbf9-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="fbbf9-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fbbf9-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="fbbf9-108">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fbbf9-108">**Schema file**</span></span> <br/> |<span data-ttu-id="fbbf9-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="fbbf9-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fbbf9-110">Definición</span><span class="sxs-lookup"><span data-stu-id="fbbf9-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fbbf9-111">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fbbf9-111">Elements and attributes</span></span>

<span data-ttu-id="fbbf9-112">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="fbbf9-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fbbf9-113">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fbbf9-113">Parent elements</span></span>

<span data-ttu-id="fbbf9-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fbbf9-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbbf9-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fbbf9-115">Child elements</span></span>

|<span data-ttu-id="fbbf9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbbf9-116">**Element**</span></span>|<span data-ttu-id="fbbf9-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fbbf9-117">**Type**</span></span>|<span data-ttu-id="fbbf9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbbf9-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbbf9-119">meteorología</span><span class="sxs-lookup"><span data-stu-id="fbbf9-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="fbbf9-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="fbbf9-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="fbbf9-121">Especifica la ubicación de meteorología de informe en.</span><span class="sxs-lookup"><span data-stu-id="fbbf9-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fbbf9-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbbf9-122">Attributes</span></span>

<span data-ttu-id="fbbf9-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fbbf9-123">None.</span></span>
  

