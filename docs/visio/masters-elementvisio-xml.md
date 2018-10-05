---
title: Elemento de patrones ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contiene el patrón de elementos para el documento.
ms.openlocfilehash: ea2cee2f9845f8a72220081617a11cf4f72dafd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400995"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="d714c-103">Elemento de patrones ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="d714c-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="d714c-104">Contiene el patrón de elementos para el documento.</span><span class="sxs-lookup"><span data-stu-id="d714c-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d714c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d714c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d714c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d714c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d714c-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="d714c-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d714c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d714c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d714c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d714c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d714c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d714c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d714c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="d714c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d714c-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="d714c-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d714c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="d714c-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d714c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d714c-114">Elements and attributes</span></span>

<span data-ttu-id="d714c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="d714c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d714c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d714c-116">Parent elements</span></span>

<span data-ttu-id="d714c-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d714c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d714c-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d714c-118">Child elements</span></span>

|<span data-ttu-id="d714c-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="d714c-119">**Element**</span></span>|<span data-ttu-id="d714c-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d714c-120">**Type**</span></span>|<span data-ttu-id="d714c-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d714c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d714c-122">Master</span><span class="sxs-lookup"><span data-stu-id="d714c-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d714c-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="d714c-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d714c-124">Contiene elementos que definen a un patrón para el documento.</span><span class="sxs-lookup"><span data-stu-id="d714c-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="d714c-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="d714c-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d714c-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="d714c-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d714c-127">Especifica un acceso directo de patrón definido en el documento.</span><span class="sxs-lookup"><span data-stu-id="d714c-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d714c-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="d714c-128">Attributes</span></span>

<span data-ttu-id="d714c-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d714c-129">None.</span></span>
  

