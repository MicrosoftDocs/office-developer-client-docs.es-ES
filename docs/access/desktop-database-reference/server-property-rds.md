---
title: Propiedad Server (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f35910591d86e0e5a2b92d680be3c5f64504088
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308690"
---
# <a name="server-property-rds"></a>Propiedad Server (RDS)

**Se aplica a:** Access 2013, Office 2013

Indica el nombre y el protocolo de comunicación de Internet Information Services (IIS).

Es posible establecer la propiedad **Server** durante el diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.

## <a name="syntax"></a>Sintaxis

|Protocolo|Sintaxis durante el diseño|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|En proceso|`<PARAM NAME="Server" VALUE="">`|


|Protocolo|Sintaxis en tiempo de ejecución|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|En proceso|`DataControl.Server=""`|


## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*awebsrvr* o *computername* |Un valor de tipo **String** que incluye una ruta de acceso de Internet o intranet o el nombre del equipo si el servidor se encuentra en un equipo remoto; o, si el servidor se encuentra en el equipo local, una cadena vacía.|
|*port* |Opcional. Un puerto que se usa para conectarse a un servidor de IIS. El número de puerto se establece en Internet Explorer (en el menú **Ver**, haga clic en **Opciones de Internet** y, a continuación, seleccione la pestaña **Conexión** ) o en IIS.|
|*DataControl* |Variable de objeto que representa un objeto **RDS.DataControl**.|

## <a name="remarks"></a>Comentarios

El servidor es la ubicación en la que se procesa la solicitud **RDS.DataControl** (es decir, una consulta o actualización). De forma predeterminada, todas las solicitudes son procesadas por el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md), el componente [MSDFMAP.Handler](datafactory-customization.md) y el archivo [MSDFMAP.INI](understanding-the-customization-file.md) en el servidor especificado. 

Recuerde que al cambiar de servidor es necesario reconciliar la configuración de los archivos **MSDFMAP.INI** antiguo y actual. Las incompatibilidades pueden hacer que las solicitudes ejecutadas correctamente en un servidor produzcan un error en otro. Si la propiedad Server está establecida en "", estos objetos se utilizarán en el equipo local.

