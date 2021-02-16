---
title: Elemento De Windows (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contiene los elementos Window de un documento.
ms.openlocfilehash: fcffcd5257b14c0ae0203a41f369536e583c1798
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538448"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="50e2b-103">Elemento De Windows (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="50e2b-103">Windows element (Visio XML)</span></span>

<span data-ttu-id="50e2b-104">Contiene los **elementos Window** de un documento.</span><span class="sxs-lookup"><span data-stu-id="50e2b-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="50e2b-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="50e2b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50e2b-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="50e2b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="50e2b-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="50e2b-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="50e2b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="50e2b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="50e2b-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="50e2b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="50e2b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="50e2b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="50e2b-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="50e2b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="50e2b-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="50e2b-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="50e2b-113">Definición</span><span class="sxs-lookup"><span data-stu-id="50e2b-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="50e2b-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="50e2b-114">Elements and attributes</span></span>

<span data-ttu-id="50e2b-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="50e2b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="50e2b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="50e2b-116">Parent elements</span></span>

<span data-ttu-id="50e2b-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="50e2b-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50e2b-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="50e2b-118">Child elements</span></span>

|<span data-ttu-id="50e2b-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50e2b-119">**Element**</span></span>|<span data-ttu-id="50e2b-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="50e2b-120">**Type**</span></span>|<span data-ttu-id="50e2b-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50e2b-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50e2b-122">Window</span><span class="sxs-lookup"><span data-stu-id="50e2b-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50e2b-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="50e2b-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="50e2b-124">Representa una ventana abierta en una instancia de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="50e2b-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="50e2b-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="50e2b-125">Attributes</span></span>

|<span data-ttu-id="50e2b-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="50e2b-126">**Attribute**</span></span>|<span data-ttu-id="50e2b-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="50e2b-127">**Type**</span></span>|<span data-ttu-id="50e2b-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="50e2b-128">**Required**</span></span>|<span data-ttu-id="50e2b-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50e2b-129">**Description**</span></span>|<span data-ttu-id="50e2b-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="50e2b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="50e2b-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="50e2b-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="50e2b-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="50e2b-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="50e2b-133">opcional</span><span class="sxs-lookup"><span data-stu-id="50e2b-133">optional</span></span>  <br/> |<span data-ttu-id="50e2b-134">Representa la dimensión de alto de un área de presentación</span><span class="sxs-lookup"><span data-stu-id="50e2b-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="50e2b-135">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="50e2b-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="50e2b-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="50e2b-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="50e2b-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="50e2b-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="50e2b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="50e2b-138">optional</span></span>  <br/> |<span data-ttu-id="50e2b-139">Representa la dimensión de ancho de un área de presentación</span><span class="sxs-lookup"><span data-stu-id="50e2b-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="50e2b-140">Valores del tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="50e2b-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

