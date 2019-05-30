---
title: Elemento RowKeyValue (complexType PrimaryKey_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Especifica el valor de una clave principal para una fila individual de un objeto Recordset.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538133"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="c75f5-103">Elemento RowKeyValue (complexType PrimaryKey_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="c75f5-103">RowKeyValue element (PrimaryKey_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c75f5-104">Especifica el valor de una clave principal para una fila individual de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="c75f5-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c75f5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c75f5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c75f5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c75f5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c75f5-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="c75f5-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c75f5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c75f5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c75f5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c75f5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c75f5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c75f5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c75f5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c75f5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c75f5-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="c75f5-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c75f5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c75f5-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c75f5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c75f5-114">Elements and attributes</span></span>

<span data-ttu-id="c75f5-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c75f5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c75f5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c75f5-116">Parent elements</span></span>

|<span data-ttu-id="c75f5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c75f5-117">**Element**</span></span>|<span data-ttu-id="c75f5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c75f5-118">**Type**</span></span>|<span data-ttu-id="c75f5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c75f5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c75f5-120">ClavePrincipal</span><span class="sxs-lookup"><span data-stu-id="c75f5-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c75f5-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="c75f5-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c75f5-122">Especifica una clave principal de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="c75f5-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c75f5-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c75f5-123">Child elements</span></span>

<span data-ttu-id="c75f5-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c75f5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c75f5-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="c75f5-125">Attributes</span></span>

|<span data-ttu-id="c75f5-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c75f5-126">**Attribute**</span></span>|<span data-ttu-id="c75f5-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c75f5-127">**Type**</span></span>|<span data-ttu-id="c75f5-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c75f5-128">**Required**</span></span>|<span data-ttu-id="c75f5-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c75f5-129">**Description**</span></span>|<span data-ttu-id="c75f5-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c75f5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c75f5-131">Pseudocolumna</span><span class="sxs-lookup"><span data-stu-id="c75f5-131">RowID</span></span>  <br/> |<span data-ttu-id="c75f5-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c75f5-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c75f5-133">necesario</span><span class="sxs-lookup"><span data-stu-id="c75f5-133">required</span></span>  <br/> |<span data-ttu-id="c75f5-134">Un valor único que identifica una fila de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="c75f5-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="c75f5-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c75f5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c75f5-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c75f5-136">Value</span></span>  <br/> |<span data-ttu-id="c75f5-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="c75f5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c75f5-138">necesario</span><span class="sxs-lookup"><span data-stu-id="c75f5-138">required</span></span>  <br/> |<span data-ttu-id="c75f5-139">El valor de la clave principal de esta fila del objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="c75f5-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="c75f5-140">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="c75f5-140">Values of the xsd:string type.</span></span>  <br/> |
   

