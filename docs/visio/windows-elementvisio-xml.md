---
title: Elemento de Windows ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contiene los elementos de la ventana de un documento.
ms.openlocfilehash: 70746ccfa2d99a9fdd5b3a91320c9372aa233c7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823542"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="90682-103">Elemento de Windows ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="90682-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="90682-104">Contiene los elementos de la **ventana** de un documento.</span><span class="sxs-lookup"><span data-stu-id="90682-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="90682-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90682-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90682-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="90682-106">**Element type**</span></span> <br/> |[<span data-ttu-id="90682-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="90682-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="90682-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="90682-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="90682-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="90682-109">**Schema file**</span></span> <br/> |<span data-ttu-id="90682-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="90682-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="90682-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="90682-111">**Document parts**</span></span> <br/> |<span data-ttu-id="90682-112">Windows.Xml</span><span class="sxs-lookup"><span data-stu-id="90682-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="90682-113">Definición</span><span class="sxs-lookup"><span data-stu-id="90682-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="90682-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="90682-114">Elements and attributes</span></span>

<span data-ttu-id="90682-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="90682-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="90682-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90682-116">Parent elements</span></span>

<span data-ttu-id="90682-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="90682-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90682-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90682-118">Child elements</span></span>

|<span data-ttu-id="90682-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="90682-119">**Element**</span></span>|<span data-ttu-id="90682-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="90682-120">**Type**</span></span>|<span data-ttu-id="90682-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90682-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="90682-122">Window</span><span class="sxs-lookup"><span data-stu-id="90682-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90682-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="90682-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="90682-124">Representa una ventana abierta en una instancia de Microsoft Visio.
</span><span class="sxs-lookup"><span data-stu-id="90682-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="90682-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="90682-125">Attributes</span></span>

|<span data-ttu-id="90682-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="90682-126">**Attribute**</span></span>|<span data-ttu-id="90682-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="90682-127">**Type**</span></span>|<span data-ttu-id="90682-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="90682-128">**Required**</span></span>|<span data-ttu-id="90682-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90682-129">**Description**</span></span>|<span data-ttu-id="90682-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="90682-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="90682-131">Propiedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="90682-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="90682-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="90682-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="90682-133">opcional</span><span class="sxs-lookup"><span data-stu-id="90682-133">optional</span></span>  <br/> |<span data-ttu-id="90682-134">Representa el alto de un área de presentación</span><span class="sxs-lookup"><span data-stu-id="90682-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="90682-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="90682-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="90682-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="90682-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="90682-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="90682-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="90682-138">opcional</span><span class="sxs-lookup"><span data-stu-id="90682-138">optional</span></span>  <br/> |<span data-ttu-id="90682-139">Representa el ancho de un área de presentación</span><span class="sxs-lookup"><span data-stu-id="90682-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="90682-140">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="90682-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

