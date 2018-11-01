---
title: Garantizar espacio suficiente para la base de datos temporal
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b08980b7bb852a497ea339f4c43d439ac16a7e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885769"
---
# <a name="ensuring-sufficient-tempdb-space"></a>Garantizar espacio suficiente para la base de datos temporal


**Se aplica a**: Access 2013, Office 2013

Si se producen errores mientras se procesan objetos [Recordset](recordset-object-ado.md) que requieren espacio de procesamiento en Microsoft SQL Server 6.5, puede que sea necesario aumentar el tamaño de la base de datos temporal (TempDB). Algunas consultas requieren espacio de procesamiento temporal; por ejemplo, una consulta con una cláusula ORDER BY necesita ordenar el objeto **Recordset**, lo cual requiere algo de espacio temporal.

> [!IMPORTANT]
> [!IMPORTANTE] Lea este procedimiento antes de realizar las acciones, ya que no es tan fácil reducir un dispositivo una vez que se ha expandido.

> [!NOTE]
> [!NOTA] De forma predeterminada en Microsoft SQL Server 7.0 y versiones posteriores, TempDB se configura de modo que pueda aumentar automáticamente según sea necesario. Por lo tanto, puede que este procedimiento sólo sea necesario en servidores que ejecutan versiones anteriores a la 7.0.



**Para aumentar el espacio de TempDB en SQL Server 6.5**

1.  Inicie Microsoft® SQL Server Enterprise Manager, abra el árbol del Servidor y, a continuación, el árbol de dispositivos de base de datos.

2.  Seleccione un dispositivo (físico) para expandirlo, tal como Master, y haga doble clic en el dispositivo para abrir el cuadro de diálogo **Editar dispositivo de base de datos**. Este cuadro de diálogo muestra cuánto espacio están utilizando las bases de datos actuales.

3.  En el cuadro **Tamaño**, aumente el dispositivo a la cantidad deseada (por ejemplo, 50 MB de espacio en disco duro).

4.  Haga clic en **Cambiar ahora** para aumentar la cantidad de espacio a la que la base de datos temporal (lógica) TempDB se puede expandir.

5.  Abra el árbol Bases de datos en el servidor y, a continuación, haga doble clic en **TempDB** para abrir el cuadro de diálogo **Edit Database**. La pestaña **Base de datos** muestra la cantidad de espacio actualmente asignado a TempDB (**Tamaño de datos**). De forma predeterminada, son 2 MB.

6.  En el grupo **Tamaño**, haga clic en **Expandir**. Los gráficos muestran el espacio disponible y utilizado en cada uno de los dispositivos físicos. Las barras en color granate representan espacio disponible.

7.  Seleccione un **Dispositivo de registro**, tal como Patrón, para mostrar el tamaño disponible en el cuadro **Tamaño (MB)**.

8.  Haga clic en **Expandir ahora** para asignar ese espacio a la base de datos TempDB. El cuadro de diálogo **Editar base de datos** muestra el nuevo tamaño asignado para TempDB.

Para obtener más información acerca de este tema, busque "cuadro de diálogo Expandir base de datos" en el archivo de Ayuda de Microsoft SQL Server Enterprise Manager.

