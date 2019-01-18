---
title: Información general sobre el objeto Command
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c7697d4ae8b830afb53eee10e7dd59a7dc8db4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712088"
---
# <a name="command-object-overview"></a><span data-ttu-id="4b7ce-102">Información general sobre el objeto Command</span><span class="sxs-lookup"><span data-stu-id="4b7ce-102">Command object overview</span></span>

<span data-ttu-id="4b7ce-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b7ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b7ce-104">Con las colecciones, los métodos y las propiedades de un objeto **Command**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b7ce-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="4b7ce-105">Definir el texto ejecutable del comando (por ejemplo, una instrucción SQL o un procedimiento almacenado) utilizando la propiedad **CommandText**.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="4b7ce-106">Definir consultas parametrizadas o argumentos de procedimientos almacenados utilizando objetos **Parameter** y la colección **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="4b7ce-107">Ejecutar un comando y devolver un objeto **Recordset**, si procede, usando el método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="4b7ce-108">Especificar el tipo de comando mediante la propiedad **CommandType** antes de la ejecución para optimizar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="4b7ce-109">Controlar si el proveedor guarda una versión preparada (o compilada) del comando antes de la ejecución mediante la propiedad **Prepared**.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="4b7ce-110">Establecer el número de segundos que esperará un proveedor para la ejecución de un comando mediante la propiedad **CommandTimeout**.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="4b7ce-111">Asociar una conexión abierta con un objeto **Command** estableciendo su propiedad **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="4b7ce-112">Establecer la propiedad **Name** para identificar el objeto **Command** como un método en el objeto **Connection** asociado.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="4b7ce-113">Pasar un objeto **Command** a la propiedad **Source** de un **conjunto de registros** para obtener datos.</span><span class="sxs-lookup"><span data-stu-id="4b7ce-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

