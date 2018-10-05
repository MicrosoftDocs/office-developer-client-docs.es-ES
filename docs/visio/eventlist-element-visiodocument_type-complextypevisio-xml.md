---
title: Elemento de EventList (VisioDocument_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Contiene un elemento EventItem para cada evento al que debe responder un objeto.
ms.openlocfilehash: 5331f1b4a510b05b862f8c7c6306c89c6be4d9f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383978"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="71290-103">Elemento de EventList (VisioDocument_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="71290-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="71290-104">Contiene un elemento **EventItem** para cada evento al que debe responder un objeto.</span><span class="sxs-lookup"><span data-stu-id="71290-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="71290-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="71290-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71290-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="71290-106">**Element type**</span></span> <br/> |[<span data-ttu-id="71290-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="71290-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="71290-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="71290-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="71290-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="71290-109">**Schema file**</span></span> <br/> |<span data-ttu-id="71290-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="71290-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="71290-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="71290-111">**Document parts**</span></span> <br/> |<span data-ttu-id="71290-112">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="71290-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="71290-113">Definición</span><span class="sxs-lookup"><span data-stu-id="71290-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="71290-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="71290-114">Elements and attributes</span></span>

<span data-ttu-id="71290-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="71290-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="71290-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="71290-116">Parent elements</span></span>

|<span data-ttu-id="71290-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="71290-117">**Element**</span></span>|<span data-ttu-id="71290-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="71290-118">**Type**</span></span>|<span data-ttu-id="71290-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71290-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71290-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="71290-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="71290-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="71290-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71290-122">El elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="71290-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="71290-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71290-123">Child elements</span></span>

|<span data-ttu-id="71290-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="71290-124">**Element**</span></span>|<span data-ttu-id="71290-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="71290-125">**Type**</span></span>|<span data-ttu-id="71290-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71290-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="71290-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="71290-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="71290-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="71290-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="71290-129">Encapsula un código de evento.</span><span class="sxs-lookup"><span data-stu-id="71290-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="71290-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="71290-130">Attributes</span></span>

<span data-ttu-id="71290-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="71290-131">None.</span></span>
  

