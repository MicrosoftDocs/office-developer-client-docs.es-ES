---
title: Elemento de ProtectMasters (DocumentSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica si el usuario impide crear, editar o eliminar formas de patrón. El usuario puede crear nuevas formas de una forma de patrón, independientemente de esta configuración.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386449"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="2d655-104">Elemento de ProtectMasters (DocumentSettings_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="2d655-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2d655-105">Especifica si el usuario impide crear, editar o eliminar formas de patrón.</span><span class="sxs-lookup"><span data-stu-id="2d655-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="2d655-106">El usuario puede crear nuevas formas de una forma de patrón, independientemente de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="2d655-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="2d655-107">El intervalo de valores posibles para este elemento es '0' o '1'.</span><span class="sxs-lookup"><span data-stu-id="2d655-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="2d655-108">Un valor de '0' indica que los usuarios pueden crear, editar o eliminar formas de patrón.</span><span class="sxs-lookup"><span data-stu-id="2d655-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="2d655-109">Un valor de '1' indica que los usuarios no pueden crear, modificar o eliminar formas de patrón.</span><span class="sxs-lookup"><span data-stu-id="2d655-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d655-110">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2d655-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d655-111">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2d655-111">**Element type**</span></span> <br/> |[<span data-ttu-id="2d655-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="2d655-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2d655-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2d655-113">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2d655-114">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2d655-114">**Schema file**</span></span> <br/> |<span data-ttu-id="2d655-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2d655-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2d655-116">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="2d655-116">**Document parts**</span></span> <br/> |<span data-ttu-id="2d655-117">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="2d655-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2d655-118">Definición</span><span class="sxs-lookup"><span data-stu-id="2d655-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2d655-119">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2d655-119">Elements and attributes</span></span>

<span data-ttu-id="2d655-120">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="2d655-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2d655-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2d655-121">Parent elements</span></span>

|<span data-ttu-id="2d655-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d655-122">**Element**</span></span>|<span data-ttu-id="2d655-123">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2d655-123">**Type**</span></span>|<span data-ttu-id="2d655-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d655-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2d655-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="2d655-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2d655-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="2d655-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2d655-127">Contiene elementos que especifican la configuración de documentos.</span><span class="sxs-lookup"><span data-stu-id="2d655-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2d655-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2d655-128">Child elements</span></span>

<span data-ttu-id="2d655-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d655-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d655-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d655-130">Attributes</span></span>

<span data-ttu-id="2d655-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d655-131">None.</span></span>
  

