---
título: uso de Microsoft Access como servidor DDE TOCTitle: uso de Microsoft Access como servidor DDE <<<<<<< HEAD ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: ms.date 48546801: 18/09/2015 === Descripción: Microsoft Access admite el intercambio dinámico de datos (DDE) como una aplicación de destino (cliente) o una aplicación de origen (servidor).  
MS:AssetId: a3e82bf7-94b5-8eec-86bc-2d5387d66738 ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15) ms:contentKeyID: ms.date 48546801: 16/10/2018
>>>>>>> maestro mtps_version: Office.15 f1_keywords:
- vbaac10.chm5186349 f1_categories:
- Office.Version=v15
---

# <a name="use-microsoft-access-as-a-dde-server"></a>Uso de Microsoft Access como servidor DDE

**Se aplica a**: Access 2013 | Office 2013 

Microsoft Access admite el intercambio dinámico de datos (DDE) como aplicación de destino (cliente) o aplicación de origen (servidor). Por ejemplo, una aplicación como Microsoft Word, que actúa como cliente, puede solicitar datos a través de DDE de una base de datos de Microsoft Access que actúa como servidor.

> [!TIP]
> [!SUGERENCIA] Si necesita manipular objetos de Microsoft Access desde otra aplicación, considere la posibilidad de usar Automatización.

<<<<<<< Conversación de cabeza A DDE entre un cliente y el servidor se establece sobre un tema concreto. Un tema puede ser un archivo de datos en el formato admitido por la aplicación servidor o puede ser el tema System, que proporciona información sobre la propia aplicación servidor. Una vez iniciada una conversación sobre un tema determinado, sólo se puede transferir un elemento de datos asociado con dicho tema.
=== Una conversación DDE entre un cliente y un servidor se establece sobre un tema concreto. Un tema puede ser un archivo de datos en el formato admitido por la aplicación servidor o puede ser el tema System, que proporciona información sobre la propia aplicación servidor. Una vez iniciada una conversación sobre un tema determinado, sólo un elemento de datos asociado con dicho tema puede transferirse.
>>>>>>> master

Por ejemplo, suponga que está ejecutando Microsoft Word y desea insertar en un documento datos de una determinada base de datos de Microsoft Access. Para iniciar una conversación DDE con Microsoft Access, abra un canal DDE mediante la función **DDEInitiate** y especifique el nombre del archivo de la base de datos como tema. A continuación, podrá transferir los datos de esa base de datos a Microsoft Word a través de dicho canal.

Como servidor DDE, Microsoft Access admite los siguiente temas:

<<<<<<< HEAD
  - El tema System (Sistema)

  - El nombre de una base de datos (tema *database (base de datos)*)

  - El nombre de una tabla (tema *tablename (nombretabla)*)

  - El nombre de una consulta (tema *queryname (nombreconsulta)*)

  - Una cadena SQL de Microsoft Access (tema *sqlstring (cadenasql)*)

Sólo después de establecer una conversación DDE, podrá utilizar la instrucción **DDEExecute** para enviar un comando de la aplicación cliente a la aplicación servidor. Cuando se utiliza como servidor DDE, Microsoft Access reconoce los siguientes elementos como un comando válido:

  - El nombre de una macro en la actual base de datos.

  - Cualquier acción que se pueda realizar en Visual Basic mediante uno de los métodos del objeto **DoCmd**.

  - Las acciones AbrirBaseDeDatos (OpenDatabase) y CerrarBaseDeDatos (CloseDatabase), que se utilizan sólo para las operaciones DDE. (Para ver cómo se utilizan estas funciones, vea el ejemplo que aparece a continuación en este tema.)


> [!NOTE]
> <P>[!NOTA] Al especificar una acción de macro como instrucción <STRONG>DDEExecute</STRONG>, la acción y los argumentos siguen la sintaxis del objeto <STRONG>DoCmd</STRONG> y deben ir entre corchetes ([ ]). Sin embargo, las aplicaciones que admiten DDE no reconocen las constantes intrínsecas en las operaciones DDE. Asimismo, los argumentos de cadena deben ir entre comillas (" ") si la cadena contiene una coma. En caso contrario, no son necesarias las comillas.</P>



La aplicación cliente puede utilizar la función **DDERequest** para solicitar datos de texto de la aplicación servidor a través de un canal DDE abierto. O bien, el cliente puede utilizar la instrucción **DDEPoke** para enviar datos a la aplicación servidor. Tras finalizar la transferencia de datos, el cliente puede utilizar la instrucción **DDETerminate** para cerrar el canal DDE o la instrucción **DDETerminateAll** para cerrar todos los canales abiertos.


