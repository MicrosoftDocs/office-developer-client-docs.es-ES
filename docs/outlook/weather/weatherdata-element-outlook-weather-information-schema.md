---
title: elemento WeatherData (esquema de información de meteorología de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Define el elemento de meteorología.
ms.openlocfilehash: 689c390f621d18f680de9635c3d82711300f8030
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821330"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="ba4a4-103">elemento WeatherData (esquema de información de meteorología de Outlook)</span><span class="sxs-lookup"><span data-stu-id="ba4a4-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="ba4a4-104">Define el elemento de meteorología.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba4a4-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba4a4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba4a4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ba4a4-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="ba4a4-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ba4a4-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="ba4a4-108">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ba4a4-108">**Schema file**</span></span> <br/> |<span data-ttu-id="ba4a4-109">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="ba4a4-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ba4a4-110">Definición</span><span class="sxs-lookup"><span data-stu-id="ba4a4-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ba4a4-111">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ba4a4-111">Elements and attributes</span></span>

<span data-ttu-id="ba4a4-112">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ba4a4-113">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba4a4-113">Parent elements</span></span>

<span data-ttu-id="ba4a4-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba4a4-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba4a4-115">Child elements</span></span>

|<span data-ttu-id="ba4a4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba4a4-116">**Element**</span></span>|<span data-ttu-id="ba4a4-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ba4a4-117">**Type**</span></span>|<span data-ttu-id="ba4a4-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba4a4-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ba4a4-119">meteorología</span><span class="sxs-lookup"><span data-stu-id="ba4a4-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="ba4a4-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="ba4a4-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="ba4a4-121">Especifica las condiciones del tiempo de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ba4a4-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba4a4-122">Attributes</span></span>

<span data-ttu-id="ba4a4-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba4a4-123">None.</span></span>
  

