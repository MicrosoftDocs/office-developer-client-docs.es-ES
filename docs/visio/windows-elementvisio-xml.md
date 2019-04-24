---
title: Elemento Windows ("XML de Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contiene los elementos Window de un documento.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339826"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="3eb65-103">Elemento Windows ("XML de Visio")</span><span class="sxs-lookup"><span data-stu-id="3eb65-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="3eb65-104">Contiene los elementos **Window** de un documento.</span><span class="sxs-lookup"><span data-stu-id="3eb65-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3eb65-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3eb65-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3eb65-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3eb65-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3eb65-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="3eb65-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3eb65-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3eb65-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3eb65-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3eb65-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3eb65-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3eb65-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3eb65-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="3eb65-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3eb65-112">Windows. XML</span><span class="sxs-lookup"><span data-stu-id="3eb65-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3eb65-113">Definición</span><span class="sxs-lookup"><span data-stu-id="3eb65-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3eb65-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3eb65-114">Elements and attributes</span></span>

<span data-ttu-id="3eb65-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="3eb65-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3eb65-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3eb65-116">Parent elements</span></span>

<span data-ttu-id="3eb65-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3eb65-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3eb65-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3eb65-118">Child elements</span></span>

|<span data-ttu-id="3eb65-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3eb65-119">**Element**</span></span>|<span data-ttu-id="3eb65-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3eb65-120">**Type**</span></span>|<span data-ttu-id="3eb65-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb65-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3eb65-122">Window</span><span class="sxs-lookup"><span data-stu-id="3eb65-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3eb65-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="3eb65-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3eb65-124">Representa una ventana abierta en una instancia de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3eb65-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3eb65-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="3eb65-125">Attributes</span></span>

|<span data-ttu-id="3eb65-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3eb65-126">**Attribute**</span></span>|<span data-ttu-id="3eb65-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3eb65-127">**Type**</span></span>|<span data-ttu-id="3eb65-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="3eb65-128">**Required**</span></span>|<span data-ttu-id="3eb65-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3eb65-129">**Description**</span></span>|<span data-ttu-id="3eb65-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="3eb65-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3eb65-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="3eb65-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="3eb65-132">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3eb65-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3eb65-133">opcional</span><span class="sxs-lookup"><span data-stu-id="3eb65-133">optional</span></span>  <br/> |<span data-ttu-id="3eb65-134">Representa la dimensión de alto de un área de presentación</span><span class="sxs-lookup"><span data-stu-id="3eb65-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="3eb65-135">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3eb65-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3eb65-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="3eb65-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="3eb65-137">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3eb65-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3eb65-138">opcional</span><span class="sxs-lookup"><span data-stu-id="3eb65-138">optional</span></span>  <br/> |<span data-ttu-id="3eb65-139">Representa la dimensión de ancho de un área de presentación</span><span class="sxs-lookup"><span data-stu-id="3eb65-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="3eb65-140">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3eb65-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

