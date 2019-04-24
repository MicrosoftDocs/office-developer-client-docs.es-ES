---
title: elemento datos (esquema de ubicación de tiempo de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Define el elemento Weather.
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355037"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="4f306-103">elemento datos (esquema de ubicación de tiempo de Outlook)</span><span class="sxs-lookup"><span data-stu-id="4f306-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="4f306-104">Define el elemento Weather.</span><span class="sxs-lookup"><span data-stu-id="4f306-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f306-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4f306-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f306-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4f306-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="4f306-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4f306-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="4f306-108">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4f306-108">**Schema file**</span></span> <br/> |<span data-ttu-id="4f306-109">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="4f306-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f306-110">Definición</span><span class="sxs-lookup"><span data-stu-id="4f306-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4f306-111">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4f306-111">Elements and attributes</span></span>

<span data-ttu-id="4f306-112">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="4f306-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f306-113">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4f306-113">Parent elements</span></span>

<span data-ttu-id="4f306-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f306-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f306-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4f306-115">Child elements</span></span>

|<span data-ttu-id="4f306-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4f306-116">**Element**</span></span>|<span data-ttu-id="4f306-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4f306-117">**Type**</span></span>|<span data-ttu-id="4f306-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4f306-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f306-119">Boletín</span><span class="sxs-lookup"><span data-stu-id="4f306-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="4f306-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="4f306-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="4f306-121">Especifica la ubicación en la que se va a notificar el tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f306-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4f306-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="4f306-122">Attributes</span></span>

<span data-ttu-id="4f306-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f306-123">None.</span></span>
  

