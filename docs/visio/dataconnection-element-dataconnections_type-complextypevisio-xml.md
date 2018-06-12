---
title: Elemento de DataConnection (DataConnections_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume la comunicación entre uno o varios elementos de DataRecordset y un origen de datos no XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821928"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="784c4-103">Elemento de DataConnection (DataConnections_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="784c4-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="784c4-104">Resume la comunicación entre uno o varios elementos de **DataRecordset** y un origen de datos no XML.</span><span class="sxs-lookup"><span data-stu-id="784c4-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="784c4-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="784c4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="784c4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="784c4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="784c4-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="784c4-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="784c4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="784c4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="784c4-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="784c4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="784c4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="784c4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="784c4-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="784c4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="784c4-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="784c4-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="784c4-113">Definición</span><span class="sxs-lookup"><span data-stu-id="784c4-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="784c4-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="784c4-114">Elements and attributes</span></span>

<span data-ttu-id="784c4-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="784c4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="784c4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="784c4-116">Parent elements</span></span>

|<span data-ttu-id="784c4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="784c4-117">**Element**</span></span>|<span data-ttu-id="784c4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="784c4-118">**Type**</span></span>|<span data-ttu-id="784c4-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="784c4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="784c4-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="784c4-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="784c4-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="784c4-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="784c4-122">Contiene los elementos de **DataConnection** para el documento.</span><span class="sxs-lookup"><span data-stu-id="784c4-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="784c4-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="784c4-123">Child elements</span></span>

<span data-ttu-id="784c4-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="784c4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="784c4-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="784c4-125">Attributes</span></span>

|<span data-ttu-id="784c4-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="784c4-126">**Attribute**</span></span>|<span data-ttu-id="784c4-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="784c4-127">**Type**</span></span>|<span data-ttu-id="784c4-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="784c4-128">**Required**</span></span>|<span data-ttu-id="784c4-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="784c4-129">**Description**</span></span>|<span data-ttu-id="784c4-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="784c4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="784c4-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="784c4-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="784c4-132">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="784c4-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="784c4-133">opcional</span><span class="sxs-lookup"><span data-stu-id="784c4-133">optional</span></span>  <br/> |<span data-ttu-id="784c4-134">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="784c4-134">The default value is false.</span></span> <span data-ttu-id="784c4-135">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="784c4-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="784c4-136">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="784c4-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="784c4-137">Comando</span><span class="sxs-lookup"><span data-stu-id="784c4-137">Command</span></span>  <br/> |<span data-ttu-id="784c4-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="784c4-138">xsd:string</span></span>  <br/> |<span data-ttu-id="784c4-139">opcional</span><span class="sxs-lookup"><span data-stu-id="784c4-139">optional</span></span>  <br/> |<span data-ttu-id="784c4-140">La cadena de comando utilizada para consultar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="784c4-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="784c4-141">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="784c4-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="784c4-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="784c4-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="784c4-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="784c4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="784c4-144">opcional</span><span class="sxs-lookup"><span data-stu-id="784c4-144">optional</span></span>  <br/> |<span data-ttu-id="784c4-145">La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="784c4-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="784c4-146">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="784c4-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="784c4-147">FileName</span><span class="sxs-lookup"><span data-stu-id="784c4-147">FileName</span></span>  <br/> |<span data-ttu-id="784c4-148">xsd: String</span><span class="sxs-lookup"><span data-stu-id="784c4-148">xsd:string</span></span>  <br/> |<span data-ttu-id="784c4-149">necesario</span><span class="sxs-lookup"><span data-stu-id="784c4-149">required</span></span>  <br/> |<span data-ttu-id="784c4-150">El nombre del archivo de conexión.</span><span class="sxs-lookup"><span data-stu-id="784c4-150">The name of the connection file.</span></span> <span data-ttu-id="784c4-151">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="784c4-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="784c4-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="784c4-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="784c4-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="784c4-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="784c4-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="784c4-154">xsd:string</span></span>  <br/> |<span data-ttu-id="784c4-155">opcional</span><span class="sxs-lookup"><span data-stu-id="784c4-155">optional</span></span>  <br/> |<span data-ttu-id="784c4-156">Un nombre proporcionado por el usuario para la conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="784c4-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="784c4-157">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="784c4-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="784c4-158">id.</span><span class="sxs-lookup"><span data-stu-id="784c4-158">ID</span></span>  <br/> |<span data-ttu-id="784c4-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="784c4-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="784c4-160">necesario</span><span class="sxs-lookup"><span data-stu-id="784c4-160">required</span></span>  <br/> |<span data-ttu-id="784c4-161">Identificador asignado por Visio para una conexión determinada, única dentro del documento.</span><span class="sxs-lookup"><span data-stu-id="784c4-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="784c4-162">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="784c4-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="784c4-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="784c4-163">Timeout</span></span>  <br/> |<span data-ttu-id="784c4-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="784c4-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="784c4-165">opcional</span><span class="sxs-lookup"><span data-stu-id="784c4-165">optional</span></span>  <br/> |<span data-ttu-id="784c4-166">El tiempo de espera en minutos al intentar establecer una conexión antes de terminar el intento.</span><span class="sxs-lookup"><span data-stu-id="784c4-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="784c4-167">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="784c4-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

