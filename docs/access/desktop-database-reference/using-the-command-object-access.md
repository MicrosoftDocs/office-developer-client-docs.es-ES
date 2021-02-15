---
title: Uso del objeto Command (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b89d292d86035e565ad18413062274dfbfc74db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312029"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="d3312-102">Uso del objeto Command (Access)</span><span class="sxs-lookup"><span data-stu-id="d3312-102">Using the Command object (Access)</span></span>


<span data-ttu-id="d3312-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3312-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3312-p101">Después de conectar con un origen de datos, debe ejecutar peticiones en él para obtener conjuntos de resultados. ADO encapsula este tipo de funcionalidad de comando en el objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="d3312-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="d3312-p102">Puede usar el objeto **Command** para solicitar cualquier tipo de operación del proveedor, suponiendo que éste pueda interpretar correctamente la cadena del comando. Una operación común para los proveedores de datos es la de consultar una base de datos y devolver registros en un objeto **Recordset**. Los objetos **Recordset** se tratarán más adelante en éste y otros capítulos; por ahora, considérelos como herramientas para contener y ver conjuntos de resultados. Al igual que ocurre con muchos objetos ADO, según la funcionalidad del proveedor, algunas colecciones de objetos **Command**, métodos o propiedades podrían generar errores al hacer referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="d3312-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset** s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="d3312-p103">No siempre es necesario crear un objeto **Command** para ejecutar un comando en un origen de datos. Puede utilizar el método **Execute** en el objeto **Connection** o el método **Open** en el objeto **Recordset**. Sin embargo, debe usar un objeto **Command** si necesita volver a usar un comando en el código o si debe pasar información detallada de parámetros con el comando. Estos escenarios se describen con más detalle posteriormente en este capítulo.</span><span class="sxs-lookup"><span data-stu-id="d3312-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="d3312-114">Algunos objetos Command pueden devolver un conjunto de resultados como una secuencia binaria o un único registro, en vez de un objeto Recordset, si el proveedor admite esa posibilidad.</span><span class="sxs-lookup"><span data-stu-id="d3312-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="d3312-115">Además, algunos objetos Command no devuelven ningún conjunto de resultados (por ejemplo, una consulta Update de SQL).</span><span class="sxs-lookup"><span data-stu-id="d3312-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="d3312-116">Este capítulo tratará el escenario más típico: ejecutar objetos Command que devuelven resultados en un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="d3312-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="d3312-117">Para obtener más información acerca de los resultados devueltos en objetos Record o Stream, vea [Capítulo 10: Objetos Record y Stream](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="d3312-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="d3312-118">Esta sección incluye los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="d3312-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="d3312-119">Información general sobre el objeto Command</span><span class="sxs-lookup"><span data-stu-id="d3312-119">Command object overview</span></span>](command-object-overview.md)
- [<span data-ttu-id="d3312-120">Crear y ejecutar un comando sencillo</span><span class="sxs-lookup"><span data-stu-id="d3312-120">Creating and executing a simple command</span></span>](creating-and-executing-a-simple-command.md)
- [<span data-ttu-id="d3312-121">Parámetros del objeto Command</span><span class="sxs-lookup"><span data-stu-id="d3312-121">Command object parameters</span></span>](command-object-parameters.md)
- [<span data-ttu-id="d3312-122">Llamar a un procedimiento almacenado con un comando</span><span class="sxs-lookup"><span data-stu-id="d3312-122">Calling a stored procedure with a command</span></span>](calling-a-stored-procedure-with-a-command.md)
- [<span data-ttu-id="d3312-123">Comandos con nombre</span><span class="sxs-lookup"><span data-stu-id="d3312-123">Named commands</span></span>](named-commands.md)
