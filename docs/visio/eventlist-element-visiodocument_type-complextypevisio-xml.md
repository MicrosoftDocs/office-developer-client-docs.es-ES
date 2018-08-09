---
title: Elemento de EventList (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contiene un elemento EventItem para cada evento al que debe responder un objeto.
ms.openlocfilehash: e1033ae93ca272b8ea1d9855d08ad13a444612db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822076"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="30143-103">Elemento de EventList (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="30143-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="30143-104">Contiene un elemento **EventItem** para cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="30143-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="30143-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="30143-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30143-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="30143-106">**Element type**</span></span> <br/> |[<span data-ttu-id="30143-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="30143-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="30143-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30143-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="30143-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="30143-109">**Schema file**</span></span> <br/> |<span data-ttu-id="30143-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="30143-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="30143-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="30143-111">**Document parts**</span></span> <br/> |<span data-ttu-id="30143-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="30143-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30143-113">Definición</span><span class="sxs-lookup"><span data-stu-id="30143-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="30143-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="30143-114">Elements and attributes</span></span>

<span data-ttu-id="30143-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="30143-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="30143-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="30143-116">Parent elements</span></span>

|<span data-ttu-id="30143-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="30143-117">**Element**</span></span>|<span data-ttu-id="30143-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30143-118">**Type**</span></span>|<span data-ttu-id="30143-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30143-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30143-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="30143-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="30143-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="30143-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30143-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="30143-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="30143-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30143-123">Child elements</span></span>

|<span data-ttu-id="30143-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="30143-124">**Element**</span></span>|<span data-ttu-id="30143-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="30143-125">**Type**</span></span>|<span data-ttu-id="30143-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30143-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30143-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="30143-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30143-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="30143-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30143-129">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="30143-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="30143-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="30143-130">Attributes</span></span>

<span data-ttu-id="30143-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30143-131">None.</span></span>
  

