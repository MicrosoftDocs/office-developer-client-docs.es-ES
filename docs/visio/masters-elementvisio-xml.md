---
title: Elemento de patrones ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contiene el patrón de elementos para el documento.
ms.openlocfilehash: d40071c64dc454eeb92f8518f89ef4de8b3b0cb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822577"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="21e87-103">Elemento de patrones ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="21e87-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="21e87-104">Contiene el patrón de elementos para el documento.</span><span class="sxs-lookup"><span data-stu-id="21e87-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21e87-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="21e87-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21e87-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="21e87-106">**Element type**</span></span> <br/> |[<span data-ttu-id="21e87-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="21e87-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="21e87-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="21e87-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="21e87-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="21e87-109">**Schema file**</span></span> <br/> |<span data-ttu-id="21e87-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="21e87-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="21e87-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="21e87-111">**Document parts**</span></span> <br/> |<span data-ttu-id="21e87-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="21e87-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21e87-113">Definición</span><span class="sxs-lookup"><span data-stu-id="21e87-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="21e87-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="21e87-114">Elements and attributes</span></span>

<span data-ttu-id="21e87-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="21e87-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="21e87-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="21e87-116">Parent elements</span></span>

<span data-ttu-id="21e87-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21e87-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21e87-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="21e87-118">Child elements</span></span>

|<span data-ttu-id="21e87-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="21e87-119">**Element**</span></span>|<span data-ttu-id="21e87-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="21e87-120">**Type**</span></span>|<span data-ttu-id="21e87-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21e87-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21e87-122">Master</span><span class="sxs-lookup"><span data-stu-id="21e87-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21e87-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="21e87-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21e87-124">Contiene elementos que definen a un patrón para el documento.</span><span class="sxs-lookup"><span data-stu-id="21e87-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="21e87-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="21e87-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21e87-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="21e87-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21e87-127">Especifica un acceso directo de patrón definido en el documento.</span><span class="sxs-lookup"><span data-stu-id="21e87-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="21e87-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="21e87-128">Attributes</span></span>

<span data-ttu-id="21e87-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21e87-129">None.</span></span>
  

