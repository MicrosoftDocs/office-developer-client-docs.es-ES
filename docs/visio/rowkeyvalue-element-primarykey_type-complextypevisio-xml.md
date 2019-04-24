---
title: Elemento RowKeyValue (complexType PrimaryKey_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Especifica el valor de una clave principal para una fila individual de un objeto Recordset.
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283506"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="e553c-103">Elemento RowKeyValue (complexType PrimaryKey_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="e553c-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e553c-104">Especifica el valor de una clave principal para una fila individual de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="e553c-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e553c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e553c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e553c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="e553c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e553c-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="e553c-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e553c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e553c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e553c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e553c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e553c-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e553c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e553c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="e553c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e553c-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="e553c-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e553c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="e553c-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e553c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e553c-114">Elements and attributes</span></span>

<span data-ttu-id="e553c-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e553c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e553c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e553c-116">Parent elements</span></span>

|<span data-ttu-id="e553c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e553c-117">**Element**</span></span>|<span data-ttu-id="e553c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e553c-118">**Type**</span></span>|<span data-ttu-id="e553c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e553c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e553c-120">ClavePrincipal</span><span class="sxs-lookup"><span data-stu-id="e553c-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e553c-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="e553c-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e553c-122">Especifica una clave principal de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="e553c-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e553c-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e553c-123">Child elements</span></span>

<span data-ttu-id="e553c-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e553c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e553c-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="e553c-125">Attributes</span></span>

|<span data-ttu-id="e553c-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e553c-126">**Attribute**</span></span>|<span data-ttu-id="e553c-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e553c-127">**Type**</span></span>|<span data-ttu-id="e553c-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e553c-128">**Required**</span></span>|<span data-ttu-id="e553c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e553c-129">**Description**</span></span>|<span data-ttu-id="e553c-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="e553c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e553c-131">Pseudocolumna</span><span class="sxs-lookup"><span data-stu-id="e553c-131">RowID</span></span>  <br/> |<span data-ttu-id="e553c-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e553c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e553c-133">necesario</span><span class="sxs-lookup"><span data-stu-id="e553c-133">required</span></span>  <br/> |<span data-ttu-id="e553c-134">Un valor único que identifica una fila de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="e553c-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="e553c-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e553c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e553c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e553c-136">Value</span></span>  <br/> |<span data-ttu-id="e553c-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e553c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e553c-138">necesario</span><span class="sxs-lookup"><span data-stu-id="e553c-138">required</span></span>  <br/> |<span data-ttu-id="e553c-139">El valor de la clave principal de esta fila del objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="e553c-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="e553c-140">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e553c-140">Values of the xsd:string type.</span></span>  <br/> |
   

