---
title: Elemento Icon (MasterShortcut_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: Especifica un icono binario codificado MIME (Multipurpose Internet Mail Extensions) (en formato .ico) para un elemento MasterShortcut de un documento.
ms.openlocfilehash: 6d223da406dd914c84aafdd3d37846c1ab30bb4e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541501"
---
# <a name="icon-element-mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="0b8d4-103">Elemento Icon (MasterShortcut_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0b8d4-103">Icon element (MasterShortcut_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0b8d4-104">Especifica un icono binario codificado MIME (Multipurpose Internet Mail Extensions) (en formato .ico) para un elemento MasterShortcut de un documento.</span><span class="sxs-lookup"><span data-stu-id="0b8d4-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b8d4-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0b8d4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b8d4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0b8d4-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="0b8d4-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0b8d4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0b8d4-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0b8d4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0b8d4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0b8d4-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0b8d4-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="0b8d4-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b8d4-113">Definición</span><span class="sxs-lookup"><span data-stu-id="0b8d4-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0b8d4-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0b8d4-114">Elements and attributes</span></span>

<span data-ttu-id="0b8d4-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0b8d4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0b8d4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0b8d4-116">Parent elements</span></span>

|<span data-ttu-id="0b8d4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-117">**Element**</span></span>|<span data-ttu-id="0b8d4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-118">**Type**</span></span>|<span data-ttu-id="0b8d4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b8d4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0b8d4-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="0b8d4-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0b8d4-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="0b8d4-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0b8d4-122">Especifica un formato maestro sin usar.</span><span class="sxs-lookup"><span data-stu-id="0b8d4-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0b8d4-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0b8d4-123">Child elements</span></span>

<span data-ttu-id="0b8d4-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0b8d4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b8d4-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="0b8d4-125">Attributes</span></span>

<span data-ttu-id="0b8d4-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0b8d4-126">None.</span></span>
  

