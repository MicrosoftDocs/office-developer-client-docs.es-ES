---
title: Elemento DataConnection (complexType DataConnections_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrae la comunicación entre uno o varios elementos DataRecordset y un origen de datos que no es XML.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344628"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="5e0c3-103">Elemento DataConnection (complexType DataConnections_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="5e0c3-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5e0c3-104">Abstrae la comunicación entre uno o varios elementos **DataRecordset** y un origen de datos que no es XML.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5e0c3-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5e0c3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e0c3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5e0c3-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="5e0c3-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5e0c3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5e0c3-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5e0c3-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="5e0c3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5e0c3-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5e0c3-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="5e0c3-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5e0c3-113">Definición</span><span class="sxs-lookup"><span data-stu-id="5e0c3-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5e0c3-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5e0c3-114">Elements and attributes</span></span>

<span data-ttu-id="5e0c3-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5e0c3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5e0c3-116">Parent elements</span></span>

|<span data-ttu-id="5e0c3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-117">**Element**</span></span>|<span data-ttu-id="5e0c3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-118">**Type**</span></span>|<span data-ttu-id="5e0c3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5e0c3-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="5e0c3-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="5e0c3-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="5e0c3-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5e0c3-122">Contiene los elementos **DataConnection** del documento.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5e0c3-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5e0c3-123">Child elements</span></span>

<span data-ttu-id="5e0c3-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e0c3-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e0c3-125">Attributes</span></span>

|<span data-ttu-id="5e0c3-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-126">**Attribute**</span></span>|<span data-ttu-id="5e0c3-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-127">**Type**</span></span>|<span data-ttu-id="5e0c3-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-128">**Required**</span></span>|<span data-ttu-id="5e0c3-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-129">**Description**</span></span>|<span data-ttu-id="5e0c3-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="5e0c3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5e0c3-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="5e0c3-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="5e0c3-132">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="5e0c3-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5e0c3-133">opcional</span><span class="sxs-lookup"><span data-stu-id="5e0c3-133">optional</span></span>  <br/> |<span data-ttu-id="5e0c3-134">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-134">The default value is false.</span></span> <span data-ttu-id="5e0c3-135">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="5e0c3-136">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5e0c3-137">Command</span><span class="sxs-lookup"><span data-stu-id="5e0c3-137">Command</span></span>  <br/> |<span data-ttu-id="5e0c3-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5e0c3-138">xsd:string</span></span>  <br/> |<span data-ttu-id="5e0c3-139">opcional</span><span class="sxs-lookup"><span data-stu-id="5e0c3-139">optional</span></span>  <br/> |<span data-ttu-id="5e0c3-140">La cadena de comando usada para consultar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="5e0c3-141">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e0c3-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5e0c3-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="5e0c3-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5e0c3-143">xsd:string</span></span>  <br/> |<span data-ttu-id="5e0c3-144">opcional</span><span class="sxs-lookup"><span data-stu-id="5e0c3-144">optional</span></span>  <br/> |<span data-ttu-id="5e0c3-145">La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="5e0c3-146">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e0c3-147">FileName</span><span class="sxs-lookup"><span data-stu-id="5e0c3-147">FileName</span></span>  <br/> |<span data-ttu-id="5e0c3-148">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5e0c3-148">xsd:string</span></span>  <br/> |<span data-ttu-id="5e0c3-149">necesario</span><span class="sxs-lookup"><span data-stu-id="5e0c3-149">required</span></span>  <br/> |<span data-ttu-id="5e0c3-150">El nombre del archivo de conexión.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-150">The name of the connection file.</span></span> <span data-ttu-id="5e0c3-151">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="5e0c3-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e0c3-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5e0c3-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="5e0c3-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="5e0c3-154">xsd:string</span></span>  <br/> |<span data-ttu-id="5e0c3-155">opcional</span><span class="sxs-lookup"><span data-stu-id="5e0c3-155">optional</span></span>  <br/> |<span data-ttu-id="5e0c3-156">Un nombre de usuario proporcionado para la conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="5e0c3-157">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5e0c3-158">ID</span><span class="sxs-lookup"><span data-stu-id="5e0c3-158">ID</span></span>  <br/> |<span data-ttu-id="5e0c3-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e0c3-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5e0c3-160">necesario</span><span class="sxs-lookup"><span data-stu-id="5e0c3-160">required</span></span>  <br/> |<span data-ttu-id="5e0c3-161">IDENTIFICADOR asignado por Visio para una conexión determinada, único dentro del documento.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="5e0c3-162">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5e0c3-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="5e0c3-163">Timeout</span></span>  <br/> |<span data-ttu-id="5e0c3-164">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5e0c3-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5e0c3-165">opcional</span><span class="sxs-lookup"><span data-stu-id="5e0c3-165">optional</span></span>  <br/> |<span data-ttu-id="5e0c3-166">Tiempo de espera en minutos al intentar establecer una conexión antes de terminar el intento.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="5e0c3-167">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5e0c3-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