> [!NOTE]
> <P>[!NOTA] Cuando la aplicación cliente termine de recibir datos a través de un canal DDE, deberá cerrar dicho canal para conservar los recursos de la memoria.</P>


=======
- El tema System (Sistema)

- El nombre de una base de datos (tema *database (base de datos)*)

- El nombre de una tabla (tema *tablename (nombretabla)*)

- El nombre de una consulta (tema *queryname (nombreconsulta)*)

- Una cadena SQL de Microsoft Access (tema *sqlstring (cadenasql)*)

Después de establecer una conversación DDE, puede usar la instrucción **DDEExecute** para enviar un comando desde el cliente a la aplicación de servidor. Cuando se utiliza como servidor DDE, Microsoft Access reconoce los siguientes elementos como un comando válido:

- El nombre de una macro en la actual base de datos.

- Cualquier acción que se pueda realizar en Visual Basic mediante uno de los métodos del objeto **DoCmd**.

- Las acciones AbrirBaseDeDatos (OpenDatabase) y CerrarBaseDeDatos (CloseDatabase), que se utilizan sólo para las operaciones DDE. (Para ver cómo se utilizan estas funciones, vea el ejemplo que aparece a continuación en este tema.)

> [!NOTE]
> [!NOTA] Al especificar una acción de macro como instrucción **DDEExecute**, la acción y los argumentos siguen la sintaxis del objeto **DoCmd** y deben ir entre corchetes ([ ]). Sin embargo, las aplicaciones que admiten DDE no reconocen las constantes intrínsecas en las operaciones DDE. Asimismo, los argumentos de cadena deben ir entre comillas (" ") si la cadena contiene una coma. En caso contrario, no son necesarias las comillas.

La aplicación cliente puede utilizar la función **DDERequest** para solicitar datos de texto de la aplicación servidor a través de un canal DDE abierto. O bien, el cliente puede utilizar la instrucción **DDEPoke** para enviar datos a la aplicación servidor. Una vez completada la transferencia de datos, el cliente puede usar la instrucción **DDETerminate** para cerrar el canal DDE o la instrucción **DDETerminateAll** para cerrar todos los canales abiertos.

> [!NOTE]
> [!NOTA] Cuando la aplicación cliente termine de recibir datos a través de un canal DDE, deberá cerrar dicho canal para conservar los recursos de la memoria.
>>>>>>> master

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

<a name="-head"></a><<<<<<< HEAD
=======
<br/>

>>>>>>> patrón de que las secciones siguientes proporcionan información acerca de los temas DDE válidos que admite Microsoft Access.

## <a name="the-system-topic"></a>El tema System (Sistema)

<<<<<<< HEAD del sistema es un tema estándar para todas las aplicaciones basadas en Windows de Microsoft. Facilita información sobre los demás temas que admite la aplicación. Para obtener acceso a esta información, el código debe llamar primero a la función **DDEInitiate** con como el argumento *tema* y, a continuación, ejecutar la instrucción **DDERequest** con uno de los siguientes para el argumento de *elemento* .
=== El tema System es un tema estándar para todas las aplicaciones basadas en Windows de Microsoft. Facilita información sobre los demás temas que admite la aplicación. Para obtener acceso a esta información, el código debe llamar primero a la función **DDEIniciar (DDEInitiate)** con el argumento *tema* y, a continuación, ejecutar la instrucción **DDERequest** con uno de los siguientes argumentos *elemento* .
>>>>>>> master

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Devuelve</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SysItems</p></td>
<td><p>Una lista de elementos que admite el tema System en Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p>Formats</p></td>
<td><p>Una lista de formatos que Microsoft Access puede copiar al Portapapeles.</p></td>
</tr>
<tr class="odd">
<td><p>Status</p></td>
<td><p>&quot;Ocupado&quot; o &quot;listo&quot;.</p></td>
</tr>
<tr class="even">
<td><p>Topics</p></td>
<td><p>Una lista de todas las bases de datos abiertas.</p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><<<<<<< HEAD
=======
<br/>
>>>>>>> master

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

## <a name="the-database-topic"></a>El tema de la base de datos

El tema de la *base de datos* es el nombre de archivo de base de datos existente. Puede escribir simplemente el nombre (Northwind) o su ruta de acceso y la extensión .mdb (C:\\Access\\ejemplos\\Neptuno.mdb). Tras iniciar una conversación DDE con la base de datos, puede solicitar una lista de los objetos incluidos en dicha base de datos.

<<<<<<< HEAD

