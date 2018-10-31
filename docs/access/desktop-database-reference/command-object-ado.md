---
title: Command (objeto) (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 153f59ebbcfae89f6358fe0d707791aab8a8cdd7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864077"
---
# <a name="command-object-ado"></a><span data-ttu-id="a3463-102">Command (objeto) (ADO)</span><span class="sxs-lookup"><span data-stu-id="a3463-102">Command Object (ADO)</span></span>


<span data-ttu-id="a3463-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3463-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a3463-104">Define un comando específico que se intenta ejecutar con respecto a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="a3463-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3463-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3463-105">Remarks</span></span>

<span data-ttu-id="a3463-p101">Use un objeto **Command** para realizar una consulta en una base de datos y devolver registros en un objeto [Recordset](recordset-object-ado.md), para ejecutar una operación masiva, o para manipular la estructura de una base de datos. Según la funcionalidad del proveedor, algunos métodos, colecciones o propiedades del objeto **Command** pueden generar un error cuando se hace referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="a3463-p101">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database. Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="a3463-108">Con las colecciones, los métodos y las propiedades de un objeto **Command**, se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a3463-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="a3463-109">Definir el texto ejecutable del comando (por ejemplo, una instrucción SQL) con la propiedad [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="a3463-110">Definir consultas con parámetros o argumentos de procedimientos almacenados con objetos [Parameter](parameter-object-ado.md) y la colección [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="a3463-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a3463-111"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="a3463-112">Ejecutar un comando y devolver un objeto **Recordset**, si procede, con el método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a3463-112">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>
=======
  - <span data-ttu-id="a3463-113">Ejecutar un comando y devolver un objeto **Recordset**, si procede, con el método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).</span><span class="sxs-lookup"><span data-stu-id="a3463-113">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>
>>>>>>> <span data-ttu-id="a3463-114">master</span><span class="sxs-lookup"><span data-stu-id="a3463-114">master</span></span>

  - <span data-ttu-id="a3463-115">Especificar el tipo de comando con la propiedad [CommandType](commandtype-property-ado.md) antes de la ejecución para optimizar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a3463-115">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="a3463-116">Controlar si el proveedor guarda una versión preparada (o compilada) del comando antes de la ejecución con la propiedad [Prepared](prepared-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-116">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="a3463-117">Establecer el número de segundos que esperará un proveedor para la ejecución de un comando con la propiedad [CommandTimeout](commandtimeout-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-117">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="a3463-118">Asociar una conexión abierta con un objeto **Command** estableciendo su propiedad [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-118">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="a3463-119">Establecer la propiedad [Name](name-property-ado.md) para identificar el objeto **Command** como un método en el objeto [Connection](connection-object-ado.md) asociado.</span><span class="sxs-lookup"><span data-stu-id="a3463-119">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="a3463-120">Pasar un objeto **Command** a la propiedad [Source](source-property-ado-recordset.md) de un objeto **Recordset** para obtener datos.</span><span class="sxs-lookup"><span data-stu-id="a3463-120">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="a3463-121">Obtener acceso a atributos específicos del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3463-121">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="a3463-p102">[!NOTA] Para ejecutar una consulta sin usar un objeto **Command**, pase una cadena de consulta al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) de un objeto **Connection** o al método [Open](open-method-ado-recordset.md) de un objeto **Recordset**. Sin embargo, un objeto **Command** es necesario cuando quiere conservar el texto del comando y volver a ejecutarlo o usar parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="a3463-p102">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object. However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="a3463-p103">Para crear un objeto **Command** independientemente de un objeto **Connection** definido anteriormente, establezca su propiedad **ActiveConnection** en una cadena de conexión válida. ADO seguirá creando un objeto **Connection**, pero no asignará ese objeto a una variable de objeto. Sin embargo, si asocia varios objetos **Command** a la misma conexión, debe crear y abrir explícitamente un objeto **Connection**; de este modo, se asigna el objeto **Connection** a una variable de objeto. Si no establece la propiedad **ActiveConnection** del objeto **Command** en esta variable de objeto, ADO creará un nuevo objeto **Connection** para cada objeto **Command**, aunque se utilice la misma cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="a3463-p103">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string. ADO still creates a **Connection** object, but it doesn't assign that object to an object variable. However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable. If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="a3463-p104">Para ejecutar un objeto **Command**, basta con invocarlo mediante su propiedad [Name](name-property-ado.md) en el objeto **Connection** asociado. El objeto **Command** debe tener su propiedad **ActiveConnection** establecida en el objeto **Connection**. Si el objeto **Command** tiene parámetros, pase como argumentos sus correspondientes valores al método.</span><span class="sxs-lookup"><span data-stu-id="a3463-p104">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object. The **Command** must have its **ActiveConnection** property set to the **Connection** object. If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="a3463-p105">Si se ejecutan dos o más objetos **Command** en la misma conexión y cualquiera de los objetos **Command** es un procedimiento almacenado con parámetros de salida, se producirá un error. Para ejecutar cada uno de los objetos **Command**, use conexiones independientes o desconecte todos los demás objetos **Command** de la conexión.</span><span class="sxs-lookup"><span data-stu-id="a3463-p105">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs. To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="a3463-p106">La colección **Parameters** es el miembro predeterminado del objeto **Command**. Como consecuencia, las dos instrucciones de código siguientes son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a3463-p106">The **Parameters** collection is the default member of the **Command** object. As a result, the following two code statements are equivalent.</span></span>

