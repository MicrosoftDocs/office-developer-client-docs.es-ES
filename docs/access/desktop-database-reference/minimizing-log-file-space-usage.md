---
title: Minimización del uso del espacio del archivo de registro
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715280"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="4de06-102">Minimización del uso del espacio del archivo de registro</span><span class="sxs-lookup"><span data-stu-id="4de06-102">Minimizing log file space usage</span></span>

<span data-ttu-id="4de06-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4de06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4de06-p101">Un archivo de registro se puede llenar rápidamente y, de esta forma, detener el servidor, si hay mucha actividad en una base de datos de SQL Server. Si selecciona la opción **Truncar registro en punto de comprobación** del archivo de registro, puede ampliar significativamente la vida del archivo de registro de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="4de06-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="4de06-106">**Para habilitar la opción Truncar registro en punto de comprobación de Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="4de06-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="4de06-107">Inicie Microsoft SQL Server Enterprise Manager, abra el árbol del servidor y, a continuación, el árbol de dispositivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4de06-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="4de06-108">Haga doble clic en el nombre de la base de datos en la que se habilitará esta característica.</span><span class="sxs-lookup"><span data-stu-id="4de06-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="4de06-109">En la pestaña **Base de datos**, seleccione **Truncamiento**.</span><span class="sxs-lookup"><span data-stu-id="4de06-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="4de06-110">En la pestaña **Opciones**, seleccione **Truncar registro en punto de comprobación** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4de06-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="4de06-111">**Para habilitar Truncar registro en punto de comprobación en Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="4de06-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="4de06-112">Inicie Microsoft SQL Server Enterprise Manager, abra el árbol del servidor y, a continuación, el árbol de dispositivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4de06-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="4de06-113">Haga clic con el botón secundario en el nombre de la base de datos para la que se habilitará esta característica y seleccione **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="4de06-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="4de06-114">En la pestaña **Opciones**, seleccione **Truncar registro en punto de comprobación** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4de06-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="4de06-115">Para obtener más información acerca de la característica **Truncar en punto de comprobación**, vea la documentación de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4de06-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