> [!NOTE]
> <P>[!NOTA] No se puede utilizar DDE para consultar el archivo de información de grupo de trabajo de Microsoft Access.</P>


=======
> [!NOTE]
> [!NOTA] No se puede utilizar DDE para consultar el archivo de información de grupo de trabajo de Microsoft Access.
>>>>>>> master

El tema *database* admite los siguientes elementos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Devuelve</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ListaDeTablas</p></td>
<<<<<<< HEAD
<td><p>Una lista de tablas.</p></td>
</tr>
<tr class="even">
<td><p>QueryList</p></td>
<td><p>Una lista de consultas.</p></td>
</tr>
<tr class="odd">
<td><p>FormList</p></td>
<td><p>Una lista de formularios.</p></td>
</tr>
<tr class="even">
<td><p>ReportList</p></td>
<td><p>Una lista de informes.</p></td>
</tr>
<tr class="odd">
<td><p>MacroList</p></td>
<td><p>Una lista de macros.</p></td>
</tr>
<tr class="even">
<td><p>ModuleList</p></td>
<td><p>Una lista de módulos.</p></td>
=======
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
>>>>>>>patrón
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

<a name="-head"></a><<<<<<< HEAD
=======
<br/>
>>>>>>> master

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

## <a name="the-table-topic"></a>El tema de la tabla

Estos temas utilizan la siguiente sintaxis:

_databasename_ ; **Tabla** _TableName_

_databasename_ ; **Consulta** _nombreconsulta_

_databasename_ ; **SQL** [ _cadenasql_ ]

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
<td><p><em>nombrebasedatos</em></p></td>
<td><p>El nombre de la base de datos donde se encuentra la tabla o consulta o a la que se aplica la instrucción SQL, seguido de un punto y coma (;). El nombre de la base de datos puede ser simplemente el nombre (Northwind) o su ruta de acceso completa y la extensión .mdb (C:\Access\Samples\Northwind.mdb).</p></td>
</tr>
<tr class="even">
<td><p><em>nombretabla</em></p></td>
<td><p>El nombre de una tabla existente.</p></td>
</tr>
<tr class="odd">
<td><p><em>nombreconsulta</em></p></td>
<td><p>El nombre de una consulta existente.</p></td>
</tr>
<tr class="even">
<td><p><em>sqlstring</em></p></td>
<td><p>Una instrucción SQL válida hasta 256 caracteres de longitud, que terminan con un punto y coma. Para intercambiar más de 256 caracteres, omita este argumento y utilice instrucciones <strong>DDEPoke</strong> sucesivas para generar una instrucción SQL. Por ejemplo, el siguiente código de Visual Basic utiliza la instrucción <strong>DDEPoke</strong> para generar una instrucción SQL y, a continuación, solicita los resultados de la consulta.</p></td>
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
<th><p>Devuelve</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Todos</p></td>
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
<<<<<<< HEAD
<td><p>Una lista de dos filas con los nombres de campo (primera fila) y los tipos de datos (segunda fila).</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>Éstos son los valores devueltos y los tipos de datos que representan.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><b>Valor</b></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>8</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>11</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>12</p></td>
=======
<td><p>Una lista de dos filas con los nombres de campo (primera fila) y los tipos de datos (segunda fila).</p>
<p>Estos son los valores devueltos:</p>
<p>Valor</p>
<p><ul>
<li>0</li>
<li>1</li>
<li>2</li>
<li>3</li>
<li>4</li>
<li>5</li>
<li>6</li>
<li>7</li>
<li>8</li>
<li>9</li>
<li>10</li>
<li>11</li>
<li>12</li>
</ul>
</p>
</td>
>>>>>>>patrón
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
<td><p>Una instrucción SQL que representa la tabla o consulta. Para las tablas, este elemento devuelve una instrucción SQL en el formulario &quot;seleccione `*` de <em>tabla</em>; &quot;.</p></td>
</tr>
<tr class="even">
<td><p>SQLText;<em>n</em></p></td>
<td><p>Una instrucción SQL, en <em>n</em>-carácter fragmentos, que representa la tabla o consulta, donde <em>n</em> es un entero hasta 256. Por ejemplo, suponga que una consulta está representada por la siguiente instrucción SQL: el elemento &quot;SQLText; 7&quot; devuelve los siguientes fragmentos delimitado por tabulaciones: el elemento &quot;SQLText; 7&quot; devuelve los siguientes fragmentos delimitado por tabulaciones:</p></td>
</tr>
</tbody>
</table>

<a name="-head"></a><<<<<<< HEAD
=======
<br/>
>>>>>>> master

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
