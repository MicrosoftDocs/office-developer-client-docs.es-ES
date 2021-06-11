---
title: Elemento Rel (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Especifica una relación con una parte con el conjunto de registros asociado y la información de enlace de datos.
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542866"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="f1f76-103">Elemento Rel (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f1f76-103">Rel element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f1f76-104">Especifica una relación con una parte con el conjunto de registros asociado y la información de enlace de datos.</span><span class="sxs-lookup"><span data-stu-id="f1f76-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1f76-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1f76-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1f76-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f1f76-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f1f76-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f1f76-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f1f76-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f1f76-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f1f76-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f1f76-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f1f76-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f1f76-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f1f76-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f1f76-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f1f76-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="f1f76-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1f76-113">Definición</span><span class="sxs-lookup"><span data-stu-id="f1f76-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1f76-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f1f76-114">Elements and attributes</span></span>

<span data-ttu-id="f1f76-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f1f76-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f1f76-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1f76-116">Parent elements</span></span>

|<span data-ttu-id="f1f76-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f1f76-117">**Element**</span></span>|<span data-ttu-id="f1f76-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f1f76-118">**Type**</span></span>|<span data-ttu-id="f1f76-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1f76-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1f76-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1f76-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1f76-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="f1f76-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1f76-122">Especifica una instancia de un conjunto de registros y la información de enlace de datos almacenada en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="f1f76-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f1f76-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1f76-123">Child elements</span></span>

<span data-ttu-id="f1f76-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1f76-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1f76-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1f76-125">Attributes</span></span>

|<span data-ttu-id="f1f76-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f1f76-126">**Attribute**</span></span>|<span data-ttu-id="f1f76-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f1f76-127">**Type**</span></span>|<span data-ttu-id="f1f76-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f1f76-128">**Required**</span></span>|<span data-ttu-id="f1f76-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1f76-129">**Description**</span></span>|<span data-ttu-id="f1f76-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f1f76-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f1f76-131">r:id</span><span class="sxs-lookup"><span data-stu-id="f1f76-131">r:id</span></span>  <br/> |<span data-ttu-id="f1f76-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f1f76-132">xsd:string</span></span>  <br/> <span data-ttu-id="f1f76-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f1f76-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="f1f76-134">necesario</span><span class="sxs-lookup"><span data-stu-id="f1f76-134">required</span></span>  <br/> |<span data-ttu-id="f1f76-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="f1f76-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="f1f76-136">"rId#"</span><span class="sxs-lookup"><span data-stu-id="f1f76-136">"rId#"</span></span>  <br/> <span data-ttu-id="f1f76-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f1f76-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1f76-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1f76-138">Remarks</span></span>

<span data-ttu-id="f1f76-139">El valor del atributo **r:id** debe ser **ST_RelationshipID** tipo.</span><span class="sxs-lookup"><span data-stu-id="f1f76-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="f1f76-140">El **ST_RelationshipID** es una cadena que debe tener el formato 'rId#', donde el carácter final debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="f1f76-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="f1f76-141">El número debe ser único entre todos los elementos del mismo nivel del **elemento Rel.**</span><span class="sxs-lookup"><span data-stu-id="f1f76-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="f1f76-142">Para obtener más información acerca del tipo ST_RelationshipID, vea la especificación [ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="f1f76-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

