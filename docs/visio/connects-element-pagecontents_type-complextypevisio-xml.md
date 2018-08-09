---
title: Se conecta el elemento (PageContents_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contiene un elemento Connect para cada conexión entre dos formas de un dibujo.
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821853"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="6a260-103">Se conecta el elemento (PageContents_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="6a260-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6a260-104">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="6a260-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6a260-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a260-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a260-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6a260-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6a260-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="6a260-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6a260-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6a260-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6a260-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6a260-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6a260-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6a260-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6a260-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="6a260-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6a260-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="6a260-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6a260-113">Definición</span><span class="sxs-lookup"><span data-stu-id="6a260-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6a260-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6a260-114">Elements and attributes</span></span>

<span data-ttu-id="6a260-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="6a260-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6a260-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a260-116">Parent elements</span></span>

|<span data-ttu-id="6a260-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a260-117">**Element**</span></span>|<span data-ttu-id="6a260-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a260-118">**Type**</span></span>|<span data-ttu-id="6a260-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a260-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6a260-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="6a260-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="6a260-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6a260-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6a260-122">Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="6a260-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="6a260-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="6a260-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="6a260-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6a260-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6a260-125">Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="6a260-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6a260-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a260-126">Child elements</span></span>

|<span data-ttu-id="6a260-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a260-127">**Element**</span></span>|<span data-ttu-id="6a260-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6a260-128">**Type**</span></span>|<span data-ttu-id="6a260-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a260-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6a260-130">Connect</span><span class="sxs-lookup"><span data-stu-id="6a260-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6a260-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="6a260-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6a260-132">
			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
</span><span class="sxs-lookup"><span data-stu-id="6a260-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6a260-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a260-133">Attributes</span></span>

<span data-ttu-id="6a260-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a260-134">None.</span></span>
  

