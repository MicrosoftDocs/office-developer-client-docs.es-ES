---
title: Elemento weatherdata (Esquema de información meteorológica de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Define el elemento meteorológico.
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538987"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="c09ed-103">Elemento weatherdata (Esquema de información meteorológica de Outlook)</span><span class="sxs-lookup"><span data-stu-id="c09ed-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="c09ed-104">Define el elemento meteorológico.</span><span class="sxs-lookup"><span data-stu-id="c09ed-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c09ed-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c09ed-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c09ed-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c09ed-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="c09ed-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c09ed-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="c09ed-108">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c09ed-108">**Schema file**</span></span> <br/> |<span data-ttu-id="c09ed-109">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="c09ed-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c09ed-110">Definición</span><span class="sxs-lookup"><span data-stu-id="c09ed-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c09ed-111">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c09ed-111">Elements and attributes</span></span>

<span data-ttu-id="c09ed-112">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c09ed-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c09ed-113">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c09ed-113">Parent elements</span></span>

<span data-ttu-id="c09ed-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c09ed-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c09ed-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c09ed-115">Child elements</span></span>

|<span data-ttu-id="c09ed-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c09ed-116">**Element**</span></span>|<span data-ttu-id="c09ed-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c09ed-117">**Type**</span></span>|<span data-ttu-id="c09ed-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c09ed-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c09ed-119">el tiempo</span><span class="sxs-lookup"><span data-stu-id="c09ed-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="c09ed-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="c09ed-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="c09ed-121">Especifica las condiciones meteorológicas de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="c09ed-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c09ed-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="c09ed-122">Attributes</span></span>

<span data-ttu-id="c09ed-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c09ed-123">None.</span></span>
  

