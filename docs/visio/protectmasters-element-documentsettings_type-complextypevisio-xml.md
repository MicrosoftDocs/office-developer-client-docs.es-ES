---
title: Elemento de ProtectMasters (DocumentSettings_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica si el usuario impide crear, editar o eliminar formas de patrón. El usuario puede crear nuevas formas de una forma de patrón, independientemente de esta configuración.
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822865"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="a6455-104">Elemento de ProtectMasters (DocumentSettings_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a6455-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a6455-105">Especifica si el usuario impide crear, editar o eliminar formas de patrón.</span><span class="sxs-lookup"><span data-stu-id="a6455-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="a6455-106">El usuario puede crear nuevas formas de una forma de patrón, independientemente de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="a6455-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="a6455-107">El intervalo de valores posibles para este elemento es '0' o '1'.</span><span class="sxs-lookup"><span data-stu-id="a6455-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="a6455-108">Un valor de '0' indica que los usuarios pueden crear, editar o eliminar formas de patrón.</span><span class="sxs-lookup"><span data-stu-id="a6455-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="a6455-109">Un valor de '1' indica que los usuarios no pueden crear, modificar o eliminar formas de patrón.</span><span class="sxs-lookup"><span data-stu-id="a6455-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6455-110">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a6455-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6455-111">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a6455-111">**Element type**</span></span> <br/> |[<span data-ttu-id="a6455-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="a6455-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a6455-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a6455-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a6455-114">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a6455-114">**Schema file**</span></span> <br/> |<span data-ttu-id="a6455-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a6455-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a6455-116">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a6455-116">**Document parts**</span></span> <br/> |<span data-ttu-id="a6455-117">Document.Xml</span><span class="sxs-lookup"><span data-stu-id="a6455-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a6455-118">Definición</span><span class="sxs-lookup"><span data-stu-id="a6455-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a6455-119">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a6455-119">Elements and attributes</span></span>

<span data-ttu-id="a6455-120">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a6455-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a6455-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a6455-121">Parent elements</span></span>

|<span data-ttu-id="a6455-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="a6455-122">**Element**</span></span>|<span data-ttu-id="a6455-123">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a6455-123">**Type**</span></span>|<span data-ttu-id="a6455-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6455-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a6455-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="a6455-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a6455-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a6455-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a6455-127">Contiene elementos que especifican la configuración de documentos.</span><span class="sxs-lookup"><span data-stu-id="a6455-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a6455-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6455-128">Child elements</span></span>

<span data-ttu-id="a6455-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6455-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6455-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6455-130">Attributes</span></span>

<span data-ttu-id="a6455-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6455-131">None.</span></span>
  

