---
title: Propiedad Workspace. LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306912"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="600fc-102">Propiedad Workspace. LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="600fc-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="600fc-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="600fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="600fc-104">Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="600fc-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="600fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="600fc-105">Syntax</span></span>

<span data-ttu-id="600fc-106">*expresión* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="600fc-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="600fc-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="600fc-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="600fc-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="600fc-108">Remarks</span></span>

<span data-ttu-id="600fc-p101">La propiedad predeterminada **LoginTimeout** está configurada en 20 segundos. Cuando la propiedad **LoginTimeout** está configurada en 0, no se produce tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="600fc-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="600fc-p102">Si está intentando conectarse a una base de datos ODBC como, por ejemplo, Microsoft SQL Server, puede producirse un error en la conexión como resultado de errores de red o porque el servidor está apagado. Mejor que esperar los 20 segundos predeterminados para realizar la conexión, puede especificar el tiempo de espera antes de que aparezca un error. Una conexión al servidor se produce implícitamente como parte de diferentes eventos, tales como ejecutar una consulta o conectarse a un servidor de base de datos externo.</span><span class="sxs-lookup"><span data-stu-id="600fc-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

