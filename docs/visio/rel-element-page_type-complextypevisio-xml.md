---
title: Elemento Rel (Page_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Especifica una relación con un elemento con el XML de página correspondiente.
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542782"
---
# <a name="rel-element-page_type-complextype-visio-xml"></a><span data-ttu-id="881d0-103">Elemento Rel (Page_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="881d0-103">Rel element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="881d0-104">Especifica una relación con un elemento con el XML de página correspondiente.</span><span class="sxs-lookup"><span data-stu-id="881d0-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="881d0-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="881d0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="881d0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="881d0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="881d0-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="881d0-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="881d0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="881d0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="881d0-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="881d0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="881d0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="881d0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="881d0-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="881d0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="881d0-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="881d0-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="881d0-113">Definición</span><span class="sxs-lookup"><span data-stu-id="881d0-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="881d0-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="881d0-114">Elements and attributes</span></span>

<span data-ttu-id="881d0-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="881d0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="881d0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="881d0-116">Parent elements</span></span>

|<span data-ttu-id="881d0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="881d0-117">**Element**</span></span>|<span data-ttu-id="881d0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="881d0-118">**Type**</span></span>|<span data-ttu-id="881d0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="881d0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="881d0-120">Page</span><span class="sxs-lookup"><span data-stu-id="881d0-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="881d0-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="881d0-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="881d0-122">Especifica una instancia de XML de página almacenada en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="881d0-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="881d0-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="881d0-123">Child elements</span></span>

<span data-ttu-id="881d0-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="881d0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="881d0-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="881d0-125">Attributes</span></span>

|<span data-ttu-id="881d0-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="881d0-126">**Attribute**</span></span>|<span data-ttu-id="881d0-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="881d0-127">**Type**</span></span>|<span data-ttu-id="881d0-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="881d0-128">**Required**</span></span>|<span data-ttu-id="881d0-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="881d0-129">**Description**</span></span>|<span data-ttu-id="881d0-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="881d0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="881d0-131">r:id</span><span class="sxs-lookup"><span data-stu-id="881d0-131">r:id</span></span>  <br/> |<span data-ttu-id="881d0-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="881d0-132">xsd:string</span></span>  <br/> <span data-ttu-id="881d0-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="881d0-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="881d0-134">necesario</span><span class="sxs-lookup"><span data-stu-id="881d0-134">required</span></span>  <br/> |<span data-ttu-id="881d0-135">Especifica una relación con una parte.</span><span class="sxs-lookup"><span data-stu-id="881d0-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="881d0-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="881d0-136">"rId#"</span></span>  <br/> <span data-ttu-id="881d0-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="881d0-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="881d0-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="881d0-138">Remarks</span></span>

<span data-ttu-id="881d0-139">El valor del atributo **r:id** debe ser un **ST_RelationshipID** predeterminado.</span><span class="sxs-lookup"><span data-stu-id="881d0-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="881d0-140">El **ST_RelationshipID** es una cadena que debe tener el formato 'rId#', donde el carácter final debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="881d0-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="881d0-141">El número debe ser único entre todos los elementos del mismo nivel del **elemento Rel.**</span><span class="sxs-lookup"><span data-stu-id="881d0-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="881d0-142">Para obtener más información acerca del tipo ST_RelationshipID, vea la especificación [ISO/IEC 29500 Parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="881d0-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

