---
title: Windows_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346448"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="eba20-102">Windows_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="eba20-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="eba20-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="eba20-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eba20-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eba20-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eba20-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="eba20-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eba20-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="eba20-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eba20-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="eba20-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eba20-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eba20-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eba20-109">Definición</span><span class="sxs-lookup"><span data-stu-id="eba20-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eba20-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="eba20-110">Elements and attributes</span></span>

<span data-ttu-id="eba20-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="eba20-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eba20-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eba20-112">Child elements</span></span>

|<span data-ttu-id="eba20-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="eba20-113">**Element**</span></span>|<span data-ttu-id="eba20-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="eba20-114">**Type**</span></span>|<span data-ttu-id="eba20-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eba20-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eba20-116">Window</span><span class="sxs-lookup"><span data-stu-id="eba20-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eba20-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="eba20-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="eba20-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="eba20-118">Attributes</span></span>

|<span data-ttu-id="eba20-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="eba20-119">**Attribute**</span></span>|<span data-ttu-id="eba20-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="eba20-120">**Type**</span></span>|<span data-ttu-id="eba20-121">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="eba20-121">**Required**</span></span>|<span data-ttu-id="eba20-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eba20-122">**Description**</span></span>|<span data-ttu-id="eba20-123">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="eba20-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eba20-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="eba20-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="eba20-125">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="eba20-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="eba20-126">opcional</span><span class="sxs-lookup"><span data-stu-id="eba20-126">optional</span></span>  <br/> ||<span data-ttu-id="eba20-127">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="eba20-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="eba20-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="eba20-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="eba20-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="eba20-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="eba20-130">opcional</span><span class="sxs-lookup"><span data-stu-id="eba20-130">optional</span></span>  <br/> ||<span data-ttu-id="eba20-131">Valores del tipo xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="eba20-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

