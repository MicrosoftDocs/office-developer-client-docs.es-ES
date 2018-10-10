---
title: Server (propiedad, RDS)
TOCTitle: Server Property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec001c57f72582dcdaabdfd6e76069582468b54c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483373"
---
# <a name="server-property-rds"></a><span data-ttu-id="da009-102">Server (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="da009-102">Server Property (RDS)</span></span>


<span data-ttu-id="da009-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="da009-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="da009-104">Indica el nombre y el protocolo de comunicación de Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="da009-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="da009-105">Es posible establecer la propiedad **Server** durante el diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.</span><span class="sxs-lookup"><span data-stu-id="da009-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="da009-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da009-106">Syntax</span></span>

|<span data-ttu-id="da009-107">Protocolo</span><span class="sxs-lookup"><span data-stu-id="da009-107">Protocol</span></span>|<span data-ttu-id="da009-108">Sintaxis durante el diseño</span><span class="sxs-lookup"><span data-stu-id="da009-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="da009-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="da009-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="da009-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="da009-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="da009-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="da009-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="da009-112">En proceso</span><span class="sxs-lookup"><span data-stu-id="da009-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="da009-113">Protocolo</span><span class="sxs-lookup"><span data-stu-id="da009-113">Protocol</span></span>|<span data-ttu-id="da009-114">Sintaxis en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="da009-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="da009-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="da009-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="da009-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="da009-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="da009-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="da009-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="da009-118">En proceso</span><span class="sxs-lookup"><span data-stu-id="da009-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="da009-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da009-119">Parameters</span></span>

<span data-ttu-id="da009-120">*awebsrvr* o *computername*</span><span class="sxs-lookup"><span data-stu-id="da009-120">*awebsrvr* or *computername*</span></span>

- <span data-ttu-id="da009-121">Un valor de tipo **String** que incluye una ruta de acceso de Internet o intranet o el nombre del equipo si el servidor se encuentra en un equipo remoto; o, si el servidor se encuentra en el equipo local, una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="da009-121">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>

<span data-ttu-id="da009-122">*port*</span><span class="sxs-lookup"><span data-stu-id="da009-122">*port*</span></span>

- <span data-ttu-id="da009-p101">Opcional. Un puerto que se usa para conectarse a un servidor de IIS. El número de puerto se establece en Internet Explorer (en el menú **Ver**, haga clic en **Opciones de Internet** y, a continuación, seleccione la pestaña **Conexión** ) o en IIS.</span><span class="sxs-lookup"><span data-stu-id="da009-p101">Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>

<span data-ttu-id="da009-126">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="da009-126">*DataControl*</span></span>

- <span data-ttu-id="da009-127">Variable de objeto que representa un objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="da009-127">An object variable that represents an **RDS.DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da009-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da009-128">Remarks</span></span>

<span data-ttu-id="da009-129">El servidor es la ubicación en la que se procesa la solicitud **RDS.DataControl** (es decir, una consulta o actualización).</span><span class="sxs-lookup"><span data-stu-id="da009-129">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="da009-130">De forma predeterminada, todas las solicitudes son procesadas por el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), el componente [MSDFMAP.Handler](datafactory-customization.md) y el archivo [MSDFMAP.INI](understanding-the-customization-file.md) en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="da009-130">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="da009-131">Recuerde que al cambiar de servidor es necesario reconciliar la configuración de los archivos **MSDFMAP.INI** antiguo y actual.</span><span class="sxs-lookup"><span data-stu-id="da009-131">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="da009-132">Las incompatibilidades pueden hacer que las solicitudes ejecutadas correctamente en un servidor produzcan un error en otro.</span><span class="sxs-lookup"><span data-stu-id="da009-132">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="da009-133">Si la propiedad Server está establecida en "", estos objetos se utilizarán en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="da009-133">If the Server property is set to "", these objects will be used on the local machine.</span></span>

