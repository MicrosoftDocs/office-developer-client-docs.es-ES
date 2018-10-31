---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1779f2c7e16e2f39a3912f271296c6a7bd0fd550
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861949"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="b439f-102">Using the Command Object (Access)</span><span class="sxs-lookup"><span data-stu-id="b439f-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="b439f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b439f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b439f-p101">Después de conectar con un origen de datos, debe ejecutar peticiones en él para obtener conjuntos de resultados. ADO encapsula este tipo de funcionalidad de comando en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="b439f-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="b439f-p102">Puede usar el objeto **Command** para solicitar cualquier tipo de operación del proveedor, suponiendo que éste pueda interpretar correctamente la cadena del comando. Una operación común para los proveedores de datos es la de consultar una base de datos y devolver registros en un objeto **Recordset**. Los objetos **Recordset** se tratarán más adelante en éste y otros capítulos; por ahora, considérelos como herramientas para contener y ver conjuntos de resultados. Al igual que ocurre con muchos objetos ADO, según la funcionalidad del proveedor, algunas colecciones de objetos **Command**, métodos o propiedades podrían generar errores al hacer referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="b439f-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="b439f-p103">No siempre es necesario crear un objeto **Command** para ejecutar un comando en un origen de datos. Puede utilizar el método **Execute** en el objeto **Connection** o el método **Open** en el objeto **Recordset**. Sin embargo, debe usar un objeto **Command** si necesita volver a usar un comando en el código o si debe pasar información detallada de parámetros con el comando. Estos escenarios se describen con más detalle posteriormente en este capítulo.</span><span class="sxs-lookup"><span data-stu-id="b439f-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="b439f-114">Determinados comandos pueden devolver un resultado de establecer como una secuencia binaria o un único registro, en lugar de un objeto Recordset, si esto es compatible con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="b439f-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="b439f-115">Además, algunos comandos no están diseñados para devolver cualquier conjunto en absoluto de resultados (por ejemplo, una consulta SQL Update).</span><span class="sxs-lookup"><span data-stu-id="b439f-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="b439f-116">Este capítulo tratará el escenario más típico: ejecutar comandos que devuelven resultados en un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="b439f-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="b439f-117">Para obtener más información sobre cómo devolver los resultados en secuencias o de registros, vea [capítulo 10: objetos Record y Stream](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="b439f-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="b439f-118">Esta sección incluye los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="b439f-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="b439f-119">Información general del objeto Command</span><span class="sxs-lookup"><span data-stu-id="b439f-119">Command Object Overview</span></span>](command-object-overview.md)

- [<span data-ttu-id="b439f-120">Creación y ejecución de un comando simple</span><span class="sxs-lookup"><span data-stu-id="b439f-120">Creating and Executing a Simple Command</span></span>](creating-and-executing-a-simple-command.md)

- [<span data-ttu-id="b439f-121">Parámetros del objeto Command</span><span class="sxs-lookup"><span data-stu-id="b439f-121">Command Object Parameters</span></span>](command-object-parameters.md)

- [<span data-ttu-id="b439f-122">Llamada a un procedimiento almacenado con un comando</span><span class="sxs-lookup"><span data-stu-id="b439f-122">Calling a Stored Procedure with a Command</span></span>](calling-a-stored-procedure-with-a-command.md)

- [<span data-ttu-id="b439f-123">Comandos con nombre</span><span class="sxs-lookup"><span data-stu-id="b439f-123">Named Commands</span></span>](named-commands.md)
