---
title: Connection (objeto) (ADO)
TOCTitle: Connection Object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0f2c629a24bf6327be8a9848e719b40bfa88ea17
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873323"
---
# <a name="connection-object-ado"></a><span data-ttu-id="002ee-102">Connection (objeto) (ADO)</span><span class="sxs-lookup"><span data-stu-id="002ee-102">Connection Object (ADO)</span></span>

<span data-ttu-id="002ee-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="002ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="002ee-104">Representa una conexión abierta con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="002ee-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="002ee-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="002ee-105">Remarks</span></span>

<span data-ttu-id="002ee-p101">Un objeto **Connection** representa una sesión única con un origen de datos. En el caso de un sistema de base de datos cliente/servidor, puede ser equivalente a una conexión de red real con el servidor. Según sea la funcionalidad admitida por el proveedor, algunas colecciones, métodos o propiedades de un objeto **Connection** podrían no estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="002ee-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it may be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="002ee-109">Con las colecciones, los métodos y las propiedades de un objeto **Connection**, se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="002ee-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="002ee-p102">Configurar la conexión antes de abrirla con las propiedades [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) y [Mode](mode-property-ado.md). **ConnectionString** es la propiedad predeterminada del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="002ee-p102">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties. **ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="002ee-112">Establecer la propiedad [CursorLocation](cursorlocation-property-ado.md) en el cliente para llamar al [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), que admite actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="002ee-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="002ee-113">Establecer la base de datos predeterminada para la conexión con la propiedad [DefaultDatabase](defaultdatabase-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="002ee-114">Establecer el nivel de aislamiento para las transacciones abiertas en la conexión con la propiedad [IsolationLevel](isolationlevel-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="002ee-115">Especificar un proveedor OLE DB con la propiedad [Provider](provider-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="002ee-116">Establecer y, posteriormente, interrumpir la conexión física con el origen de datos con los métodos [Open](open-method-ado-connection.md) y [Close](close-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="002ee-117">Ejecutar un comando en la conexión con el método [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) y configurar la ejecución con la propiedad [CommandTimeout](commandtimeout-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-117">Execute a command on the connection with the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="002ee-p103">[!NOTA] Para ejecutar una consulta sin usar un objeto Command, pase una cadena de consulta al método **Execute** de un objeto **Connection**. Sin embargo, se requiere un objeto [Command](command-object-ado.md) cuando se desea conservar el texto del comando y volver a ejecutarlo, o usar parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="002ee-p103">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object. However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="002ee-120">Administrar transacciones en la conexión abierta, incluidas las transacciones anidadas si el proveedor las admite, con los métodos [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) y [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) y la propiedad [Attributes](attributes-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="002ee-121">Examinar los errores devueltos desde el origen de datos con la colección [Errors](errors-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="002ee-122">Leer la versión de la implementación de ADO utilizada con la propiedad [Version](version-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="002ee-123">Obtener información de esquema acerca de la base de datos con el método [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="002ee-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="002ee-124">Puede crear objetos **Connection** independientemente de cualquier otro objeto definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="002ee-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="002ee-125">Puede ejecutar comandos o procedimientos almacenados como si fueran métodos nativos en el objeto **Connection**, como se ilustra más adelante.</span><span class="sxs-lookup"><span data-stu-id="002ee-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="002ee-126">Ejecutar un comando como un método nativo de un objeto Connection</span><span class="sxs-lookup"><span data-stu-id="002ee-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="002ee-p104">Para ejecutar un comando, asígnele un nombre mediante la propiedad **Name** del objeto [Command](name-property-ado.md). Establezca la propiedad **ActiveConnection** del objeto **Command** en la conexión. A continuación, emita una instrucción en la que se use el nombre del comando como si fuera un método en el objeto **Connection**, seguido de los parámetros que desee, y seguido después de un objeto **Recordset** si se devuelven filas. Establezca las propiedades **Recordset** para personalizar el objeto **Recordset** resultante. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="002ee-p104">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property. Set the **Command** object's **ActiveConnection** property to the connection. Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned. Set the **Recordset** properties to customize the resulting **Recordset**. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="002ee-132">Ejecutar un procedimiento como un método nativo de un objeto Connection</span><span class="sxs-lookup"><span data-stu-id="002ee-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="002ee-p105">Para ejecutar un procedimiento almacenado, emita una instrucción en la que el nombre del procedimiento almacenado se utilice como si fuera un método en el objeto **Connection**, seguido de los parámetros que desee. ADO realizará un "ejercicio de adivinación" de los tipos de parámetro. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="002ee-p105">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters. ADO will make a "best guess" of parameter types. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
