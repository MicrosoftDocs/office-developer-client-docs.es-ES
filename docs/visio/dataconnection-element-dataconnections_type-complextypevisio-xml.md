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
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="13840-103">Elemento de DataConnection (DataConnections_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="13840-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="13840-104">Resume la comunicación entre uno o varios elementos de **DataRecordset** y un origen de datos no XML.</span><span class="sxs-lookup"><span data-stu-id="13840-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="13840-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13840-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13840-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="13840-106">**Element type**</span></span> <br/> |[<span data-ttu-id="13840-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="13840-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="13840-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13840-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="13840-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="13840-109">**Schema file**</span></span> <br/> |<span data-ttu-id="13840-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="13840-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="13840-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="13840-111">**Document parts**</span></span> <br/> |<span data-ttu-id="13840-112">Connections.Xml</span><span class="sxs-lookup"><span data-stu-id="13840-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13840-113">Definición</span><span class="sxs-lookup"><span data-stu-id="13840-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="13840-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="13840-114">Elements and attributes</span></span>

<span data-ttu-id="13840-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="13840-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="13840-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13840-116">Parent elements</span></span>

|<span data-ttu-id="13840-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="13840-117">**Element**</span></span>|<span data-ttu-id="13840-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13840-118">**Type**</span></span>|<span data-ttu-id="13840-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13840-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13840-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="13840-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="13840-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="13840-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="13840-122">Contiene los elementos de **DataConnection** para el documento.</span><span class="sxs-lookup"><span data-stu-id="13840-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13840-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13840-123">Child elements</span></span>

<span data-ttu-id="13840-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="13840-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13840-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="13840-125">Attributes</span></span>

|<span data-ttu-id="13840-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="13840-126">**Attribute**</span></span>|<span data-ttu-id="13840-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13840-127">**Type**</span></span>|<span data-ttu-id="13840-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="13840-128">**Required**</span></span>|<span data-ttu-id="13840-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13840-129">**Description**</span></span>|<span data-ttu-id="13840-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="13840-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13840-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="13840-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="13840-132">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="13840-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13840-133">opcional</span><span class="sxs-lookup"><span data-stu-id="13840-133">optional</span></span>  <br/> |<span data-ttu-id="13840-134">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="13840-134">The default value is false.</span></span> <span data-ttu-id="13840-135">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="13840-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="13840-136">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="13840-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13840-137">Comando</span><span class="sxs-lookup"><span data-stu-id="13840-137">Command</span></span>  <br/> |<span data-ttu-id="13840-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="13840-138">xsd:string</span></span>  <br/> |<span data-ttu-id="13840-139">opcional</span><span class="sxs-lookup"><span data-stu-id="13840-139">optional</span></span>  <br/> |<span data-ttu-id="13840-140">La cadena de comando utilizada para consultar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="13840-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="13840-141">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="13840-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13840-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="13840-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="13840-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="13840-143">xsd:string</span></span>  <br/> |<span data-ttu-id="13840-144">opcional</span><span class="sxs-lookup"><span data-stu-id="13840-144">optional</span></span>  <br/> |<span data-ttu-id="13840-145">La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="13840-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="13840-146">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="13840-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13840-147">FileName</span><span class="sxs-lookup"><span data-stu-id="13840-147">FileName</span></span>  <br/> |<span data-ttu-id="13840-148">xsd: String</span><span class="sxs-lookup"><span data-stu-id="13840-148">xsd:string</span></span>  <br/> |<span data-ttu-id="13840-149">necesario</span><span class="sxs-lookup"><span data-stu-id="13840-149">required</span></span>  <br/> |<span data-ttu-id="13840-150">El nombre del archivo de conexión.</span><span class="sxs-lookup"><span data-stu-id="13840-150">The name of the connection file.</span></span> <span data-ttu-id="13840-151">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="13840-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="13840-152">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="13840-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13840-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="13840-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="13840-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="13840-154">xsd:string</span></span>  <br/> |<span data-ttu-id="13840-155">opcional</span><span class="sxs-lookup"><span data-stu-id="13840-155">optional</span></span>  <br/> |<span data-ttu-id="13840-156">Un nombre proporcionado por el usuario para la conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="13840-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="13840-157">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="13840-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13840-158">ID</span><span class="sxs-lookup"><span data-stu-id="13840-158">ID</span></span>  <br/> |<span data-ttu-id="13840-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13840-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13840-160">necesario</span><span class="sxs-lookup"><span data-stu-id="13840-160">required</span></span>  <br/> |<span data-ttu-id="13840-161">Identificador asignado por Visio para una conexión determinada, única dentro del documento.</span><span class="sxs-lookup"><span data-stu-id="13840-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="13840-162">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13840-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13840-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="13840-163">Timeout</span></span>  <br/> |<span data-ttu-id="13840-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13840-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13840-165">opcional</span><span class="sxs-lookup"><span data-stu-id="13840-165">optional</span></span>  <br/> |<span data-ttu-id="13840-166">El tiempo de espera en minutos al intentar establecer una conexión antes de terminar el intento.</span><span class="sxs-lookup"><span data-stu-id="13840-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="13840-167">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13840-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

