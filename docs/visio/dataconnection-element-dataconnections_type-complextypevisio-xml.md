---
title: Elemento DataConnection (complexType DataConnections_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Abstrae la comunicación entre uno o varios elementos DataRecordset y un origen de datos que no es XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538406"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="bd3e8-103">Elemento DataConnection (complexType DataConnections_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="bd3e8-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="bd3e8-104">Abstrae la comunicación entre uno o varios elementos **DataRecordset** y un origen de datos que no es XML.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="bd3e8-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bd3e8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd3e8-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bd3e8-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="bd3e8-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bd3e8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bd3e8-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bd3e8-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="bd3e8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bd3e8-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bd3e8-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="bd3e8-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd3e8-113">Definición</span><span class="sxs-lookup"><span data-stu-id="bd3e8-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bd3e8-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="bd3e8-114">Elements and attributes</span></span>

<span data-ttu-id="bd3e8-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bd3e8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bd3e8-116">Parent elements</span></span>

|<span data-ttu-id="bd3e8-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-117">**Element**</span></span>|<span data-ttu-id="bd3e8-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-118">**Type**</span></span>|<span data-ttu-id="bd3e8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bd3e8-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="bd3e8-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="bd3e8-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="bd3e8-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bd3e8-122">Contiene los elementos **DataConnection** del documento.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bd3e8-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bd3e8-123">Child elements</span></span>

<span data-ttu-id="bd3e8-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd3e8-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd3e8-125">Attributes</span></span>

|<span data-ttu-id="bd3e8-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-126">**Attribute**</span></span>|<span data-ttu-id="bd3e8-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-127">**Type**</span></span>|<span data-ttu-id="bd3e8-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-128">**Required**</span></span>|<span data-ttu-id="bd3e8-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-129">**Description**</span></span>|<span data-ttu-id="bd3e8-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="bd3e8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd3e8-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="bd3e8-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="bd3e8-132">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="bd3e8-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bd3e8-133">opcional</span><span class="sxs-lookup"><span data-stu-id="bd3e8-133">optional</span></span>  <br/> |<span data-ttu-id="bd3e8-134">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-134">The default value is false.</span></span> <span data-ttu-id="bd3e8-135">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="bd3e8-136">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bd3e8-137">Command</span><span class="sxs-lookup"><span data-stu-id="bd3e8-137">Command</span></span>  <br/> |<span data-ttu-id="bd3e8-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bd3e8-138">xsd:string</span></span>  <br/> |<span data-ttu-id="bd3e8-139">opcional</span><span class="sxs-lookup"><span data-stu-id="bd3e8-139">optional</span></span>  <br/> |<span data-ttu-id="bd3e8-140">La cadena de comando usada para consultar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="bd3e8-141">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bd3e8-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bd3e8-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="bd3e8-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bd3e8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="bd3e8-144">opcional</span><span class="sxs-lookup"><span data-stu-id="bd3e8-144">optional</span></span>  <br/> |<span data-ttu-id="bd3e8-145">La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="bd3e8-146">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bd3e8-147">FileName</span><span class="sxs-lookup"><span data-stu-id="bd3e8-147">FileName</span></span>  <br/> |<span data-ttu-id="bd3e8-148">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bd3e8-148">xsd:string</span></span>  <br/> |<span data-ttu-id="bd3e8-149">necesario</span><span class="sxs-lookup"><span data-stu-id="bd3e8-149">required</span></span>  <br/> |<span data-ttu-id="bd3e8-150">El nombre del archivo de conexión.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-150">The name of the connection file.</span></span> <span data-ttu-id="bd3e8-151">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="bd3e8-152">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bd3e8-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bd3e8-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="bd3e8-154">xsd: String</span><span class="sxs-lookup"><span data-stu-id="bd3e8-154">xsd:string</span></span>  <br/> |<span data-ttu-id="bd3e8-155">opcional</span><span class="sxs-lookup"><span data-stu-id="bd3e8-155">optional</span></span>  <br/> |<span data-ttu-id="bd3e8-156">Un nombre de usuario proporcionado para la conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="bd3e8-157">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bd3e8-158">ID</span><span class="sxs-lookup"><span data-stu-id="bd3e8-158">ID</span></span>  <br/> |<span data-ttu-id="bd3e8-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd3e8-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd3e8-160">necesario</span><span class="sxs-lookup"><span data-stu-id="bd3e8-160">required</span></span>  <br/> |<span data-ttu-id="bd3e8-161">IDENTIFICADOR asignado por Visio para una conexión determinada, único dentro del documento.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="bd3e8-162">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd3e8-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="bd3e8-163">Timeout</span></span>  <br/> |<span data-ttu-id="bd3e8-164">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd3e8-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd3e8-165">opcional</span><span class="sxs-lookup"><span data-stu-id="bd3e8-165">optional</span></span>  <br/> |<span data-ttu-id="bd3e8-166">Tiempo de espera en minutos al intentar establecer una conexión antes de terminar el intento.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="bd3e8-167">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd3e8-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

