---
title: Elemento EventList (complexType VisioDocument_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contiene un elemento EventItem por cada evento al que debe responder un objeto.
ms.openlocfilehash: 7b1406f56dddd8507e330aa93d5cfe9f390caf21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541802"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="afcfc-103">Elemento EventList (complexType VisioDocument_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="afcfc-103">EventList element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="afcfc-104">Contiene un elemento **EventItem** por cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="afcfc-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="afcfc-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="afcfc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afcfc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="afcfc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="afcfc-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="afcfc-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="afcfc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="afcfc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="afcfc-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="afcfc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="afcfc-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="afcfc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="afcfc-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="afcfc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="afcfc-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="afcfc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="afcfc-113">Definición</span><span class="sxs-lookup"><span data-stu-id="afcfc-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="afcfc-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="afcfc-114">Elements and attributes</span></span>

<span data-ttu-id="afcfc-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="afcfc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="afcfc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="afcfc-116">Parent elements</span></span>

|<span data-ttu-id="afcfc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afcfc-117">**Element**</span></span>|<span data-ttu-id="afcfc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="afcfc-118">**Type**</span></span>|<span data-ttu-id="afcfc-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afcfc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afcfc-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="afcfc-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="afcfc-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="afcfc-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afcfc-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="afcfc-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="afcfc-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="afcfc-123">Child elements</span></span>

|<span data-ttu-id="afcfc-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="afcfc-124">**Element**</span></span>|<span data-ttu-id="afcfc-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="afcfc-125">**Type**</span></span>|<span data-ttu-id="afcfc-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="afcfc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="afcfc-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="afcfc-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="afcfc-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="afcfc-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="afcfc-129">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="afcfc-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="afcfc-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="afcfc-130">Attributes</span></span>

<span data-ttu-id="afcfc-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afcfc-131">None.</span></span>
  

