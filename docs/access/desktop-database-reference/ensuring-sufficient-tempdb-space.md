---
title: Comprobación de que hay espacio suficiente en TempDB
TOCTitle: Ensuring sufficient TempDB space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6414c9dd4c3218c2c2bf90f39d0cfb950e6e1018
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293577"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="9025d-102">Comprobación de que hay espacio suficiente en TempDB</span><span class="sxs-lookup"><span data-stu-id="9025d-102">Ensuring sufficient TempDB space</span></span>


<span data-ttu-id="9025d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9025d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9025d-p101">Si se producen errores mientras se procesan objetos [Recordset](recordset-object-ado.md) que requieren espacio de procesamiento en Microsoft SQL Server 6.5, puede que sea necesario aumentar el tamaño de la base de datos temporal (TempDB). Algunas consultas requieren espacio de procesamiento temporal; por ejemplo, una consulta con una cláusula ORDER BY necesita ordenar el objeto **Recordset**, lo cual requiere algo de espacio temporal.</span><span class="sxs-lookup"><span data-stu-id="9025d-p101">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB. (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9025d-106">[!IMPORTANTE] Lea este procedimiento antes de realizar las acciones, ya que no es tan fácil reducir un dispositivo una vez que se ha expandido.</span><span class="sxs-lookup"><span data-stu-id="9025d-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="9025d-p102">[!NOTA] De forma predeterminada en Microsoft SQL Server 7.0 y versiones posteriores, TempDB se configura de modo que pueda aumentar automáticamente según sea necesario. Por lo tanto, puede que este procedimiento sólo sea necesario en servidores que ejecutan versiones anteriores a la 7.0.</span><span class="sxs-lookup"><span data-stu-id="9025d-p102">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed. Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="9025d-109">**Para aumentar el espacio de TempDB en SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="9025d-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="9025d-110">Inicie Microsoft SQL Server Enterprise Manager, abra el árbol del servidor y, a continuación, el árbol de dispositivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="9025d-110">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="9025d-p103">Seleccione un dispositivo (físico) para expandirlo, tal como Master, y haga doble clic en el dispositivo para abrir el cuadro de diálogo **Editar dispositivo de base de datos**. Este cuadro de diálogo muestra cuánto espacio están utilizando las bases de datos actuales.</span><span class="sxs-lookup"><span data-stu-id="9025d-p103">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="9025d-113">En el cuadro **Tamaño**, aumente el dispositivo a la cantidad deseada (por ejemplo, 50 MB de espacio en disco duro).</span><span class="sxs-lookup"><span data-stu-id="9025d-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="9025d-114">Haga clic en **Cambiar ahora** para aumentar la cantidad de espacio a la que la base de datos temporal (lógica) TempDB se puede expandir.</span><span class="sxs-lookup"><span data-stu-id="9025d-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="9025d-p104">Abra el árbol Bases de datos en el servidor y, a continuación, haga doble clic en **TempDB** para abrir el cuadro de diálogo **Edit Database**. La pestaña **Base de datos** muestra la cantidad de espacio actualmente asignado a TempDB (**Tamaño de datos**). De forma predeterminada, son 2 MB.</span><span class="sxs-lookup"><span data-stu-id="9025d-p104">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box. The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**). By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="9025d-p105">En el grupo **Tamaño**, haga clic en **Expandir**. Los gráficos muestran el espacio disponible y utilizado en cada uno de los dispositivos físicos. Las barras en color granate representan espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="9025d-p105">Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="9025d-121">Seleccione un **Dispositivo de registro**, tal como Patrón, para mostrar el tamaño disponible en el cuadro **Tamaño (MB)**.</span><span class="sxs-lookup"><span data-stu-id="9025d-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="9025d-p106">Haga clic en **Expandir ahora** para asignar ese espacio a la base de datos TempDB. El cuadro de diálogo **Editar base de datos** muestra el nuevo tamaño asignado para TempDB.</span><span class="sxs-lookup"><span data-stu-id="9025d-p106">Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="9025d-124">Para obtener más información acerca de este tema, busque "cuadro de diálogo Expandir base de datos" en el archivo de Ayuda de Microsoft SQL Server Enterprise Manager.</span><span class="sxs-lookup"><span data-stu-id="9025d-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

