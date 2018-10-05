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
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391314"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="fde28-103">elemento WeatherData (esquema de ubicación de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="fde28-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="fde28-104">Define el elemento de meteorología.</span><span class="sxs-lookup"><span data-stu-id="fde28-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fde28-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fde28-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fde28-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fde28-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="fde28-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fde28-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="fde28-108">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fde28-108">**Schema file**</span></span> <br/> |<span data-ttu-id="fde28-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="fde28-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fde28-110">Definición</span><span class="sxs-lookup"><span data-stu-id="fde28-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fde28-111">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fde28-111">Elements and attributes</span></span>

<span data-ttu-id="fde28-112">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="fde28-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fde28-113">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fde28-113">Parent elements</span></span>

<span data-ttu-id="fde28-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fde28-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fde28-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fde28-115">Child elements</span></span>

|<span data-ttu-id="fde28-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fde28-116">**Element**</span></span>|<span data-ttu-id="fde28-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fde28-117">**Type**</span></span>|<span data-ttu-id="fde28-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fde28-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fde28-119">meteorología</span><span class="sxs-lookup"><span data-stu-id="fde28-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="fde28-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="fde28-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="fde28-121">Especifica la ubicación de meteorología de informe en.</span><span class="sxs-lookup"><span data-stu-id="fde28-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fde28-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="fde28-122">Attributes</span></span>

<span data-ttu-id="fde28-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fde28-123">None.</span></span>
  

