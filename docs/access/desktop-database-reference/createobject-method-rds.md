---
title: Método CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295376"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="0e2fc-102">Método CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="0e2fc-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="0e2fc-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e2fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e2fc-p101">Crea el proxy para el objeto de negocio de destino y devuelve un puntero al mismo. El proxy empaqueta y calcula las referencias de los datos en el código auxiliar de servidor para permitir la comunicación con el objeto de negocio y enviar solicitudes y datos a través de Internet. Para los objetos componentes en proceso, no se utiliza ningún proxy; solo se proporciona un puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2fc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e2fc-107">Syntax</span></span>

<span data-ttu-id="0e2fc-108">El Servicio de datos remotos (RDS) admite los protocolos siguientes: HTTP, HTTPS (HTTP a través de Capa de sockets seguros), DCOM y en proceso.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e2fc-109">Protocolo</span><span class="sxs-lookup"><span data-stu-id="0e2fc-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="0e2fc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e2fc-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e2fc-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="0e2fc-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="0e2fc-112">Establecer<em>objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="0e2fc-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2fc-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="0e2fc-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="0e2fc-114">Establecer<em>objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>https://awebsrvr</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="0e2fc-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e2fc-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="0e2fc-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="0e2fc-116">Establecer<em>objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; <em>computername</em> &quot; )</span><span class="sxs-lookup"><span data-stu-id="0e2fc-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2fc-117">En proceso</span><span class="sxs-lookup"><span data-stu-id="0e2fc-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="0e2fc-118">Establecer<em>objeto</em>  =  <em>DataSpace</em>. CreateObject( &quot; <em>ProgId</em> &quot; , &quot; &quot; )</span><span class="sxs-lookup"><span data-stu-id="0e2fc-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="0e2fc-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e2fc-119">Parameters</span></span>

|<span data-ttu-id="0e2fc-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0e2fc-120">Parameter</span></span>|<span data-ttu-id="0e2fc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e2fc-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0e2fc-122">*Objeto*</span><span class="sxs-lookup"><span data-stu-id="0e2fc-122">*Object*</span></span> |<span data-ttu-id="0e2fc-123">Variable de objeto que da como resultado un objeto que es el tipo especificado en *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="0e2fc-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="0e2fc-124">*DataSpace*</span></span> |<span data-ttu-id="0e2fc-125">Variable de objeto que representa un objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para crear una instancia del objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="0e2fc-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="0e2fc-126">*ProgID*</span></span> |<span data-ttu-id="0e2fc-127">Valor de tipo **String** que contiene el identificador de programación que especifica un objeto de negocio de servidor que implementa las reglas de negocios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="0e2fc-128">*awebsrvr* o *computername*</span><span class="sxs-lookup"><span data-stu-id="0e2fc-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="0e2fc-129">Valor **string** que representa una dirección URL que identifica el servidor web Internet Information Services (IIS) donde se crea una instancia del objeto de negocio del servidor.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0e2fc-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e2fc-130">Remarks</span></span>

<span data-ttu-id="0e2fc-131">El *protocolo HTTP* es el protocolo web estándar; *HTTPS* es un protocolo web seguro.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="0e2fc-132">Utilice el *protocolo DCOM* cuando ejecute una red de área local sin HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="0e2fc-133">El protocolo *en proceso* es una biblioteca de vínculos dinámicos (DLL) local; no utiliza una red.</span><span class="sxs-lookup"><span data-stu-id="0e2fc-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

