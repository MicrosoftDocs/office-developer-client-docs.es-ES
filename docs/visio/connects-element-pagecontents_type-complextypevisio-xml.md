---
title: Se conecta el elemento (PageContents_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contiene un elemento Connect para cada conexión entre dos formas de un dibujo.
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399959"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="d637c-103">Se conecta el elemento (PageContents_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="d637c-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d637c-104">Contiene un elemento **Connect** para cada conexión entre dos formas de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d637c-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d637c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d637c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d637c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d637c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d637c-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="d637c-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d637c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d637c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d637c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d637c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d637c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d637c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d637c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="d637c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d637c-112">página # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="d637c-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d637c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="d637c-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d637c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d637c-114">Elements and attributes</span></span>

<span data-ttu-id="d637c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="d637c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d637c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d637c-116">Parent elements</span></span>

|<span data-ttu-id="d637c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d637c-117">**Element**</span></span>|<span data-ttu-id="d637c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d637c-118">**Type**</span></span>|<span data-ttu-id="d637c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d637c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d637c-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="d637c-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="d637c-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="d637c-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d637c-122">Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d637c-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="d637c-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="d637c-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="d637c-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="d637c-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d637c-125">Especifica la información acerca de las formas en una página maestra o dibujo de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d637c-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d637c-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d637c-126">Child elements</span></span>

|<span data-ttu-id="d637c-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="d637c-127">**Element**</span></span>|<span data-ttu-id="d637c-128">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d637c-128">**Type**</span></span>|<span data-ttu-id="d637c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d637c-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d637c-130">Connect</span><span class="sxs-lookup"><span data-stu-id="d637c-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d637c-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="d637c-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d637c-132">
			Representa una conexión entre dos formas de un dibujo, como una línea y un cuadro en un organigrama.
</span><span class="sxs-lookup"><span data-stu-id="d637c-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d637c-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="d637c-133">Attributes</span></span>

<span data-ttu-id="d637c-134">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d637c-134">None.</span></span>
  

