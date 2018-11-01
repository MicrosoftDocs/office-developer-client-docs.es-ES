---
title: DBEngine.LoginTimeout Property (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8c6b7798419dc72dc28822741e2d038203ae257e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880722"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="5149e-102">DBEngine.LoginTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="5149e-102">DBEngine.LoginTimeout Property (DAO)</span></span>


<span data-ttu-id="5149e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5149e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5149e-104">Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="5149e-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5149e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5149e-105">Syntax</span></span>

<span data-ttu-id="5149e-106">*expresión* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="5149e-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="5149e-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="5149e-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5149e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5149e-108">Remarks</span></span>

<span data-ttu-id="5149e-p101">El valor predeterminado de la propiedad **LoginTimeout** es de 20 segundos. Cuando la propiedad **LoginTimeout** se establece en 0, no se produce tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="5149e-p101">The default **LoginTimeout** property setting is 20 seconds. When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="5149e-p102">Cuando se intenta establecer sesión en una base de datos ODBC, como Microsoft SQL Server, puede producirse un error en la conexión debido a errores en la red o a que el servidor no esté funcionando. En lugar de esperar los 20 segundos predeterminados para establecer la conexión, se puede especificar cuánto tiempo se desea esperar antes de que se produzca un error. El inicio de sesión en el servidor se produce implícitamente como parte de una serie de eventos diferentes, como la ejecución de una consulta en una base de datos externa del servidor.</span><span class="sxs-lookup"><span data-stu-id="5149e-p102">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running. Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error. Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

