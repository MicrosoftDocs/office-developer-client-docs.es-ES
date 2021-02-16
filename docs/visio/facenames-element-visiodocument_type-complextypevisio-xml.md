---
title: Elemento FaceNames (VisioDocument_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Contiene una colección de elementos FaceName.
ms.openlocfilehash: ce18847fdd46a0c703a0df5e8d8c7a877f864d35
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539716"
---
# <a name="facenames-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="32bb6-103">Elemento FaceNames (VisioDocument_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="32bb6-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="32bb6-104">Contiene una colección de **elementos FaceName.**</span><span class="sxs-lookup"><span data-stu-id="32bb6-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="32bb6-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="32bb6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32bb6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="32bb6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="32bb6-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="32bb6-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="32bb6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="32bb6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="32bb6-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="32bb6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="32bb6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="32bb6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="32bb6-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="32bb6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="32bb6-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="32bb6-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32bb6-113">Definición</span><span class="sxs-lookup"><span data-stu-id="32bb6-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32bb6-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="32bb6-114">Elements and attributes</span></span>

<span data-ttu-id="32bb6-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="32bb6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="32bb6-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="32bb6-116">Parent elements</span></span>

|<span data-ttu-id="32bb6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="32bb6-117">**Element**</span></span>|<span data-ttu-id="32bb6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="32bb6-118">**Type**</span></span>|<span data-ttu-id="32bb6-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="32bb6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32bb6-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="32bb6-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="32bb6-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="32bb6-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32bb6-122">Elemento raíz de un documento de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="32bb6-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="32bb6-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="32bb6-123">Child elements</span></span>

|<span data-ttu-id="32bb6-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="32bb6-124">**Element**</span></span>|<span data-ttu-id="32bb6-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="32bb6-125">**Type**</span></span>|<span data-ttu-id="32bb6-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="32bb6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32bb6-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="32bb6-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32bb6-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="32bb6-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32bb6-129">Contiene información acerca de una fuente.</span><span class="sxs-lookup"><span data-stu-id="32bb6-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="32bb6-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="32bb6-130">Attributes</span></span>

<span data-ttu-id="32bb6-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="32bb6-131">None.</span></span>
  

