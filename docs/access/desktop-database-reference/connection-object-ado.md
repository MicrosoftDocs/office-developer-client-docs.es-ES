---
title: Connection (objeto) (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ed736a0e52ff45cd0fed63f1ba5bd7060d7a2380
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295880"
---
# <a name="connection-object-ado"></a>Connection (objeto) (ADO)

**Se aplica a:** Access 2013, Office 2013

Representa una conexión abierta con un origen de datos.

## <a name="remarks"></a>Comentarios

Un objeto **Connection** representa una sesión única con un origen de datos. En el caso de un sistema de base de datos cliente/servidor, puede ser equivalente a una conexión de red real con el servidor. Según sea la funcionalidad admitida por el proveedor, algunas colecciones, métodos o propiedades de un objeto **Connection** podrían no estar disponibles.

Con las colecciones, los métodos y las propiedades de un objeto **Connection**, se puede hacer lo siguiente:

  - Configurar la conexión antes de abrirla con las propiedades [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) y [Mode](mode-property-ado.md). **ConnectionString** es la propiedad predeterminada del objeto **Connection**.

  - Establecer la propiedad [CursorLocation](cursorlocation-property-ado.md) en el cliente para llamar al [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), que admite actualizaciones por lotes.

  - Establecer la base de datos predeterminada para la conexión con la propiedad [DefaultDatabase](defaultdatabase-property-ado.md).

  - Establecer el nivel de aislamiento para las transacciones abiertas en la conexión con la propiedad [IsolationLevel](isolationlevel-property-ado.md).

  - Especificar un proveedor OLE DB con la propiedad [Provider](provider-property-ado.md).

  - Establecer y, posteriormente, interrumpir la conexión física con el origen de datos con los métodos [Open](open-method-ado-connection.md) y [Close](close-method-ado.md).

  - Ejecutar un comando en la conexión con el método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) y configurar la ejecución con la propiedad [CommandTimeout](commandtimeout-property-ado.md).
    
    > [!NOTE]
    > [!NOTA] Para ejecutar una consulta sin usar un objeto Command, pase una cadena de consulta al método **Execute** de un objeto **Connection**. Sin embargo, se requiere un objeto [Command](command-object-ado.md) cuando se desea conservar el texto del comando y volver a ejecutarlo, o usar parámetros de consulta.

  - Administrar transacciones en la conexión abierta, incluidas las transacciones anidadas si el proveedor las admite, con los métodos [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) y [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) y la propiedad [Attributes](attributes-property-ado.md).

  - Examinar los errores devueltos desde el origen de datos con la colección [Errors](errors-collection-ado.md).

  - Leer la versión de la implementación de ADO utilizada con la propiedad [Version](version-property-ado.md).

  - Obtener información de esquema acerca de la base de datos con el método [OpenSchema](openschema-method-ado.md).

Puede crear objetos **Connection** independientemente de cualquier otro objeto definido anteriormente.

Puede ejecutar comandos o procedimientos almacenados como si fueran métodos nativos en el objeto **Connection**, como se ilustra más adelante.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Ejecutar un comando como un método nativo de un objeto Connection

Para ejecutar un comando, asígnele un nombre mediante la propiedad [Name](name-property-ado.md) del objeto **Command**. Establezca la propiedad **ActiveConnection** del objeto **Command** en la conexión. A continuación, emita una instrucción en la que se use el nombre del comando como si fuera un método en el objeto **Connection**, seguido de los parámetros que desee, y seguido después de un objeto **Recordset** si se devuelven filas. Establezca las propiedades **Recordset** para personalizar el objeto **Recordset** resultante. Por ejemplo:

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Ejecutar un procedimiento como un método nativo de un objeto Connection

Para ejecutar un procedimiento almacenado, emita una instrucción en la que el nombre del procedimiento almacenado se utilice como si fuera un método en el objeto **Connection**, seguido de los parámetros que desee. ADO realizará un "ejercicio de adivinación" de los tipos de parámetro. Por ejemplo:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
