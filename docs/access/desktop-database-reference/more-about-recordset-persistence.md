---
title: Información adicional sobre la persistencia del objeto Recordset
TOCTitle: More About Recordset Persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05287befde90319ad2844effef8ef2d47e1241b7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485526"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="9e204-102">Información adicional sobre la persistencia del objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="9e204-102">More About Recordset Persistence</span></span>


<span data-ttu-id="9e204-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e204-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e204-104">El objeto Recordset de ADO admite el almacenamiento del contenido de un objeto **Recordset** en un archivo mediante el método [Save](save-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9e204-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="9e204-105">El archivo almacenado de manera persistente puede existir en una unidad local, servidor de red, o como una dirección URL en un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="9e204-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="9e204-106">Más adelante, se puede restaurar el archivo con el método **Open** del objeto [Recordset](open-method-ado-recordset.md) o el método [Execute](connection-object-ado.md) del objeto [Connection](https://msdn.microsoft.com/library/jj249832\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9e204-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method.</span></span>

<span data-ttu-id="9e204-107">Además, el método [GetString](getstring-method-ado.md) convierte un objeto **Recordset** a un formato donde las columnas y las filas estén delimitadas con los caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="9e204-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="9e204-p102">Para almacenar un objeto **Recordset**, conviértalo primero a un formato que se pueda almacenar en un archivo. Los objetos **Recordset** se pueden almacenar en el formato ADTG (Advanced Data TableGram) propietario o el formato XML (Lenguaje de marcado extensible) abierto. A continuación, se muestran ejemplos de ADTG. Para obtener más información sobre el almacenamiento en formato de lenguaje XML, vea [Almacenar registros en formato XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="9e204-p102">To persist a **Recordset**, begin by converting it to a form that can be stored in a file. **Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format. ADTG examples are shown below. For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="9e204-p103">Guarde los cambios pendientes en el archivo almacenado. De este modo, puede emitir una consulta que devuelva un objeto **Recordset**, lo edite, guarde el objeto **Recordset** y los cambios pendientes, restaure posteriormente el objeto **Recordset** y, a continuación, actualice el origen de datos con los cambios pendientes guardados.</span><span class="sxs-lookup"><span data-stu-id="9e204-p103">Save any pending changes in the persisted file. Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="9e204-114">Para obtener información sobre cómo almacenar los objetos **Stream** de manera persistente, vea [Secuencias y persistencia](streams-and-persistence.md) en el capítulo 10.</span><span class="sxs-lookup"><span data-stu-id="9e204-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="9e204-115">Para obtener un ejemplo del almacenamiento de un objeto **Recordset**, vea [Escenario de almacenamiento de un objeto Recordset en formato XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="9e204-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="9e204-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e204-116">Example</span></span>

<span data-ttu-id="9e204-117">**Guardar un objeto Recordset:**</span><span class="sxs-lookup"><span data-stu-id="9e204-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="9e204-118">**Abrir un archivo almacenado con Recordset.Open:**</span><span class="sxs-lookup"><span data-stu-id="9e204-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="9e204-119">De manera opcional, si el objeto **Recordset** no tiene una conexión activa, podrá aceptar todos los valores predeterminados y escribir simplemente el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="9e204-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="9e204-120">**Abrir un archivo almacenado con Connection.Execute:**</span><span class="sxs-lookup"><span data-stu-id="9e204-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="9e204-121">**Abrir un archivo almacenado con RDS.DataControl:**</span><span class="sxs-lookup"><span data-stu-id="9e204-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="9e204-122">En este caso, la propiedad **Server** no está establecida.</span><span class="sxs-lookup"><span data-stu-id="9e204-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```
