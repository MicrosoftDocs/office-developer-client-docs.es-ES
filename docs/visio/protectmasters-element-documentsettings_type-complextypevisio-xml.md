---
title: Elemento ProtectMasters (DocumentSettings_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Especifica si el usuario no puede crear, editar o eliminar formas maestras. El usuario aún puede crear nuevas formas a partir de una forma maestra, independientemente de esta configuración.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540696"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="1350d-104">Elemento ProtectMasters (DocumentSettings_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="1350d-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1350d-105">Especifica si el usuario no puede crear, editar o eliminar formas maestras.</span><span class="sxs-lookup"><span data-stu-id="1350d-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="1350d-106">El usuario aún puede crear nuevas formas a partir de una forma maestra, independientemente de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="1350d-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="1350d-107">El intervalo de valores posibles para este elemento es '0' o '1'.</span><span class="sxs-lookup"><span data-stu-id="1350d-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="1350d-108">Un valor de "0" indica que los usuarios pueden crear, editar o eliminar formas maestras.</span><span class="sxs-lookup"><span data-stu-id="1350d-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="1350d-109">Un valor de "1" indica que los usuarios no pueden crear, editar ni eliminar formas maestras.</span><span class="sxs-lookup"><span data-stu-id="1350d-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1350d-110">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1350d-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1350d-111">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1350d-111">**Element type**</span></span> <br/> |[<span data-ttu-id="1350d-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="1350d-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1350d-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1350d-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1350d-114">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1350d-114">**Schema file**</span></span> <br/> |<span data-ttu-id="1350d-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1350d-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1350d-116">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1350d-116">**Document parts**</span></span> <br/> |<span data-ttu-id="1350d-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="1350d-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1350d-118">Definición</span><span class="sxs-lookup"><span data-stu-id="1350d-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1350d-119">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1350d-119">Elements and attributes</span></span>

<span data-ttu-id="1350d-120">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="1350d-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1350d-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1350d-121">Parent elements</span></span>

|<span data-ttu-id="1350d-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1350d-122">**Element**</span></span>|<span data-ttu-id="1350d-123">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1350d-123">**Type**</span></span>|<span data-ttu-id="1350d-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1350d-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1350d-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="1350d-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1350d-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="1350d-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1350d-127">Contiene elementos que especifican la configuración del documento.</span><span class="sxs-lookup"><span data-stu-id="1350d-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1350d-128">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1350d-128">Child elements</span></span>

<span data-ttu-id="1350d-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1350d-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1350d-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="1350d-130">Attributes</span></span>

<span data-ttu-id="1350d-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1350d-131">None.</span></span>
  

