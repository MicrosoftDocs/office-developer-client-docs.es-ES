---
title: Server (propiedad, RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492602d7150f3080df329d30a38e3af51755cf0f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949506"
---
# <a name="server-property-rds"></a><span data-ttu-id="3fb30-102">Server (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="3fb30-102">Server property (RDS)</span></span>

<span data-ttu-id="3fb30-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fb30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fb30-104">Indica el nombre y el protocolo de comunicación de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="3fb30-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="3fb30-105">Es posible establecer la propiedad **Server** durante el diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.</span><span class="sxs-lookup"><span data-stu-id="3fb30-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb30-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fb30-106">Syntax</span></span>

|<span data-ttu-id="3fb30-107">Protocolo</span><span class="sxs-lookup"><span data-stu-id="3fb30-107">Protocol</span></span>|<span data-ttu-id="3fb30-108">Sintaxis durante el diseño</span><span class="sxs-lookup"><span data-stu-id="3fb30-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="3fb30-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="3fb30-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="3fb30-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3fb30-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="3fb30-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="3fb30-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="3fb30-112">En proceso</span><span class="sxs-lookup"><span data-stu-id="3fb30-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="3fb30-113">Protocolo</span><span class="sxs-lookup"><span data-stu-id="3fb30-113">Protocol</span></span>|<span data-ttu-id="3fb30-114">Sintaxis en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="3fb30-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="3fb30-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="3fb30-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="3fb30-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3fb30-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="3fb30-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="3fb30-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="3fb30-118">En proceso</span><span class="sxs-lookup"><span data-stu-id="3fb30-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="3fb30-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fb30-119">Parameters</span></span>

|<span data-ttu-id="3fb30-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3fb30-120">Parameter</span></span>|<span data-ttu-id="3fb30-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fb30-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3fb30-122">*awebsrvr* o *computername*</span><span class="sxs-lookup"><span data-stu-id="3fb30-122">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="3fb30-123">Un valor de tipo **String** que incluye una ruta de acceso de Internet o intranet o el nombre del equipo si el servidor se encuentra en un equipo remoto; o, si el servidor se encuentra en el equipo local, una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="3fb30-123">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>|
|<span data-ttu-id="3fb30-124">*port*</span><span class="sxs-lookup"><span data-stu-id="3fb30-124">*port*</span></span> |<span data-ttu-id="3fb30-p101">Opcional. Un puerto que se usa para conectarse a un servidor de IIS. El número de puerto se establece en Internet Explorer (en el menú **Ver**, haga clic en **Opciones de Internet** y, a continuación, seleccione la pestaña **Conexión** ) o en IIS.</span><span class="sxs-lookup"><span data-stu-id="3fb30-p101">Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>|
|<span data-ttu-id="3fb30-128">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3fb30-128">*DataControl*</span></span> |<span data-ttu-id="3fb30-129">Variable de objeto que representa un objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="3fb30-129">An object variable that represents an **RDS.DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3fb30-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fb30-130">Remarks</span></span>

<span data-ttu-id="3fb30-131">El servidor es la ubicación en la que se procesa la solicitud **RDS.DataControl** (es decir, una consulta o actualización).</span><span class="sxs-lookup"><span data-stu-id="3fb30-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="3fb30-132">De forma predeterminada, todas las solicitudes son procesadas por el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), el componente [MSDFMAP.Handler](datafactory-customization.md) y el archivo [MSDFMAP.INI](understanding-the-customization-file.md) en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3fb30-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="3fb30-133">Recuerde que al cambiar de servidor es necesario reconciliar la configuración de los archivos **MSDFMAP.INI** antiguo y actual.</span><span class="sxs-lookup"><span data-stu-id="3fb30-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="3fb30-134">Las incompatibilidades pueden hacer que las solicitudes ejecutadas correctamente en un servidor produzcan un error en otro.</span><span class="sxs-lookup"><span data-stu-id="3fb30-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="3fb30-135">Si la propiedad Server está establecida en "", estos objetos se utilizarán en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="3fb30-135">If the Server property is set to "", these objects will be used on the local machine.</span></span>

