---
title: Enumeración Driverpromptenum ((DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293668"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="cc83e-102">Enumeración Driverpromptenum ((DAO)</span><span class="sxs-lookup"><span data-stu-id="cc83e-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="cc83e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc83e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc83e-104">Especifica si se ha de preguntar al usuario para establecer una conexión y cuándo.</span><span class="sxs-lookup"><span data-stu-id="cc83e-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc83e-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc83e-105">Name</span></span></p></th>
<th><p><span data-ttu-id="cc83e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="cc83e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cc83e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc83e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc83e-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="cc83e-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="cc83e-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="cc83e-109">0</span></span></p></td>
<td><p><span data-ttu-id="cc83e-110">Si la cadena de conexión proporcionada incluye la palabra clave DSN, el administrador de controladores utiliza la cadena que se proporciona al establecer conexión; en caso contrario, se comporta al igual que cuando se especifica <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc83e-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc83e-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="cc83e-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="cc83e-112">3</span><span class="sxs-lookup"><span data-stu-id="cc83e-112">3</span></span></p></td>
<td><p><span data-ttu-id="cc83e-113">(Valor predeterminado) Se comporta como <strong>dbDriverComplete</strong>, con la excepción de que el controlador deshabilita los controles correspondientes a la información no necesaria para realizar la conexión.</span><span class="sxs-lookup"><span data-stu-id="cc83e-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc83e-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="cc83e-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="cc83e-115">1</span><span class="sxs-lookup"><span data-stu-id="cc83e-115">1</span></span></p></td>
<td><p><span data-ttu-id="cc83e-p101">El administrador de controladores utiliza la cadena de conexión proporcionada al establecer conexión. Si no se proporciona información suficiente, se devuelve un error interceptable.</span><span class="sxs-lookup"><span data-stu-id="cc83e-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc83e-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="cc83e-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="cc83e-119">segundo</span><span class="sxs-lookup"><span data-stu-id="cc83e-119">2</span></span></p></td>
<td><p><span data-ttu-id="cc83e-p102">El administrador de controladores muestra el cuadro de diálogo <strong>Orígenes de datos ODBC</strong>. La cadena de conexión utilizada para establecer la conexión se crea a partir del nombre del origen de datos (DSN) seleccionado y cumplimentado por el usuario a través de los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cc83e-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>

