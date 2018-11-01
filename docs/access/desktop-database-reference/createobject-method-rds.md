---
title: CreateObject (método, RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87bba22a6563c92e78b5dff3f737c0963de51cb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867394"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="b32fe-102">CreateObject (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="b32fe-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="b32fe-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b32fe-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b32fe-p101">Crea el proxy para el objeto de negocio de destino y devuelve un puntero al mismo. El proxy empaqueta y calcula las referencias de los datos en el código auxiliar de servidor para permitir la comunicación con el objeto de negocio y enviar solicitudes y datos a través de Internet. Para los objetos componentes en proceso, no se utiliza ningún proxy; solo se proporciona un puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="b32fe-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32fe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b32fe-107">Syntax</span></span>

<span data-ttu-id="b32fe-108">El Servicio de datos remotos (RDS) admite los protocolos siguientes: HTTP, HTTPS (HTTP a través de Capa de sockets seguros), DCOM y en proceso.</span><span class="sxs-lookup"><span data-stu-id="b32fe-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b32fe-109">Protocolo</span><span class="sxs-lookup"><span data-stu-id="b32fe-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="b32fe-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b32fe-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b32fe-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="b32fe-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="b32fe-112"><em>Objeto</em>de conjunto de = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="b32fe-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32fe-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b32fe-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b32fe-114"><em>Objeto</em>de conjunto de = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="b32fe-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32fe-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="b32fe-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="b32fe-116"><em>Objeto</em>de conjunto de = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>nombreDeEquipo</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="b32fe-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32fe-117">En proceso</span><span class="sxs-lookup"><span data-stu-id="b32fe-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="b32fe-118"><em>Objeto</em>de conjunto de = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="b32fe-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="b32fe-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b32fe-119">Parameters</span></span>

  - <span data-ttu-id="b32fe-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="b32fe-120">*Object*</span></span>

  - <span data-ttu-id="b32fe-121">Variable de objeto que da como resultado un objeto que es el tipo especificado en *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="b32fe-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="b32fe-122">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="b32fe-122">*DataSpace*</span></span>

  - <span data-ttu-id="b32fe-123">Variable de objeto que representa un objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para crear una instancia del objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="b32fe-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="b32fe-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="b32fe-124">*ProgID*</span></span>

  - <span data-ttu-id="b32fe-125">Valor de tipo **String** que contiene el identificador de programación que especifica un objeto de negocio de servidor que implementa las reglas de negocios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b32fe-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="b32fe-126">*awebsrvr* o *computername*</span><span class="sxs-lookup"><span data-stu-id="b32fe-126">*awebsrvr* or *computername*</span></span>

  - <span data-ttu-id="b32fe-127">Un valor de **tipo String** que representa una dirección URL que identifica el servidor web de Internet Information Services (IIS) donde se crea una instancia del objeto de negocio de servidor.</span><span class="sxs-lookup"><span data-stu-id="b32fe-127">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32fe-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b32fe-128">Remarks</span></span>

<span data-ttu-id="b32fe-129">El *protocolo HTTP* es el protocolo web estándar; *HTTPS* es un protocolo web seguro.</span><span class="sxs-lookup"><span data-stu-id="b32fe-129">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="b32fe-130">Usar el *protocolo DCOM* cuando ejecute una red de área local sin HTTP.</span><span class="sxs-lookup"><span data-stu-id="b32fe-130">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="b32fe-131">El protocolo *en proceso* es una biblioteca de vínculos dinámicos (DLL); local no se usa una red.</span><span class="sxs-lookup"><span data-stu-id="b32fe-131">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

