---
title: Elemento weatherdata (Esquema de ubicación meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Define el elemento meteorológico.
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540934"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="1e7ba-103">Elemento weatherdata (Esquema de ubicación meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="1e7ba-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="1e7ba-104">Define el elemento meteorológico.</span><span class="sxs-lookup"><span data-stu-id="1e7ba-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e7ba-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1e7ba-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e7ba-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1e7ba-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="1e7ba-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e7ba-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="1e7ba-108">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1e7ba-108">**Schema file**</span></span> <br/> |<span data-ttu-id="1e7ba-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="1e7ba-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e7ba-110">Definición</span><span class="sxs-lookup"><span data-stu-id="1e7ba-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1e7ba-111">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1e7ba-111">Elements and attributes</span></span>

<span data-ttu-id="1e7ba-112">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1e7ba-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1e7ba-113">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1e7ba-113">Parent elements</span></span>

<span data-ttu-id="1e7ba-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1e7ba-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e7ba-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1e7ba-115">Child elements</span></span>

|<span data-ttu-id="1e7ba-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1e7ba-116">**Element**</span></span>|<span data-ttu-id="1e7ba-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1e7ba-117">**Type**</span></span>|<span data-ttu-id="1e7ba-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1e7ba-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e7ba-119">el tiempo</span><span class="sxs-lookup"><span data-stu-id="1e7ba-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="1e7ba-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="1e7ba-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="1e7ba-121">Especifica la ubicación en la que se debe informar sobre el tiempo.</span><span class="sxs-lookup"><span data-stu-id="1e7ba-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1e7ba-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="1e7ba-122">Attributes</span></span>

<span data-ttu-id="1e7ba-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1e7ba-123">None.</span></span>
  

