---
title: Elemento Masters (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contiene los elementos Master del documento.
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538056"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="4e4c5-103">Elemento Masters (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="4e4c5-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="4e4c5-104">Contiene los elementos Master del documento.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e4c5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4e4c5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e4c5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4e4c5-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="4e4c5-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4e4c5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4e4c5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4e4c5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4e4c5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4e4c5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4e4c5-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="4e4c5-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4e4c5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="4e4c5-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4e4c5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4e4c5-114">Elements and attributes</span></span>

<span data-ttu-id="4e4c5-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4e4c5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4e4c5-116">Parent elements</span></span>

<span data-ttu-id="4e4c5-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e4c5-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e4c5-118">Child elements</span></span>

|<span data-ttu-id="4e4c5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-119">**Element**</span></span>|<span data-ttu-id="4e4c5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-120">**Type**</span></span>|<span data-ttu-id="4e4c5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e4c5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4e4c5-122">Master</span><span class="sxs-lookup"><span data-stu-id="4e4c5-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4e4c5-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="4e4c5-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4e4c5-124">Contiene elementos que definen un patrón para el documento.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="4e4c5-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="4e4c5-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4e4c5-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="4e4c5-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4e4c5-127">Especifica un acceso directo de patrón definido en el documento.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4e4c5-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e4c5-128">Attributes</span></span>

<span data-ttu-id="4e4c5-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-129">None.</span></span>
  

