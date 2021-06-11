---
title: Elemento DataConnection (DataConnections_Type complexType) (Visio XML)
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
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="6167e-103">Elemento DataConnection (DataConnections_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6167e-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6167e-104">Abstrae la comunicación entre uno o varios **elementos DataRecordset** y un origen de datos que no es XML.</span><span class="sxs-lookup"><span data-stu-id="6167e-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6167e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6167e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6167e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6167e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6167e-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="6167e-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6167e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6167e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6167e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6167e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6167e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6167e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6167e-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="6167e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6167e-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="6167e-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6167e-113">Definición</span><span class="sxs-lookup"><span data-stu-id="6167e-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6167e-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6167e-114">Elements and attributes</span></span>

<span data-ttu-id="6167e-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6167e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6167e-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6167e-116">Parent elements</span></span>

|<span data-ttu-id="6167e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6167e-117">**Element**</span></span>|<span data-ttu-id="6167e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6167e-118">**Type**</span></span>|<span data-ttu-id="6167e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6167e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6167e-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="6167e-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="6167e-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="6167e-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6167e-122">Contiene los **elementos DataConnection** del documento.</span><span class="sxs-lookup"><span data-stu-id="6167e-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6167e-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6167e-123">Child elements</span></span>

<span data-ttu-id="6167e-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6167e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6167e-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="6167e-125">Attributes</span></span>

|<span data-ttu-id="6167e-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6167e-126">**Attribute**</span></span>|<span data-ttu-id="6167e-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6167e-127">**Type**</span></span>|<span data-ttu-id="6167e-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6167e-128">**Required**</span></span>|<span data-ttu-id="6167e-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6167e-129">**Description**</span></span>|<span data-ttu-id="6167e-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="6167e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6167e-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="6167e-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="6167e-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6167e-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6167e-133">opcional</span><span class="sxs-lookup"><span data-stu-id="6167e-133">optional</span></span>  <br/> |<span data-ttu-id="6167e-134">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="6167e-134">The default value is false.</span></span> <span data-ttu-id="6167e-135">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6167e-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="6167e-136">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6167e-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6167e-137">Comando</span><span class="sxs-lookup"><span data-stu-id="6167e-137">Command</span></span>  <br/> |<span data-ttu-id="6167e-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6167e-138">xsd:string</span></span>  <br/> |<span data-ttu-id="6167e-139">opcional</span><span class="sxs-lookup"><span data-stu-id="6167e-139">optional</span></span>  <br/> |<span data-ttu-id="6167e-140">Cadena de comandos usada para consultar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="6167e-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="6167e-141">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6167e-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6167e-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6167e-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="6167e-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6167e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6167e-144">opcional</span><span class="sxs-lookup"><span data-stu-id="6167e-144">optional</span></span>  <br/> |<span data-ttu-id="6167e-145">La cadena de conexión que define los parámetros necesarios para conectarse a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="6167e-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="6167e-146">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6167e-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6167e-147">FileName</span><span class="sxs-lookup"><span data-stu-id="6167e-147">FileName</span></span>  <br/> |<span data-ttu-id="6167e-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6167e-148">xsd:string</span></span>  <br/> |<span data-ttu-id="6167e-149">necesario</span><span class="sxs-lookup"><span data-stu-id="6167e-149">required</span></span>  <br/> |<span data-ttu-id="6167e-150">Nombre del archivo de conexión.</span><span class="sxs-lookup"><span data-stu-id="6167e-150">The name of the connection file.</span></span> <span data-ttu-id="6167e-151">Para obtener más información, vea los Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6167e-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="6167e-152">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6167e-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6167e-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6167e-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="6167e-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6167e-154">xsd:string</span></span>  <br/> |<span data-ttu-id="6167e-155">opcional</span><span class="sxs-lookup"><span data-stu-id="6167e-155">optional</span></span>  <br/> |<span data-ttu-id="6167e-156">Un usuario proporcionó el nombre para la conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="6167e-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="6167e-157">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6167e-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6167e-158">ID</span><span class="sxs-lookup"><span data-stu-id="6167e-158">ID</span></span>  <br/> |<span data-ttu-id="6167e-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6167e-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6167e-160">necesario</span><span class="sxs-lookup"><span data-stu-id="6167e-160">required</span></span>  <br/> |<span data-ttu-id="6167e-161">El identificador asignado por Visio para una conexión determinada, única en el documento.</span><span class="sxs-lookup"><span data-stu-id="6167e-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="6167e-162">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6167e-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6167e-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="6167e-163">Timeout</span></span>  <br/> |<span data-ttu-id="6167e-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6167e-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6167e-165">opcional</span><span class="sxs-lookup"><span data-stu-id="6167e-165">optional</span></span>  <br/> |<span data-ttu-id="6167e-166">Tiempo de espera en minutos al intentar establecer una conexión antes de finalizar el intento.</span><span class="sxs-lookup"><span data-stu-id="6167e-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="6167e-167">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6167e-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

