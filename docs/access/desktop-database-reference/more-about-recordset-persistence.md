---
title: Más información sobre la persistencia del conjunto de registros
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288851"
---
# <a name="more-about-recordset-persistence"></a>Más información sobre la persistencia del conjunto de registros

**Se aplica a:** Access 2013, Office 2013

El objeto Recordset de ADO admite el almacenamiento del contenido de un objeto **Recordset** en un archivo mediante el método [Save](save-method-ado.md). El archivo almacenado persistentemente puede existir en una unidad local, un servidor de red o como una dirección URL en un sitio Web. Más adelante, se puede restaurar el archivo con el método **Open** del objeto [Recordset](open-method-ado-recordset.md) o el método [Execute](connection-object-ado.md) del objeto [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection).

Además, el método [GetString](getstring-method-ado.md) convierte un objeto **Recordset** a un formato donde las columnas y las filas estén delimitadas con los caracteres especificados.

Para almacenar un objeto **Recordset**, conviértalo primero a un formato que se pueda almacenar en un archivo. Los objetos **Recordset** se pueden almacenar en el formato ADTG (Advanced Data TableGram) propietario o el formato XML (Lenguaje de marcado extensible) abierto. A continuación, se muestran ejemplos de ADTG. Para obtener más información sobre el almacenamiento en formato de lenguaje XML, vea [Almacenar registros en formato XML](persisting-records-in-xml-format.md).

Guarde los cambios pendientes en el archivo almacenado. De este modo, puede emitir una consulta que devuelva un objeto **Recordset**, lo edite, guarde el objeto **Recordset** y los cambios pendientes, restaure posteriormente el objeto **Recordset** y, a continuación, actualice el origen de datos con los cambios pendientes guardados.

Para obtener información sobre cómo almacenar los objetos **Stream** de manera persistente, vea [Secuencias y persistencia](streams-and-persistence.md) en el capítulo 10.

Para obtener un ejemplo del almacenamiento de un objeto **Recordset**, vea [Escenario de almacenamiento de un objeto Recordset en formato XML](xml-recordset-persistence-scenario.md).

## <a name="example"></a>Ejemplo

**Guardar un objeto Recordset:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Abrir un archivo almacenado con Recordset.Open:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

De manera opcional, si el objeto **Recordset** no tiene una conexión activa, podrá aceptar todos los valores predeterminados y escribir simplemente el siguiente código:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Abrir un archivo almacenado con Connection.Execute:**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Abrir un archivo almacenado con RDS.DataControl:**

En este caso, la propiedad **Server** no está establecida.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

