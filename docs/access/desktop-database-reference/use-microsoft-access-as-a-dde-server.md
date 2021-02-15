---
title: Usar Microsoft Access como servidor DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access admite el intercambio dinámico de datos (DDE) como aplicación de destino (cliente) o aplicación de origen (servidor).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0750bdce0e1cda383c48f9c16e62e00997fdfb0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313394"
---
# <a name="use-microsoft-access-as-a-dde-server"></a>Usar Microsoft Access como servidor DDE

**Se aplica a:** Access 2013, Office 2013 

Microsoft Access admite el intercambio dinámico de datos (DDE) como aplicación de destino (cliente) o aplicación de origen (servidor). Por ejemplo, una aplicación como Microsoft Word, que actúa como cliente, puede solicitar datos a través de DDE de una base de datos de Microsoft Access que actúa como servidor.

> [!TIP]
> [!SUGERENCIA] Si necesita manipular objetos de Microsoft Access desde otra aplicación, considere la posibilidad de usar Automatización.

Una conversación DDE entre un cliente y un servidor se establece sobre un tema determinado. Un tema puede ser un archivo de datos en el formato admitido por la aplicación servidor o puede ser el tema System, que proporciona información sobre la propia aplicación servidor. Una vez iniciada una conversación sobre un tema determinado, solo se puede transferir un elemento de datos asociado a ese tema.

Por ejemplo, suponga que está ejecutando Microsoft Word y desea insertar en un documento datos de una determinada base de datos de Microsoft Access. Para iniciar una conversación DDE con Microsoft Access, abra un canal DDE mediante la función **DDEInitiate** y especifique el nombre del archivo de la base de datos como tema. A continuación, podrá transferir los datos de esa base de datos a Microsoft Word a través de dicho canal.

Como servidor DDE, Microsoft Access admite los siguiente temas:

- El tema System (Sistema)

- El nombre de una base de datos (tema *database (base de datos)*)

- El nombre de una tabla (tema *tablename (nombretabla)*)

- El nombre de una consulta (tema *queryname (nombreconsulta)*)

- Una cadena SQL de Microsoft Access (tema *sqlstring (cadenasql)*)

Después de establecer una conversación DDE, puede usar la instrucción **DDEExecute** para enviar un comando desde el cliente a la aplicación servidor. Cuando se utiliza como servidor DDE, Microsoft Access reconoce los siguientes elementos como un comando válido:

- El nombre de una macro en la actual base de datos.

- Cualquier acción que se pueda realizar en Visual Basic mediante uno de los métodos del objeto **DoCmd**.

- Las acciones AbrirBaseDeDatos (OpenDatabase) y CerrarBaseDeDatos (CloseDatabase), que se utilizan sólo para las operaciones DDE. (Para ver cómo se utilizan estas funciones, vea el ejemplo que aparece a continuación en este tema.)

> [!NOTE]
> [!NOTA] Al especificar una acción de macro como instrucción **DDEExecute**, la acción y los argumentos siguen la sintaxis del objeto **DoCmd** y deben ir entre corchetes ([ ]). Sin embargo, las aplicaciones que admiten DDE no reconocen las constantes intrínsecas en las operaciones DDE. Asimismo, los argumentos de cadena deben ir entre comillas (" ") si la cadena contiene una coma. En caso contrario, no son necesarias las comillas.

La aplicación cliente puede utilizar la función **DDERequest** para solicitar datos de texto de la aplicación servidor a través de un canal DDE abierto. O bien, el cliente puede utilizar la instrucción **DDEPoke** para enviar datos a la aplicación servidor. Una vez completada la transferencia de datos, el cliente puede usar la instrucción **DDETerminate** para cerrar el canal DDE o la instrucción **DDETerminateAll** para cerrar todos los canales abiertos.

> [!NOTE]
> Cuando la aplicación cliente termine de recibir datos a través de un canal DDE, deberá cerrar dicho canal para conservar los recursos de la memoria.

El siguiente ejemplo muestra cómo se crea un procedimiento de Microsoft Word mediante Visual Basic que utiliza Microsoft Access como servidor DDE. (Para que funcione este ejemplo, Microsoft Access debe estar ejecutándose.)

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

La siguiente sección facilita información sobre los temas DDE válidos que admite Microsoft Access.

## <a name="the-system-topic"></a>El tema System (Sistema)

El tema System es un tema estándar para todas las aplicaciones basadas en Microsoft Windows. Facilita información sobre los demás temas que admite la aplicación. Para obtener acceso a esta información, el código debe  llamar primero a la función **DDEInitiate** con el argumento de tema y, a continuación, ejecutar la instrucción **DDERequest** con uno de los siguientes valores proporcionados para el argumento *item.*

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Valores devueltos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Una lista de elementos que admite el tema System en Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Formatos</p></td>
<td><p>Una lista de formatos que Microsoft Access puede copiar al Portapapeles.</p></td>
</tr>
<tr class="odd">
<td><p>Estado</p></td>
<td><p>&quot;Ocupado &quot; o &quot; &quot; listo.</p></td>
</tr>
<tr class="even">
<td><p>Topics</p></td>
<td><p>Una lista de todas las bases de datos abiertas.</p></td>
</tr>
</tbody>
</table>

<br/>

El siguiente ejemplo muestra cómo se utilizan las funciones **DDEIniciar (DDEInitiate)** y **DDEPedido (DDERequest)** con el tema System:

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a>Tema de la base de datos

El tema *database* es el nombre de archivo de una base de datos existente. Puede escribir solo el nombre base (Northwind), o su ruta de acceso y extensión .mdb (C: Ejemplos de \\ Access \\ \\ Northwind.mdb). Tras iniciar una conversación DDE con la base de datos, puede solicitar una lista de los objetos incluidos en dicha base de datos.

