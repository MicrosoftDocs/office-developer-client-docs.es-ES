---
title: Elemento EventList (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contiene un elemento EventItem para cada evento al que debe responder un objeto.
ms.openlocfilehash: 7b1406f56dddd8507e330aa93d5cfe9f390caf21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541802"
---
# <a name="eventlist-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="bb42b-103">Elemento EventList (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bb42b-103">EventList element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bb42b-104">Contiene un **elemento EventItem** para cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="bb42b-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="bb42b-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb42b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb42b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="bb42b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bb42b-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="bb42b-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bb42b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bb42b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bb42b-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bb42b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bb42b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bb42b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bb42b-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="bb42b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bb42b-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="bb42b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bb42b-113">Definición</span><span class="sxs-lookup"><span data-stu-id="bb42b-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bb42b-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bb42b-114">Elements and attributes</span></span>

<span data-ttu-id="bb42b-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="bb42b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bb42b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb42b-116">Parent elements</span></span>

|<span data-ttu-id="bb42b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb42b-117">**Element**</span></span>|<span data-ttu-id="bb42b-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bb42b-118">**Type**</span></span>|<span data-ttu-id="bb42b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb42b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bb42b-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="bb42b-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="bb42b-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="bb42b-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bb42b-122">Elemento raíz de un documento Visio Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bb42b-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb42b-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb42b-123">Child elements</span></span>

|<span data-ttu-id="bb42b-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb42b-124">**Element**</span></span>|<span data-ttu-id="bb42b-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bb42b-125">**Type**</span></span>|<span data-ttu-id="bb42b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb42b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bb42b-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="bb42b-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bb42b-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="bb42b-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bb42b-129">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="bb42b-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bb42b-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb42b-130">Attributes</span></span>

<span data-ttu-id="bb42b-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb42b-131">None.</span></span>
  

