---
title: Propiedad Workspace. Isolateodbctrans ((DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 781679dfbd4050cfde219802db4cd9e1544d83ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302516"
---
# <a name="workspaceisolateodbctrans-property-dao"></a><span data-ttu-id="dad76-102">Propiedad Workspace. Isolateodbctrans ((DAO)</span><span class="sxs-lookup"><span data-stu-id="dad76-102">Workspace.IsolateODBCTrans property (DAO)</span></span>


<span data-ttu-id="dad76-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dad76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dad76-104">Establece o devuelve un valor que indica si varias transacciones que implican los mismos motores de base de datos de Microsoft Access conectados al origen de datos ODBC están aisladas (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="dad76-104">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="dad76-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dad76-105">Syntax</span></span>

<span data-ttu-id="dad76-106">*expresión* . Isolateodbctrans (</span><span class="sxs-lookup"><span data-stu-id="dad76-106">*expression* .IsolateODBCTrans</span></span>

<span data-ttu-id="dad76-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="dad76-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dad76-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dad76-108">Remarks</span></span>

<span data-ttu-id="dad76-p101">En algunas situaciones, necesitará tener simultáneamente varias transacciones pendientes de la misma conexión ODBC. Para esto, debe abrir un **Workspace** distinto para cada transacción. Aunque cada **Workspace** puede tener su propia conexión ODBC a la base de datos, ello puede hacer descender el rendimiento del sistema. Como normalmente el aislamiento de la transacción no es necesario, las conexiones ODBC desde varios objetos **Workspace** abiertos por el mismo usuario se comparten de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dad76-p101">In some situations, you need to have multiple simultaneous transactions pending on the same ODBC connection. To do this, you need to open a separate **Workspace** for each transaction. Although each **Workspace** can have its own ODBC connection to the database, this slows system performance. Because transaction isolation isn't usually required, ODBC connections from multiple **Workspace** objects opened by the same user are shared by default.</span></span>

<span data-ttu-id="dad76-p102">Algunos servidores ODBC, como Microsoft SQL Server, no permiten transacciones simultáneas en una sola conexión. Si necesita tener más de una transacción pendiente a la vez en una base de datos, establezca la propiedad **IsolateODBCTrans** en **True** para cada **Workspace** tan pronto como abra la propiedad. Con ello se fuerza una conexión ODBC individual para cada **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="dad76-p102">Some ODBC servers, such as Microsoft SQL Server, don't allow simultaneous transactions on a single connection. If you need to have more than one transaction at a time pending against such a database, set the **IsolateODBCTrans** property to **True** on each **Workspace** as soon as you open it. This forces a separate ODBC connection for each **Workspace**.</span></span>

