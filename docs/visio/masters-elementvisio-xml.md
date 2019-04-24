---
title: Elemento Masters ("XML de Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contiene los elementos Master del documento.
ms.openlocfilehash: ea2cee2f9845f8a72220081617a11cf4f72dafd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341429"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="ccaa8-103">Elemento Masters ("XML de Visio")</span><span class="sxs-lookup"><span data-stu-id="ccaa8-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="ccaa8-104">Contiene los elementos Master del documento.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccaa8-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ccaa8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccaa8-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ccaa8-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="ccaa8-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ccaa8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ccaa8-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ccaa8-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ccaa8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ccaa8-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ccaa8-112">Masters. XML</span><span class="sxs-lookup"><span data-stu-id="ccaa8-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ccaa8-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ccaa8-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ccaa8-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ccaa8-114">Elements and attributes</span></span>

<span data-ttu-id="ccaa8-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ccaa8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ccaa8-116">Parent elements</span></span>

<span data-ttu-id="ccaa8-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccaa8-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccaa8-118">Child elements</span></span>

|<span data-ttu-id="ccaa8-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-119">**Element**</span></span>|<span data-ttu-id="ccaa8-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-120">**Type**</span></span>|<span data-ttu-id="ccaa8-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ccaa8-122">Master</span><span class="sxs-lookup"><span data-stu-id="ccaa8-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ccaa8-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="ccaa8-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccaa8-124">Contiene elementos que definen un patrón para el documento.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="ccaa8-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="ccaa8-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ccaa8-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="ccaa8-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccaa8-127">Especifica un acceso directo de patrón definido en el documento.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ccaa8-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="ccaa8-128">Attributes</span></span>

<span data-ttu-id="ccaa8-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-129">None.</span></span>
  

