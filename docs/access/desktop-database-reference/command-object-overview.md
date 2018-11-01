---
title: Descripción general del objeto Command
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39724156b8644b6d99ffec82bdf79624b6cfaee1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875038"
---
# <a name="command-object-overview"></a><span data-ttu-id="95164-102">Descripción general del objeto Command</span><span class="sxs-lookup"><span data-stu-id="95164-102">Command Object Overview</span></span>


<span data-ttu-id="95164-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95164-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95164-104">Con las colecciones, los métodos y las propiedades de un objeto **Command**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="95164-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="95164-105">Definir el texto ejecutable del comando (por ejemplo, una instrucción SQL o un procedimiento almacenado) utilizando la propiedad **CommandText**.</span><span class="sxs-lookup"><span data-stu-id="95164-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="95164-106">Definir consultas parametrizadas o argumentos de procedimientos almacenados utilizando objetos **Parameter** y la colección **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="95164-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="95164-107">Ejecutar un comando y devolver un objeto **Recordset**, si procede, usando el método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="95164-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="95164-108">Especificar el tipo de comando mediante la propiedad **CommandType** antes de la ejecución para optimizar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="95164-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="95164-109">Controlar si el proveedor guarda una versión preparada (o compilada) del comando antes de la ejecución mediante la propiedad **Prepared**.</span><span class="sxs-lookup"><span data-stu-id="95164-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="95164-110">Establecer el número de segundos que esperará un proveedor para la ejecución de un comando mediante la propiedad **CommandTimeout**.</span><span class="sxs-lookup"><span data-stu-id="95164-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="95164-111">Asociar una conexión abierta con un objeto **Command** estableciendo su propiedad **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="95164-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="95164-112">Establecer la propiedad **Name** para identificar el objeto **Command** como un método en el objeto **Connection** asociado.</span><span class="sxs-lookup"><span data-stu-id="95164-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="95164-113">Pasar un objeto **Command** a la propiedad **Source** de un **conjunto de registros** para obtener datos.</span><span class="sxs-lookup"><span data-stu-id="95164-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

