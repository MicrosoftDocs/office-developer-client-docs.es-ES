---
title: Elemento REL (complexType DataRecordSet_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Especifica una relación con un elemento con el conjunto de registros y la información de enlace de datos asociados.
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542866"
---
# <a name="rel-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="b59ed-103">Elemento REL (complexType DataRecordSet_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="b59ed-103">Rel element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b59ed-104">Especifica una relación con un elemento con el conjunto de registros y la información de enlace de datos asociados.</span><span class="sxs-lookup"><span data-stu-id="b59ed-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b59ed-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b59ed-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b59ed-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b59ed-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b59ed-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="b59ed-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b59ed-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b59ed-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b59ed-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b59ed-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b59ed-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b59ed-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b59ed-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b59ed-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b59ed-112">Pages. XML, Masters. XML, Recordsets. XML, página #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="b59ed-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b59ed-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b59ed-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b59ed-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b59ed-114">Elements and attributes</span></span>

<span data-ttu-id="b59ed-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b59ed-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b59ed-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b59ed-116">Parent elements</span></span>

|<span data-ttu-id="b59ed-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b59ed-117">**Element**</span></span>|<span data-ttu-id="b59ed-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b59ed-118">**Type**</span></span>|<span data-ttu-id="b59ed-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b59ed-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b59ed-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="b59ed-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b59ed-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="b59ed-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b59ed-122">Especifica una instancia de un objeto Recordset y la información de enlace de datos almacenada en el dibujo.</span><span class="sxs-lookup"><span data-stu-id="b59ed-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b59ed-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b59ed-123">Child elements</span></span>

<span data-ttu-id="b59ed-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b59ed-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b59ed-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="b59ed-125">Attributes</span></span>

|<span data-ttu-id="b59ed-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b59ed-126">**Attribute**</span></span>|<span data-ttu-id="b59ed-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b59ed-127">**Type**</span></span>|<span data-ttu-id="b59ed-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b59ed-128">**Required**</span></span>|<span data-ttu-id="b59ed-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b59ed-129">**Description**</span></span>|<span data-ttu-id="b59ed-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b59ed-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b59ed-131">r:id</span><span class="sxs-lookup"><span data-stu-id="b59ed-131">r:id</span></span>  <br/> |<span data-ttu-id="b59ed-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b59ed-132">xsd:string</span></span>  <br/> <span data-ttu-id="b59ed-133">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b59ed-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="b59ed-134">necesario</span><span class="sxs-lookup"><span data-stu-id="b59ed-134">required</span></span>  <br/> |<span data-ttu-id="b59ed-135">Especifica una relación con un elemento.</span><span class="sxs-lookup"><span data-stu-id="b59ed-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="b59ed-136">"Nº rId"</span><span class="sxs-lookup"><span data-stu-id="b59ed-136">"rId#"</span></span>  <br/> <span data-ttu-id="b59ed-137">Consulte Comentarios.</span><span class="sxs-lookup"><span data-stu-id="b59ed-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b59ed-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b59ed-138">Remarks</span></span>

<span data-ttu-id="b59ed-139">El valor del atributo **r:ID** debe ser un tipo **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="b59ed-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="b59ed-140">El tipo **ST_RelationshipID** es una cadena que debe tener el formato "rId #", donde el último carácter debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="b59ed-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="b59ed-141">El número debe ser único entre todos los elementos del mismo nivel del elemento **REL** .</span><span class="sxs-lookup"><span data-stu-id="b59ed-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="b59ed-142">Para obtener más información acerca del tipo ST_RelationshipID, consulte la [especificación ISO/IEC 29500 parte 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="b59ed-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