> [!NOTE]
> No se puede utilizar DDE para consultar el archivo de información de grupo de trabajo de Microsoft Access.

El tema *database* admite los siguientes elementos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Valores devueltos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TableList</p></td>
<td><p>Una lista de tablas</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Una lista de consultas</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Una lista de formularios</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Una lista de informes</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Una lista de macros</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Una lista de módulos</p></td>
</tr>
<tr class="odd">
<td><p>ViewList</p></td>
<td><p>Una lista de vistas</p></td>
</tr>
<tr class="even">
<td><p>StoredProcedureList</p></td>
<td><p>Una lista de procedimientos almacenados</p></td>
</tr>
<tr class="odd">
<td><p>DatabaseDiagramList</p></td>
<td><p>Una lista de diagramas de base de datos</p></td>
</tr>
</tbody>
</table>

<br/>

El siguiente ejemplo muestra cómo se puede abrir el formulario Empleados en la base de datos de ejemplo Northwind desde un procedimiento de Visual Basic:

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a>El tema TABLE

Estos temas utilizan la siguiente sintaxis:

_databasename_ ; **TABLE** _tablename_

_databasename_ ; **QUERY** _queryname_

_databasename_ ; **SQL** [ _sqlstring_ ]

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>databasename</em></p></td>
<td><p>El nombre de la base de datos donde se encuentra la tabla o consulta o a la que se aplica la instrucción SQL, seguido de un punto y coma (;). El nombre de la base de datos puede ser simplemente el nombre (Northwind) o su ruta de acceso completa y la extensión .mdb (C:\Access\Samples\Northwind.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>tablename</em></p></td>
<td><p>El nombre de una tabla existente.</p></td>
</tr>
<tr class="odd">
<td><p><em>queryname</em></p></td>
<td><p>El nombre de una consulta existente.</p></td>
</tr>
<tr class="even">
<td><p><em>sqlstring</em></p></td>
<td><p>Una instrucción SQL válida de hasta 256 caracteres que termina con un punto y coma. Para intercambiar más de 256 caracteres, omita este argumento y utilice instrucciones <strong>DDEPoke</strong> sucesivas para generar una instrucción SQL. Por ejemplo, el siguiente código de Visual Basic utiliza la instrucción <strong>DDEPoke</strong> para generar una instrucción SQL y, a continuación, solicita los resultados de la consulta.</p></td>
</tr>
</tbody>
</table>

<br/>

La siguiente tabla muestra los elementos válidos para los temas TABLA *nombretabla*, CONSULTA *nombreconsulta* y SQL *cadenasql*.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Valores devueltos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Todo</p></td>
<td><p>Todos los datos de la tabla, incluidos los nombres de campo.</p></td>
</tr>
<tr class="even">
<td><p>Datos</p></td>
<td><p>Todas las filas de datos, sin los nombres de campo.</p></td>
</tr>
<tr class="odd">
<td><p>FieldNames</p></td>
<td><p>Una lista de una sola fila con los nombres de campo.</p></td>
</tr>
<tr class="even">
<td><p>FieldNames; T</p></td>
<td><p>Una lista de dos filas con los nombres de campo (primera fila) y los tipos de datos (segunda fila).</p>
<p>Estos son los valores devueltos:</p>
<p>Valor</p>
<p><ul>
<li>0</li>
<li>1 </li>
<li>2 </li>
<li>3 </li>
<li>4 </li>
<li>5 </li>
<li>6 </li>
<li>7 </li>
<li>8 </li>
<li>9 </li>
<li>10  </li>
<li>11</li>
<li>12 </li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p>NextRow</p></td>
<td><p>Los datos en la siguiente fila de la tabla o consulta. Al abrir un canal, NextRow devuelve los datos de la primera fila. Si la fila actual es el último registro y ejecuta NextRow, se produce un error en la solicitud.</p></td>
</tr>
<tr class="odd">
<td><p>PrevRow</p></td>
<td><p>Los datos en la fila anterior de la tabla o consulta. Si PrevRow es la primera solicitud en un nuevo canal, se devolverán los datos en la última fila de la tabla o consulta. Si el primer registro es la fila actual, se produce un error en la solicitud de PrevRow.</p></td>
</tr>
<tr class="even">
<td><p>FirstRow</p></td>
<td><p>Los datos en la primera fila de la tabla o consulta.</p></td>
</tr>
<tr class="odd">
<td><p>LastRow</p></td>
<td><p>Los datos en la última fila de la tabla o consulta.</p></td>
</tr>
<tr class="even">
<td><p>FieldCount</p></td>
<td><p>El número de campos de la tabla o consulta.</p></td>
</tr>
<tr class="odd">
<td><p>SQLText</p></td>
<td><p>Una instrucción SQL que representa la tabla o consulta. Para tablas, este elemento devuelve una instrucción SQL con el formato &quot; SELECT `*` FROM <em>tabla</em>; &quot; .</p></td>
</tr>
<tr class="even">
<td><p>SQLText; <em>n</em></p></td>
<td><p>Una instrucción SQL en fragmentos de <em>n</em> caracteres, que representa la tabla o la consulta y donde <em>n</em> es un entero hasta 256. Por ejemplo, suponga que una consulta está representada por la siguiente instrucción SQL: El elemento SQLText;7 devuelve los siguientes fragmentos delimitados por tabulaciones: El elemento &quot; &quot; SQLText;7 devuelve los siguientes fragmentos delimitados por &quot; &quot; tabulaciones:</p></td>
</tr>
</tbody>
</table>

<br/>

El siguiente ejemplo muestra cómo se puede utilizar DDE en un procedimiento de Visual Basic para solicitar datos de una tabla en la base de datos de ejemplo Northwind e insertar dichos datos en un archivo de texto:

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
