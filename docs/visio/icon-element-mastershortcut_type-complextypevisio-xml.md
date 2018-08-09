---
title: Elemento de icono (MasterShortcut_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 07d8ba86-8e35-d151-e6c1-150c37cc2acd
description: Especifica que un MIME (Extensiones multipropósito de correo Internet) codificado binario icono (en formato .ico) para un elemento MasterShortcut en un documento.
ms.openlocfilehash: 46ca7c3f6ba733d31823f6b47f083c46dd941c14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822311"
---
# <a name="icon-element-mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="8d2d0-103">Elemento de icono (MasterShortcut_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="8d2d0-103">Icon element (MasterShortcut_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8d2d0-104">Especifica que un MIME (Extensiones multipropósito de correo Internet) codificado binario icono (en formato .ico) para un elemento MasterShortcut en un documento.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-104">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a MasterShortcut element in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d2d0-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8d2d0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d2d0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8d2d0-107">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="8d2d0-107">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8d2d0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8d2d0-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8d2d0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8d2d0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8d2d0-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8d2d0-112">Masters.Xml</span><span class="sxs-lookup"><span data-stu-id="8d2d0-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8d2d0-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8d2d0-113">Definition</span></span>

```XML
< xs:element name="Icon" type="Icon_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8d2d0-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8d2d0-114">Elements and attributes</span></span>

<span data-ttu-id="8d2d0-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8d2d0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8d2d0-116">Parent elements</span></span>

|<span data-ttu-id="8d2d0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-117">**Element**</span></span>|<span data-ttu-id="8d2d0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-118">**Type**</span></span>|<span data-ttu-id="8d2d0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8d2d0-120">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="8d2d0-120">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8d2d0-121">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="8d2d0-121">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8d2d0-122">Especifica un formato de patrón no usado.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-122">Specifies an unused master format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8d2d0-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d2d0-123">Child elements</span></span>

<span data-ttu-id="8d2d0-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d2d0-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d2d0-125">Attributes</span></span>

<span data-ttu-id="8d2d0-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-126">None.</span></span>
  

